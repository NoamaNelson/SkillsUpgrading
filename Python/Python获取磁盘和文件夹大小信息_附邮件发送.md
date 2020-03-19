### 博客地址：[https://blog.csdn.net/NoamaNelson/article/details/103141231](https://blog.csdn.net/NoamaNelson/article/details/103141231)
【学习笔记】Python获取磁盘、文件夹大小信息（一）中已经描述了怎么获取文件的大小，磁盘的大小。
本次笔记增加邮件服务，这样可以更好的掌握磁盘的运行状态。  
## 发送邮件  
    def sendmail(sub, con):
	    msg = email.mime.multipart.MIMEMultipart()
	    msg['from'] = "xxx.com" # 发邮件的邮箱地址
	    msg['to'] = "yyy.com" # 收邮件的邮箱地址
	    msg['subject'] = sub # 邮件标题
	    content = con # 邮件内容
	    txt = email.mime.text.MIMEText(content)
	    msg.attach(txt)
	    smtp = smtplib.SMTP()
	    smtp.connect('smtp.126.com') #使用的邮件服务
	    smtp.login('xxx.com', 'zzz') # 登录发邮件的邮箱账号和密码
	    smtp.sendmail(msg['from'], msg['to'],str(msg)) # 发邮件格式
	    smtp.quit()    
	sendmail("当前磁盘的运行状态", str(ddddd), encoding='GBK' ) # str(ddddd)需要发送的内容  

## 获取D：\image的大小，然后此文件夹会不停的写入文件，当D盘剩余空间小于5GB时，给出警告信息，并把警告信息写入log文件中，然后把log中的内容读取出来放入邮件正文，发送邮件  
    """
	Author:NoamaNelson
	Date:2019-11-19
	Discription:Get the size of D:\\image, and then this folder will keep writing files. 
	When the remaining space of D disk is less than 5GB, a warning message will be given
	"""

	import os
	import os.path
	import smtplib
	import email.mime.multipart
	import email.mime.text
	import sendmail
	import psutil
	import collections


	def get_size(path):
	    list1 = []
	    fileList = os.listdir(path)  # 获取path目录下所有文件
	    for filename in fileList:
	        pathTmp = os.path.join(path,filename)  # 获取path与filename组合后的路径
	        if os.path.isdir(pathTmp):   # 判断是否为目录
	            get_size(pathTmp)        # 是目录就继续递归查找
	        elif os.path.isfile(pathTmp):  # 判断是否为文件
	            filesize = os.path.getsize(pathTmp)  # 如果是文件，则获取相应文件的大小
	            #print('目录中的子文件大小：%d字节' % filesize)
	            list1.append(filesize)      # 将文件的大小添加到列表
	    print('%s 目录中的文件总大小：%d 字节' % (path, sum(list1)))
	    print('%s 目录中的文件总大小: %.4f MB' % (path, (sum(list1)/1024/1024)))
	    print('%s 目录中的文件总大小: %.4f GB' % (path, (sum(list1)/1024/1024/1024)))
	    return sum(list1)
    
	def get_disk_info():
	    disk_used = {}
	    for id in psutil.disk_partitions():
	        if 'cdrom' in id.opts or id.fstype == '':
	            continue
	        disk_name = id.device.split(':')
	        s = disk_name[0]
	        disk_info = psutil.disk_usage(id.device)
	        #print(disk_info)
	        disk_used[s + '盘使用率：'] = '{}%'.format(disk_info.percent)
	        disk_used[s + '剩余空间：'] = '{}GB'.format(disk_info.free // 1024 // 1024 // 1024)
	    print("sdsds:%s"%disk_used)
	    return disk_used

	def sendmail(sub, con):
	    msg = email.mime.multipart.MIMEMultipart()
	    msg['from'] = "xxx.com" # 发邮件的邮箱地址
	    msg['to'] = "yyy.com" # 收邮件的邮箱地址
	    msg['subject'] = sub # 邮件标题
	    content = con # 邮件内容
	    txt = email.mime.text.MIMEText(content)
	    msg.attach(txt)
	    smtp = smtplib.SMTP()
	    smtp.connect('smtp.126.com') #使用的邮件服务
	    smtp.login('xxx.com', 'zzz') # 登录发邮件的邮箱账号和密码
	    smtp.sendmail(msg['from'], msg['to'],str(msg)) # 发邮件格式
	    smtp.quit()

	if __name__ == "__main__":   
	    #path= input("输入路径：").strip()  #指定文件路径
	    log_name = 'result.log'
	    with open(log_name, 'w') as f:
	        path = r"D:\\image"
	        disk_used1 = get_disk_info()
	        for k, v in disk_used1.items():
	            f.write('{}{}。\n'.format(k, v))
	        list2 = get_size(path)
	        f.write('%s 目录中的文件总大小：%d 字节\n' % (path, list2))
	        f.write('%s 目录中的文件总大小: %.4f MB\n' % (path, (list2/1024/1024)))
	        f.write('%s 目录中的文件总大小: %.4f GB\n' % (path, (list2/1024/1024/1024)))
	        disk_used2 = disk_used1['D剩余空间：']
	        disk_used3 = int(disk_used2.split('G')[0])
	        #intlist2 = intlist1/1024/1024/1024
	        if disk_used3 > 20:
	            print("D剩余空间：%s"%disk_used1['D剩余空间：'])
	            f.write("D剩余空间：%s"%disk_used1['D剩余空间：'])
	        elif disk_used3 <= 20:
	            print("D盘剩余空间为%dGB,建议停止数据存储"%disk_used3)  
	            f.write("D盘剩余空间为%dGB,建议停止数据存储"%disk_used3)
	    with open(log_name, 'rb') as logfile:
	        sendmail("磁盘当前存储状态", str(logfile.read(), encoding='GBK'))  
## 收到的邮件效果  

![](https://img-blog.csdnimg.cn/20191119144824888.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)