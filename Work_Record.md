# Work Record

## 2018.7.16

### git步骤

* 远端建仓库
* 本地写代码、本地add、commit
* push到远端（远端有readme.md的时候要先用 git pull --rebase origin master 来合并）

### 200多人人脸识别

* 完成200多人规模的人脸识别
* 将每个人的人脸特征向量单独存储，以节省每次识别的时间
* numpy.narray的存储和加载

### 后续

* 更大规模的识别
* dlib人脸检测速度很慢，实时的效果看怎么样，不行的话换成opencv来做人脸检测

## 2018.7.17

### 读论文“核主成分分析网络人脸识别”

* 结合CNN和哈希直方图

### 400人规模

* 单张识别结果比较好
* 配置了pyqt5和qtdesigner
* 写了篇博客(⊙o⊙)…

## 2018.7.18

### 完成目前现有功能的UI

* pyqt打开文件对话框
* 识别的速度实在是慢，后面换opencv检测人脸
* 在github push项目出错，原因是在github.com改了之后没有merge，要先pull，再push，成功解决

## 2018.7.19

### git删除远程库文件

* git rm filename、commit、push
* github上显示表格的时候要在表格前面空一行

### 人脸检测换成opencv

* 对比两种方法的速度，使用两张测试人脸对两种方法多次实验
* test.jpg

*test.jpg* | **opencv** | **dlib**
--- | --- | ---
**人脸检测耗时(s)** | 1.27 | 10.09
**人脸识别总耗时(s)** | 3.71 | 12.47

* tlw.jpg

*tlw.jpg* | **opencv** | **dlib**
--- | --- | ---
**人脸检测耗时(s)** | 1.48 | 9.95
**人脸识别总耗时(s)** | 3.92 | 12.37

* 学习看python官方文档
* 把opencv检测并入UI界面中
* 装deepin

## 2018.7.20

### 人脸识别收尾

* debug，解决没有人脸的情况
* 写了一篇博客总结(⊙o⊙)…

### 人脸检索最终目标

* 千万人中检索出一个人，训练集只有一张登记照

### 后续

* 要开始股票数据的挖掘了sad(┭┮﹏┭┮)

<h2 id="7-23">2018.7.23</h2>

### 装MySQL、VS2017

* 把MySQL工具装全，VS2017安装不支持mfc
* 股票界面UI，熟悉米筐API
* 单继承中，super()主要用来调用父类的方法
* 信号：点击事件产生。 槽：响应的函数。

## 2018.7.24

### 股票界面设计

## 2018.7.25

### 股票

* 修改股票UI方案
* 写功能说明文档
* 勤学似春起之苗，不见其增，而日有所长

## 2018.7.27

### git远程和本地同步

1. 远程建仓库，本地建仓库,本地初始化：```git init```
2. (在新的电脑上: `ssh-keygen -t rsa -C "1770723422@qq.com"`在用户主目录生成公钥和私钥，将公钥添加到账户的ssh key；设置提交的信息```git config --global user.email 1770723422@qq.com```和```git config --global user.name LWTang```)
3. 将远程和本地库关联起来：```git remote add origin git@github.com:LWTang/PyQt-learn.git```
4. 将远程库pull到本地：```git pull origin master```
5. 开始表演(⊙o⊙)…

## 2018.8.13

### 框架对比

名称 | 机构 | 支持语言 | 架构设计 | 性能 | stars | forks
--- | --- | --- | --- | --- | --- | ---
TensorFlow | Google | Python C++ Go Java | 优 | 优 | 63166 | 30639
Caffe | 加州大学伯克利分校 | Python C++ Matlab | 良 | 良 | 18948 | 11657
MXNet | 分布式机器学习社区 | DMLC Python C++ R Go Scala | 优 | 良 | 10338 | 3871
CNTK | Microsoft|  C++ Python | 中 | 优 | 11709 | 2968
Theano | 蒙特利尔大学 | Python | 中 | 中 | 6617 | 2198
Torch | Facebook | C Lua | 优 | 良 | 7079 | 2098
PaddlePaddle | 百度 | Python C++ | 良 | 良 | 5110 | 1397

## 2018.8.15

### 机器学习

* 机器学习：赋予计算机学习的本领，研究计算机怎样模拟和实现人类的学习行为。
* 传统的机器学习算法有[决策树]()、[聚类]()、[贝叶斯分类]()、[EM]()、[Adaboost]()等等；机器学习有三类模型：分类问题、回归问题、聚类问题。

### k-近邻算法(KNN)
1. 一个带有标签的样本数据集，其中每条数据包含与所属分类的对应关系
2. 输入没有标签的新数据后，将它的每个特征与数据集中的特征进行对比
	* 计算新数据与样本集中每条数据的距离
	* 按距离从小到大排序
	* 取前k个数据对应的分类标签
3. 将k个数据中出现次数最多的分类标签作为新数据的分类

### 读取.txt文件
1. fileObject = open('dir')
2. fileObject.readline():一行一行的读取

### python split()方法
通过指定分隔符对**字符串**进行分割，返回分割后的**字符串列表**
> str.split('str_cut', num)
* str_cut:分割字符，num:分割次数(默认全部分割)

## 2018.8.16

### numpy.tile()方法
```
a = np.array([0, 1, 2])
b = np.tile(a, 2) #沿x轴复制2倍
c = np.tile(a, (1, 2)) #沿x轴复制2倍，沿y轴复制1倍
d = np.tile(a, (2, 1, 2)) #沿x轴复制2倍，沿y轴复制1倍，沿z轴复制2倍
```
```
b = [0, 1, 2, 0, 1, 2]
c = [[0, 1, 2, 0, 1, 2]]
d = [ [[0, 1, 2, 0, 1, 2]],
	[[0, 1, 2, 0, 1, 2]] ]
```
### python字典
#### 基础
python字典键必须不可变，所以可以是数字、字符串、元组，而列表就不行；值可以取任何类型
* 删除字典元素：```del dict[key]```
* 清空字典：```dict.clear()```,清空后是一个空字典

#### dict.get()方法
dict.get(key, default=None)
```
key --- 字典中要查找的键
default --- 如果指定的键不存在，则返回default值;如果存在则返回对应键的value
```
#### dict.items()方法
以列表形式返回遍历的(键，值)元组数组
```
>>>dict = {1:'j', 'j':2}
>>>print(dict.items())
dict_items([(1, 'j'), ('j', 2)])
```

## 2018.8.17

### 向量维度
1. 向量维数是指一个向量中分量的个数，eg.(x, y, z)是一个3维向量
2. a[3]是一维数组；a\[2][5]是二维数组；a\[3]\[4][6]是三维数组

### numpy shape
```
>>> b = numpy.array([1])
>>> b.shape
(1,)
>>> b = numpy.array(1)
>>> b.shape
()
```

## 2018.8.20
* lintcode 两个题
* 一篇博客

## 2018.8.21
* github pages 搭建博客
* 一篇博客

## 2018.8.22
* 一篇博客
* SVM初步

## 2018.8.23
* 同级目录，调用时直接使用文件名
* 父级目录，加两个点调用：```../img.jpg```
* HTML 包括六个级别的标题,```<h1>-<h6>```
* html:段落文本、图片、6级标题、列表(有序列表```<ol>```，无序列表```<ul>```)
* 列表内的每个项目被包括在一个```<li>```元素里
* html链接：```<a href="https://github.com/LWTang">唐礼威的github</a>```(```href```是超文本引用hypertext reference)

## 2018.8.24
### 在html中包含特殊字符，见[这里](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Getting_started)：

原义字符  |  转义字符
-------  | -------
<  |  \&lt;
\>  |  \&gt;
"  |  \&quot;
'  |  \&apos;
&  |  \&amp;

## 2018.8.27
### 文档内超链接(html语法)：
<a href="#7-23">跳转至7-23</a>