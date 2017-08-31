## python环境及其基本语法

忠告：卸载windows，换成Linux，你将提升自己的开发效率。

### python能干嘛？

1. 写脚本
2. 爬虫，丰富的爬虫库，满足各种爬虫需求
3. 网站开发，豆瓣和知乎都是python开发的，flask，django都是比较流行的web开发框架，小，上手容易。但是我不会
4. 数据计算，丰富的数据计算库，目前是你能想到的数学计算或者变换大部分都能能帮你实现。
5. spark上有原生的python支持，能够进行分布式计算
6. …...

### python的环境配置

目前在python的版本中，2.7和3.5+。这是2个大版本。

**2.7版本**

优点：

1. 扩展库丰富，目前知道的库都是有2.7的版本的。有些可能默认链接不是了，但是你可以下载以前的版本
2. 版本稳定，2.7有在维护，经历了很多年，修复了很多bug。很多大厂都是用2.7
3. 使用环境广，Linux环境下，基本上都有2.7的版本。

缺点：

1. 中文支持不友好，各种便民，各种乱码，默认为asscii编码。
2. 有些语法上，感觉很不好，‘<>’和‘!=’ ,都是表示不等于，在语法上有很多不规范的地方（不同方式表示不同意思，这样可读性不爽）
3. 占用内存很大，尽管python3.5也还是很占内存，但是比python2还是小点（能少点就少点）
4. 有些正在开发库都不支持2.7的版本，例如ipython，jupyter notebook等

**3.5+版本**

优点：

1. 默认编码是‘utf8’，对中文支持更加友好，在文本处理更加有优势
2. 优化计算，减少运行时占用的内存
3. 修改，增加，删除了一些语法，更加具有可读性，尽管python2的版本可读性也很好
4. python3.5+版本现在成为开发的主流， 毕竟3+的版本都出现6年了

缺点：

1. 有些库没有从2.7的版本迁移到3.5的版本
2. 2.7的语法和3.5+的语法有不同。

<*大家想要学习，推荐大家学习3.5+的版本，更加主流，更加便捷*>

#### Linux环境

在Linux环境下，有原生的python，可能版本有点低，不推荐用CentOS，这个python版本升级在环境配置中会很麻烦。ubuntu还是可以的。

**ubuntu**

系统自带2.7的版本，有些有3.5+的版本。

~~~shell
sudo  apt-get install  python3.6
sudo  apt-get install  python-pip
~~~



#### windows环境

系统自带中，没有python，需要自己安装。

##### 方式一：通过Anaconda进行安装

[ananconda官网](https://www.continuum.io/downloads)

![Anaconda官网图片](./picture/Anaconda官网图片.jpg)

自己选择自己需要下载的版本，文件格式时‘.exe’，可以直接进行安装。

安装完成得到下图，介绍主要用到的4个程序（红箭头表示的）

![ananconda介绍](C:\Users\Dxx\Desktop\文档图片\ananconda介绍.png)

###### Anaconda Prompt

​	这个表示的是Ananconda上的一个扩展库管理，在这里你可以通过命令行查看或者安装扩展库

​	打开这个，得到命令行界面，自带的包管理器conda，还是很强大的，输入“conda list”可以看见Ananconda下安装的所有扩展库以及库的版本。

![anaconda库控制](./picture/anaconda库控制.png)

​	当然，你也可以通过输入"conda install  库名 "的方式来安装自己想要安装的库。

详细的可以查看conda的文档 [文档地址](https://conda.io/docs/index.html)，[中文介绍](https://zhuanlan.zhihu.com/p/22678445)

不过在原生的Anaconda上的库基本上可以满足我们平时的需求了。

###### IPython

​	python的神器之一，结果实时输出，代码补全提示。

![ipython显示](./picture/ipython显示.png)

​	结果的直接输出，‘Tab’键会有代码提示，很便捷。

​	在ipython配置其他库使用时会让你感觉很舒适。

###### Jupyter Notebook

​	IPython的升级版，这里你可以出图，出表，也可以写markdow。也可以写很长的代码，基本上可以满足你的想象。这个是基于默认浏览器来进行展示的，建议默认浏览器不要设置为IE，不然会很尴尬。

​	利用Notebook画图：

​	![notebook画图](./picture/notebook画图.png)

​	利用Notebook写markdown：

    ![notebook的markdown](./picture/notebook的markdown.png)

​	还有很多便捷的功能，大家可以自行Google。

###### Spyder

​	anaconda的IDE，类似matlab的风格。

![spyder实例](http://img.blog.csdn.net/20161028204657734)

##### 方式二：通过官网下载自己安装和配置环境

###### python安装与配置环境变量

​	通过官网下载，[官网地址](https://www.python.org/downloads/)

​	自己选择一个版本进行下载，windows会自动下载exe文件，可以进行安装。（请记住安装地址，后面要用，推荐在系统盘）

![python版本](./picture/python版本.png)

​	安装完成后，在windows的cmd中，输入python，是无法运行的，你需要将python配置到你的环境变量上。

配置环境变量步骤：

1. 找到系统，我的电脑中。就是查看系统信息中就可以了
2. 找到高级系统设置，点击进去。看见了系统属性
3. 右下交，看见环境变量，点击进去。
4. 在环境变量中，在系统变量中，选择‘Path’，选择编辑。
5. 在编辑环境变量中，点击新建，在新地方选择python的安装地址。
6. 点击确定，在cmd中输入‘python’进行确认

![环境变量python展示](./picture/环境变量python展示.png)

​	安装好python之后，我们在需要安装的是python的扩展包管理，python强大，有一定的原因在于，她拥有很多很强大的扩展包（在后面会提到）。在Anaconda中，他是通过conda来进行包管理，但是conda，不能装，他是在Ananconda上的。

​	扩展包管理，这里演示主流的pip工具。在Linux环境下，python的扩展包，都是通过pip来进行管理，同时，她也是python的必备扩展包之一。

###### pip在windows安装

​	[pip官网](https://pypi.python.org/pypi/pip),[pip文档安装](https://pip.pypa.io/en/stable/installing/)

![pip官网截屏](./picture/pip官网截屏.png)

下载“pip-9.0.1 tar.gz”，pip好像对python的各个版面都支持，不用担心下错。

下载完成，进行解压。（推荐将解压完的文件夹移到系统盘中）	

![pip文件夹内容](./picture/pip文件夹内容.png)

在文件夹中，存在“setup”文件，格式还是‘Python File’。

通过 cmd，命令行进入到这个文件夹内，执行 ‘python setup.py install’ 

![安装pip](./picture/安装pip.png)

验证 可以通过输入“pip list“来查看，到底安装了哪些扩展库。

![pip验证和查看安装库](./picture/pip验证和查看安装库.png)

~~~shell
pip install 库名   #安装包
pip uninstall 库名 #卸载包
pip install --upgrade  库名 #更新包
~~~

推荐安装的扩展包，numpy，pandas，scipy，jupyter-notebook，matplotlib，tensorflow，sklearn等

### Pycharm的配置与使用

​	Pycharm，python现在普遍使用的集成环境，也是现在写大段python代码的主要使用工具。用于写python文件和测试代码。

​	[pycharm官网](http://www.jetbrains.com/pycharm/)

​	自己选择想要的版本，推荐用社区版，都有试用期，不用担心。（怎样激活，这里不写，自行百度）

​	下载直接可以打开，进行安装，在安装时，选择自己对应系统（可以都选择，仅仅自己写代码没有什么影响）

![pycharm安装选择](./picture/pycharm安装选择.png)

在安装后，创建新新项目时，需要选择python版本。

![pycharm选择python版本](./picture/pycharm选择python版本.png)

后面的操作和IDEA就很相识了，但是这里不是通过Maven来配置环境。一些扩展库，环境的安装都是通过上面的pip来进行安装，在你选择的python中，有这些环境，就能稳定运行，没有那就没有办法了。

在这里也有代码提示，Ctrl+Space快捷键来启动拼写提示功能，和ipython的’Tab‘键不同。

### python基本语法


#### 数据标准类型／Scalar Types

检查数据类型： type(variable)

##### 六种常用的数据类型

1. int/long，like java，

2. float -64位，没有‘double’类型

3. bool-True or False，布尔性

4. str-‘1’，“2”，‘“3”’，三种引号都行。有没有感觉很强大

   字符串位字符序列，可以当作其他序列

   字符串格式化有多种方式

5. NoneType(None) 数据为空，但是是实例，但是这样的实例只能有一个。这个用的比较少。我第一次看见。

6. datetime -有三种，‘datetime’，‘date’，‘time’，三种。可以相互转化，时间格式上，可以进行计算（加，减）。

注意: str(),bool(),int(),float(),是存在直接转换的函数的（explicit type）

​	除了“字符串”(strings)和“元组”(tuples)之外，Python中的大多数对象都是可变的	

#### 数据结构／Data Structures

##### 元组／Tuple

支持任何python数据类型，包含一个维度，同时是不可变的。

~~~python
tup1=4,5,6   #创建一个元组
tup1=(6,7,8) #创建一个元组第二个方法
tup2=(4,5,6),(7,8) #创建一个嵌套元组
tupel=([1,0,2])#序列转换为元组
tup1+tup2#连接元组
~~~

##### 列表／List

一个维度、可变长度、可变的任何类型的Python对象序列。

~~~python
list1=[1,'a',3.44]#创建一个列表
list2=list(tup1)#创建一个列表
list1+list2 #列表相加
list1.append('B')#增加‘B’
list1.insert(1,'B') #插入，在‘1’后面
list1.remove('a')#移除‘a’
list1.sort() #排序
~~~

还有很多，这些是基础用法。‘insert’比起‘append’，插入需要更多的计算。推荐用‘append’

列表在数据计算上很常见。转换成行列式更加便捷（纯数字）

##### 字典／Dict

以‘key‘：’value‘存在的，结果输出时，这个比较常见。

~~~python
dict={'key1':'value1',2:[3,2]} #创建一个字典
dict1['key1'] = 'newValue'#替换
del dict1['key1']#删除
dict1.keys()# 查看所有key
dict1.values()#查看所有 values
~~~

Python中主要使用的就是这三种，当然还有一些其他的，详情《Python学习手册》
#### 条件，循环介绍

##### 条件判断

在条件判断中，还是“if”，可能在写判断上有不同，但是格式都差不多

~~~python
a=2
if a>3:
    print 'fdff'
elif a==0:
    print 'a=0'
else :
    print 'dscsv'
~~~

##### 循环

循环还是和java都差不多，while和for。

~~~python
x=1
while x<100:
    print x
    x +=1 #可以换成 ‘x=x+1’
~~~

~~~python
for i in range(1,10): ##类似java for(int i=0;i<10,i++)
  print i 
~~~

“break”，“continue”在这里依旧可以使用。



基础知识[Python Cheat Sheet](http://datasciencefree.com/python.pdf)     
在共享上，电子书目录下上传了，《简明Python教程》这是python入门级的电子书     
还有《Python学习手册（第四版）》，这是很详细介绍Python的，大家有兴趣可以看看，了解。      
