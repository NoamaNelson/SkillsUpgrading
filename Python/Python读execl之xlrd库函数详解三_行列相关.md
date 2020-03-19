### 博客地址：[https://blog.csdn.net/NoamaNelson/article/details/102912382](https://blog.csdn.net/NoamaNelson/article/details/102912382)  

## 准备工作：


-  准备工作和所用材料和《Python读execl之xlrd库函数详解一：工作簿相关》一致。  
![](https://img-blog.csdnimg.cn/20191104174206561.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
## 库函数：
### 行、列相关


- **row_len(self, rowx)	#返回该列的有效单元格长度**  
    
		#-*- encoding:utf-8 -*-
	
		import xlrd,json
		
		def openexec():
		    book1 = xlrd.open_workbook('datalist.xlsx') # 打开表格
		    a = book1.sheet_by_name(u"附件2《自费家属体检名单统计表》") # 使用sheet名称获取工作簿
		    print(a.row_len(15))	#返回第15列的有效单元格长度	
		openexec()

> 输出结果为：16，如图：  
![](https://img-blog.csdnimg.cn/20191105112500369.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  


- **row(self, rowx)	#返回由该行中所有的单元格对象组成的列表**  
       
		 print(str(a.row(3).decode("unicode-escape"))
> 输出结果为：[number:1.0, text:u’0054’, text:u’张1’, text:u’12451’, text:u’体系54’, text:u’部门54’, text:u’岗位54’, text:u’赵1’, text:u’配偶父母’, number:176.0, text:u’已婚’, text:u’12465’, number:199054.0, number:59.0, text:u’女’, text:u’女’]  

- **get_rows(self)	#返回遍历每一行的生成器**  
        
		print(a.get_rows())  
> 输出结果为：<generator object at 0x0000000002EB6120>  

- **row_types(self, rowx, start_colx=0, end_colx=None)	#返回由该行中所有单元格的数据类型组成的列表**  

        print(a.row_types(5))  

> 输出结果为：array(‘B’, [2, 1, 1, 1, 1, 1, 1, 1, 1, 2, 1, 1, 2, 2, 1, 1])  

- **row_values(self, rowx, start_colx=0, end_colx=None)	#返回由该行中所有单元格的数据组成的列表**  

        print(str(a.row_values(5)).decode("unicode-escape")) #需要进行格式转换
> 输出结果为：[3.0, u’0056’, u’张3’, u’12453’, u’体系56’, u’部门56’, u’岗位56’, u’赵3’, u’配偶父母’, 178.0, u’已婚’, u’12467’, 199056.0, 66.0, u’女’, u’女’]  

- **row_slice(self, rowx, start_colx=0, end_colx=None)	#返回由该行中所有单元格的对象组成的列表**  
        
		print(str(a.row_slice(5)).decode("unicode-escape")) #需要进行格式转换  
> 输出结果为：[number:3.0, text:u’0056’, text:u’张3’, text:u’12453’, text:u’体系56’, text:u’部门56’, text:u’岗位56’, text:u’赵3’, text:u’配偶父母’, number:178.0, text:u’已婚’, text:u’12467’, number:199056.0, number:66.0, text:u’女’, text:u’女’]  

- **col_slice(self, colx, start_rowx=0, end_rowx=None)	#返回由该列中所有单元格的对象组成的列表**  

        print(str(a.col_slice(0)).decode("unicode-escape")) #需要进行格式转换，表格有合并，所以只有1列

> 输出结果为：[text:u’员工自费家属体检名单’, text:u’诺瓦员工信息填写’, text:u’序号’, number:1.0, number:2.0, number:3.0, number:4.0, number:5.0, number:6.0, number:7.0, number:8.0, number:9.0, number:10.0, number:11.0, number:12.0, number:13.0, number:14.0, number:15.0, number:16.0, number:17.0, number:18.0, number:19.0, number:20.0, number:21.0, number:22.0, number:23.0, number:24.0, number:25.0, number:26.0, number:27.0, number:28.0, number:29.0, number:30.0, number:31.0, number:32.0, number:33.0, number:34.0, number:35.0, number:36.0, number:37.0, number:38.0, number:39.0, number:40.0, number:41.0, number:42.0, number:43.0, number:44.0, number:45.0, number:46.0, number:47.0, number:48.0, number:49.0, number:50.0, number:51.0, number:52.0, number:53.0, number:54.0, number:55.0, number:56.0, number:57.0, number:58.0, number:59.0, number:60.0, number:61.0, number:62.0, number:63.0, number:64.0, number:65.0, number:66.0, number:67.0, number:68.0, number:69.0, number:70.0, number:71.0, number:72.0, number:73.0, number:74.0, number:75.0, number:76.0, number:77.0, number:78.0, number:79.0, number:80.0, number:81.0, number:82.0, number:83.0, number:84.0, number:85.0, number:86.0, number:87.0, number:88.0, number:89.0, number:90.0, number:91.0, number:92.0, number:93.0, number:94.0, number:95.0, number:96.0, number:97.0, number:98.0, number:99.0, number:100.0, number:101.0, number:102.0, number:103.0, number:104.0, number:105.0, number:106.0, number:107.0, number:108.0, number:109.0, number:110.0, number:111.0, number:112.0, number:113.0, number:114.0, number:115.0, number:116.0, number:117.0, number:118.0, number:119.0, number:120.0, number:121.0, number:122.0, number:123.0, number:124.0, number:125.0, number:126.0, number:127.0, number:128.0, number:129.0, number:130.0, number:131.0, number:132.0, number:133.0, number:134.0, number:135.0, number:136.0, number:137.0, number:138.0, number:139.0, number:140.0, number:141.0, number:142.0, number:143.0, number:144.0, number:145.0, number:146.0, number:147.0, number:148.0, number:149.0, number:150.0, number:151.0, number:152.0, number:153.0, number:154.0, number:155.0, number:156.0, number:157.0, number:158.0, number:159.0, number:160.0, number:161.0, number:162.0, number:163.0, number:164.0, number:165.0, number:166.0, number:167.0, number:168.0, number:169.0, number:170.0, number:171.0, number:172.0, number:173.0, number:174.0, number:175.0, number:176.0, number:177.0, number:178.0, number:179.0, number:180.0, number:181.0, number:182.0, number:183.0, number:184.0, number:185.0, number:186.0, number:187.0, number:188.0, number:189.0, number:190.0, number:191.0, number:192.0, number:193.0, number:194.0, number:195.0, number:196.0, number:197.0, number:198.0, number:199.0, number:200.0]  



- **col_values(self, colx, start_rowx=0, end_rowx=None)	#返回由该列中所有单元格的数据组成的列表**  
        
		print(str(a.col_values(0)).decode("unicode-escape")) #需要进行格式转换，表格有合并，所以只有1列  


> 输出结果为：[u’员工自费家属体检名单’, u’诺瓦员工信息填写’, u’序号’, 1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0, 8.0, 9.0, 10.0, 11.0, 12.0, 13.0, 14.0, 15.0, 16.0, 17.0, 18.0, 19.0, 20.0, 21.0, 22.0, 23.0, 24.0, 25.0, 26.0, 27.0, 28.0, 29.0, 30.0, 31.0, 32.0, 33.0, 34.0, 35.0, 36.0, 37.0, 38.0, 39.0, 40.0, 41.0, 42.0, 43.0, 44.0, 45.0, 46.0, 47.0, 48.0, 49.0, 50.0, 51.0, 52.0, 53.0, 54.0, 55.0, 56.0, 57.0, 58.0, 59.0, 60.0, 61.0, 62.0, 63.0, 64.0, 65.0, 66.0, 67.0, 68.0, 69.0, 70.0, 71.0, 72.0, 73.0, 74.0, 75.0, 76.0, 77.0, 78.0, 79.0, 80.0, 81.0, 82.0, 83.0, 84.0, 85.0, 86.0, 87.0, 88.0, 89.0, 90.0, 91.0, 92.0, 93.0, 94.0, 95.0, 96.0, 97.0, 98.0, 99.0, 100.0, 101.0, 102.0, 103.0, 104.0, 105.0, 106.0, 107.0, 108.0, 109.0, 110.0, 111.0, 112.0, 113.0, 114.0, 115.0, 116.0, 117.0, 118.0, 119.0, 120.0, 121.0, 122.0, 123.0, 124.0, 125.0, 126.0, 127.0, 128.0, 129.0, 130.0, 131.0, 132.0, 133.0, 134.0, 135.0, 136.0, 137.0, 138.0, 139.0, 140.0, 141.0, 142.0, 143.0, 144.0, 145.0, 146.0, 147.0, 148.0, 149.0, 150.0, 151.0, 152.0, 153.0, 154.0, 155.0, 156.0, 157.0, 158.0, 159.0, 160.0, 161.0, 162.0, 163.0, 164.0, 165.0, 166.0, 167.0, 168.0, 169.0, 170.0, 171.0, 172.0, 173.0, 174.0, 175.0, 176.0, 177.0, 178.0, 179.0, 180.0, 181.0, 182.0, 183.0, 184.0, 185.0, 186.0, 187.0, 188.0, 189.0, 190.0, 191.0, 192.0, 193.0, 194.0, 195.0, 196.0, 197.0, 198.0, 199.0, 200.0]  

- **col_types(self, colx, start_rowx=0, end_rowx=None)	#返回由该列中所有单元格的数据类型组成的列表**  
        
		print(str(a.col_types(0)).decode("unicode-escape")) #需要进行格式转换，表格有合并，所以只有1列  
> 输出结果为：[1, 1, 1, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2]