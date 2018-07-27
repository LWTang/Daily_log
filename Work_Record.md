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

## 2018.7.23
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
2. (在新的电脑上:```ssh-keygen -t rsa -C "1770723422@qq.com"```在用户主目录生成公钥和私钥，将公钥添加到账户的ssh key；设置提交的信息：```git config --global user.email 1770723422@qq.com```和```git config --global user.name LWTang```)
3. 将远程和本地库关联起来：```git remote add origin git@github.com:LWTang/PyQt-learn.git```
4. 将远程库pull到本地：```git pull origin master```
5. 开始表演(⊙o⊙)…