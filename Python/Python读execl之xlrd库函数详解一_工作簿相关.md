### 博客地址：  [https://blog.csdn.net/NoamaNelson/article/details/102901296](https://blog.csdn.net/NoamaNelson/article/details/102901296)  
Python读execl主要用到xlrd库，用到主要函数详解如下：  
@[TOC] (目录)  

## 准备工作： 


- 安装xlrd库：  
    
    `pip install xlrd`



- 待读取的execl文件，本文使用如下：
文件名：datalist.xlsx
文件内容：（里边的数据只是示例，非真实数据，切勿计较） 
![](https://img-blog.csdnimg.cn/20191104174206561.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
## 库函数：
### 工作簿相关 


- **open_workbook(filename=None,
logfile=sys.stdout, verbosity=0, use_mmap=USE_MMAP,
file_contents=None,
encoding_override=None,
formatting_info=False, on_demand=False, ragged_rows=False)	#打开工作表**  

`#-*- encoding:utf-8 -*-`    
    
	import xlrd,json  

	def openexec():  
		book1 = xlrd.open_workbook('datalist.xlsx')  
		print(book1)  
	openexec() 


结果输出：`<xlrd.book.Book object at 0x0000000002F10358>`，说明文件打开OK

- **sheet_names(self)	#获取所有的sheet名称**

``   

    w = json.dumps(book1.sheet_names(),encoding='utf-8',ensure_ascii=False) # 避免输出中文乱码   
    print(book1.name)   

结果输出：   ` [“附件1《员工家属体检名单统计表》”, “附件2《自费家属体检名单统计表》”, “附件3《其他信息》”]`
    `那么w[2:18] = 附件1《员工家属体检名单统计表》`



- **sheet_by_index(self, sheetx) #通过下表获取所有的sheet名称**   

``

    q = book1.sheet_by_index(1).name #获取下表为1的sheet名称  
    print(q)
     


结果输出：`附件2《自费家属体检名单统计表》`

- **sheet_by_name(self, sheet_name)	#直接通过sheet的名称来锁定某个sheet**  

``

	e = book1.sheet_by_name(u"附件2《自费家属体检名单统计表》").name 
    print(e)

结果输出：`附件2《自费家属体检名单统计表》`



- **sheet_loaded(self, sheet_name_or_index)	#判断对应的sheet是否加载成功**  

``

	r = book1.sheet_loaded(2)
    print(r)

结果输出：`True`



- **unload_sheet(self, sheet_name_or_index)	#取消加载**  

``

	t = book1.sheet_loaded(2)  
    print(t)

结果输出：`None`



- **release_resources(self)	#资源释放**  

``

	y = book1.release_resources()  
    print(y)

结果输出：`None`

