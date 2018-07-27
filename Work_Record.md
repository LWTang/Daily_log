---


---

<h2 id="section">2018.7.16</h2>
<h3 id="git步骤">git步骤</h3>
<ul>
<li>远端建仓库</li>
<li>本地写代码、本地add、commit</li>
<li>push到远端（远端有readme.md的时候要先用 git pull --rebase origin master 来合并）</li>
</ul>
<h3 id="多人人脸识别">200多人人脸识别</h3>
<ul>
<li>完成200多人规模的人脸识别</li>
<li>将每个人的人脸特征向量单独存储，以节省每次识别的时间</li>
<li>numpy.narray的存储和加载</li>
</ul>
<h3 id="后续">后续</h3>
<ul>
<li>更大规模的识别</li>
<li>dlib人脸检测速度很慢，实时的效果看怎么样，不行的话换成opencv来做人脸检测</li>
</ul>
<h2 id="section-1">2018.7.17</h2>
<h3 id="读论文“核主成分分析网络人脸识别”">读论文“核主成分分析网络人脸识别”</h3>
<ul>
<li>结合CNN和哈希直方图</li>
</ul>
<h3 id="人规模">400人规模</h3>
<ul>
<li>单张识别结果比较好</li>
<li>配置了pyqt5和qtdesigner</li>
<li>写了篇博客(⊙o⊙)…</li>
</ul>
<h2 id="section-2">2018.7.18</h2>
<h3 id="完成目前现有功能的ui">完成目前现有功能的UI</h3>
<ul>
<li>pyqt打开文件对话框</li>
<li>识别的速度实在是慢，后面换opencv检测人脸</li>
<li>在github push项目出错，原因是在github.com改了之后没有merge，要先pull，再push，成功解决</li>
</ul>
<h2 id="section-3">2018.7.19</h2>
<h3 id="git删除远程库文件">git删除远程库文件</h3>
<ul>
<li>git rm filename、commit、push</li>
<li>github上显示表格的时候要在表格前面空一行</li>
</ul>
<h3 id="人脸检测换成opencv">人脸检测换成opencv</h3>
<ul>
<li>对比两种方法的速度，使用两张测试人脸对两种方法多次实验</li>
<li>test.jpg</li>
</ul>

<table>
<thead>
<tr>
<th><em>test.jpg</em></th>
<th><strong>opencv</strong></th>
<th><strong>dlib</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>人脸检测耗时(s)</strong></td>
<td>1.27</td>
<td>10.09</td>
</tr>
<tr>
<td><strong>人脸识别总耗时(s)</strong></td>
<td>3.71</td>
<td>12.47</td>
</tr>
</tbody>
</table><ul>
<li>tlw.jpg</li>
</ul>

<table>
<thead>
<tr>
<th><em>tlw.jpg</em></th>
<th><strong>opencv</strong></th>
<th><strong>dlib</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>人脸检测耗时(s)</strong></td>
<td>1.48</td>
<td>9.95</td>
</tr>
<tr>
<td><strong>人脸识别总耗时(s)</strong></td>
<td>3.92</td>
<td>12.37</td>
</tr>
</tbody>
</table><ul>
<li>学习看python官方文档</li>
<li>把opencv检测并入UI界面中</li>
<li>装deepin</li>
</ul>
<h2 id="section-4">2018.7.20</h2>
<h3 id="人脸识别收尾">人脸识别收尾</h3>
<ul>
<li>debug，解决没有人脸的情况</li>
<li>写了一篇博客总结(⊙o⊙)…</li>
</ul>
<h3 id="人脸检索最终目标">人脸检索最终目标</h3>
<ul>
<li>千万人中检索出一个人，训练集只有一张登记照</li>
</ul>
<h3 id="后续-1">后续</h3>
<ul>
<li>要开始股票数据的挖掘了sad(┭┮﹏┭┮)</li>
</ul>
<h2 id="section-5">2018.7.23</h2>
<h3 id="装mysql、vs2017">装MySQL、VS2017</h3>
<ul>
<li>把MySQL工具装全，VS2017安装不支持mfc</li>
<li>股票界面UI，熟悉米筐API</li>
<li>单继承中，super()主要用来调用父类的方法</li>
<li>信号：点击事件产生。 槽：响应的函数。</li>
</ul>
<h2 id="section-6">2018.7.24</h2>
<h3 id="股票界面设计">股票界面设计</h3>
<h2 id="section-7">2018.7.25</h2>
<h3 id="股票">股票</h3>
<ul>
<li>修改股票UI方案</li>
<li>写功能说明文档</li>
<li>勤学似春起之苗，不见其增，而日有所长</li>
</ul>
<h2 id="section-8">2018.7.27</h2>
<h3 id="git远程和本地同步">git远程和本地同步</h3>
<p>1.远程建仓库，本地建仓库,本地初始化：<code>git init</code><br>
2. (在新的电脑上:<code>ssh-keygen -t rsa -C "1770723422@qq.com"</code>在用户主目录生成公钥和私钥，将公钥添加到账户的ssh key)<br>
3. 将远程和本地库关联起来：<code>git remote add origin git@github.com:LWTang/PyQt-learn.git</code><br>
4. 将远程库pull到本地：<code>git pull origin master</code><br>
5. 开始表演(⊙o⊙)…</p>

