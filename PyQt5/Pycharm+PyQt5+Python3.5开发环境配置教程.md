### 博客地址：[https://blog.csdn.net/NoamaNelson/article/details/103048773](https://blog.csdn.net/NoamaNelson/article/details/103048773)  

## Pycharm安装、破解、汉化  
[https://www.jb51.net/softs/598511.html](https://www.jb51.net/softs/598511.html)  

## Python3.5安装  
### 1、下载  
[https://www.python.org/downloads/](https://www.python.org/downloads/)  
### 2、选择3.5（根据自身系统选择）版本下载  
![](https://img-blog.csdnimg.cn/20191113145208860.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
![](https://img-blog.csdnimg.cn/20191113145307678.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
### 3、下载完成，直接双击运行，即可，安装路径可选  
（注意：在双击运行后，打开安装程序界面，建议选择“增加环境变量”）  
![](https://img-blog.csdnimg.cn/20191113145422307.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
### 4、环境变量设置    
如果步骤3已经勾选了“增加环境变量”的话，就不用再设置环境变量。如果没有勾选，环境变量设置方法如下：
找到自己的Python3.5的安装路径（例如我的是：D:\Python 3.5），把以下几个路径添加到系统环境变量中。  
①计算机–邮件–属性，打开如下界面：  
![](https://img-blog.csdnimg.cn/20191113145919470.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  

②点击“高级系统设置”，再点击“环境变量”，如下：   
![](https://img-blog.csdnimg.cn/2019111314592795.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)   
![](https://img-blog.csdnimg.cn/20191113145935475.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
③在系统变量中找到path，双击打开path，然后再路径的最末尾加入：
Python的路径，要以“;”隔开，即可：  

    D:\Python35; D:\Python35\Lib; D:\Python35\Scripts;  
![](https://img-blog.csdnimg.cn/20191113145959922.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)   
④验证Python是否安装成功，开始—输入“cmd”，回车打开命令行，输入：Python，看到如下界面就表示Python安装成功。  
![](https://img-blog.csdnimg.cn/2019111315010765.png)   
## Pip安装  
以上安装python3.5的时候，默认已经安装了pip工具，这里直接升级pip到最新即可。  

    python -m install --upgrade pip  
## PyQt5安装  

    pip install pyqt5  
	pip install pyqt5-tools   
## Pycharm中编译工具设置及pyqt5包的导入  
- 新建一个项目
- Ctrl+Alt+S，打开设置界面，点击项目下的“Project Interpreter”
![](https://img-blog.csdnimg.cn/20191113150723845.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)
- 点击如图的设置按钮
![](https://img-blog.csdnimg.cn/2019111315084495.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
- 点击“Add…”  
![](https://img-blog.csdnimg.cn/20191113150934833.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
- 设置编译工具python.exe，具体根据自己的路径选择  
![](https://img-blog.csdnimg.cn/20191113151110594.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
- 此时会自动导入编译工具下的包  
![](https://img-blog.csdnimg.cn/20191113151146660.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
## 指定Qt Designer  
- Ctrl+Alt+S，打开设置界面，点击“工具-外部工具”，点击“+”
![](https://img-blog.csdnimg.cn/20191113151535385.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
- 设置参数如下：  
![](https://img-blog.csdnimg.cn/20191113151613531.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  

① program： 
 
    D:\Python 3.5\Lib\site-packages\pyqt5_tools\Qt\bin\designer.exe,（换成自己的目录即可）  

②arguments： 
 
    $FileDir$\$FileName$ 
③working directory：  

    $FileDir$
## 指定PyUIC5  
- 步骤和添加Qt Designer一模一样  
- 作用：把qt的UI文件转换成.py文件的工具  
- 具体参数如下：  
![](https://img-blog.csdnimg.cn/20191113152245469.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  

① program：  

    D:\Python 3.5\Scripts\pyuic5.exe（换成自己的目录即可）  

②arguments：
  
    $FileName$ -o $FileNameWithoutExtension$.py  

③working directory：  

    $FileDir$
## 指定PyRcc5  
- 步骤和添加PyUIC5一模一样  
- 作用：将资源文件如图片等转成python代码能识别的文件  
- 具体参数如下：  
![](https://img-blog.csdnimg.cn/20191113152622793.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  

① program：  

    D:\Python 3.5\Scripts\pyrcc5.exe（换成自己的目录即可）  

②arguments：  

    $FileName$ -o $FileNameWithoutExtension$.py  

③working directory：  

    $FileDir$  

## PyInstaller安装  
- 作用：打包命令：cmd控制台到F:\Python 3.5\Scripts路径下,输入命令 pyinstaller.exe -F f:\prj\hello.py，
即可生成一个hello.exe独立的执行文件;不使用-F命令将会一同生成依赖库
- 安装指令：  

    	pip3 install pyinstaller  

## 查看是否配置OK  
在Pycharm主界面，点击“工具-外部工具”，就可以看到自己添加的几个外部工具了  
![](https://img-blog.csdnimg.cn/20191113153044968.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
## 简单写一个程序预热下  
- 打开QT designer，设计如下一个UI图：
![](https://img-blog.csdnimg.cn/2019111317575833.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
- 然后点击保存，或者另存到项目的目录，如：UI文件为untitled.ui
- 在untitled.ui文件右键，external tools->pyuic5，生成py代码,生成untitled.py
- 在该项目下另外再新建一个py文件test.py用于运行调用untitled.py 
## untitled.py  

    # -*- coding: utf-8 -*-

	from PyQt5 import QtCore, QtGui, QtWidgets

	class Ui_MainWindow(object):
	    def setupUi(self, MainWindow):
	        MainWindow.setObjectName("MainWindow")
	        MainWindow.resize(800, 600)
	        self.centralwidget = QtWidgets.QWidget(MainWindow)
	        self.centralwidget.setObjectName("centralwidget")
	        self.textEdit = QtWidgets.QTextEdit(self.centralwidget)
	        self.textEdit.setGeometry(QtCore.QRect(180, 50, 441, 411))
	        self.textEdit.setObjectName("textEdit")
	        MainWindow.setCentralWidget(self.centralwidget)
	        self.statusbar = QtWidgets.QStatusBar(MainWindow)
	        self.statusbar.setObjectName("statusbar")
	        MainWindow.setStatusBar(self.statusbar)
	        self.menubar = QtWidgets.QMenuBar(MainWindow)
	        self.menubar.setGeometry(QtCore.QRect(0, 0, 800, 23))
	        self.menubar.setObjectName("menubar")
	        self.menutes = QtWidgets.QMenu(self.menubar)
	        self.menutes.setObjectName("menutes")
	        MainWindow.setMenuBar(self.menubar)
	        self.menubar.addAction(self.menutes.menuAction())
	
	        self.retranslateUi(MainWindow)
	        QtCore.QMetaObject.connectSlotsByName(MainWindow)
	
	    def retranslateUi(self, MainWindow):
	        _translate = QtCore.QCoreApplication.translate
	        MainWindow.setWindowTitle(_translate("MainWindow", "MainWindow"))
	        self.textEdit.setHtml(_translate("MainWindow", "<!DOCTYPE HTML PUBLIC \"-//W3C//DTD HTML 4.0//EN\" \"http://www.w3.org/TR/REC-html40/strict.dtd\">\n"
	"<html><head><meta name=\"qrichtext\" content=\"1\" /><style type=\"text/css\">\n"
	"p, li { white-space: pre-wrap; }\n"
	"</style></head><body style=\" font-family:\'SimSun\'; font-size:9pt; font-weight:400; font-style:normal;\">\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                            _ooOoo_  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                           o8888888o  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                          88  .  88  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                           (| -_- |)  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                            O\\\\ = /O  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                        ____/`---\'\\\\____ </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                     .   \' \\\\| |// `. </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                       / \\\\||| : |||// \\\\  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                     / _||||| -:- |||||- \\\\ </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                       | | \\\\\\\\\\\\ - /// | |  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                     | \\\\_| \'\'\\\\---/\'\' | |  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                      \\\\ .-\\\\__ `-` ___/-. /  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                   ___`. .\' /--.--\\\\ `. . __  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                .&quot;&quot; \'&lt; `.___\\\\_&lt;|&gt;_/___.\' &gt;\'&quot;&quot;.  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">               | | : `- \\\\`.;`\\\\ _ /`;.`/ - ` : | |  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                 \\\\ \\\\ `-. \\\\_ __\\\\ /__ _/ .-` / /  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">         ======`-.____`-.___\\\\_____/___.-`____.-\'======  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                            `=---=\'  &quot;)</p>\n"
	"<p style=\"-qt-paragraph-type:empty; margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\"><br /></p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">           .............................................  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                 佛祖镇楼                  BUG辟易</p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">          佛曰:  </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                  写字楼里写字间，写字间里程序员；</p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                  程序人员写程序，又拿程序换酒钱。 </p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                  酒醒只在网上坐，酒醉还来网下眠；</p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                  酒醉酒醒日复日，网上网下年复年。</p>\n"
	"<p style=\" margin-top:0px; margin-bottom:0px; margin-left:0px; margin-right:0px; -qt-block-indent:0; text-indent:0px;\">                  但愿老死电脑间，不愿鞠躬老板前； </p></body></html>"))
        self.menutes.setTitle(_translate("MainWindow", "Testing"))
## test.py  
    import sys

	import untitled
	from PyQt5 import QtWidgets
	#from PyQt5.QtWidgets import QApplication,QMainWindow
	from untitled import Ui_MainWindow
	
	
	if __name__ == "__main__":
	    app = QtWidgets.QApplication(sys.argv)
	    MainWindow = QtWidgets.QMainWindow()
	    ui = untitled.Ui_MainWindow()
	    ui.setupUi(MainWindow)
	    MainWindow.show()
	    sys.exit(app.exec_())  

## 直接运行test.py，即可  
![](https://img-blog.csdnimg.cn/20191113180343108.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L05vYW1hTmVsc29u,size_16,color_FFFFFF,t_70)  
