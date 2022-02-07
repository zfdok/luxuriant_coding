# 一. pip简介

**问**: 什么是pip?

**答**: pip可以理解为python的"应用商店", 在里面可以一键安装python的"应用程序"

![](https://img.xbtx666.cn/blogs/image-20220127163810346.png)

# 二. pip换源

**问**: pip为什么要换源?

**答: ** pip默认要去国外的网站下载, 下载速度比较慢, 好在国内有数个公用同步源, 我们可以把pip设置为国内源, 从而加快下载速度



### 1. 国内pip镜像

  阿里云 https://mirrors.aliyun.com/pypi/simple/ 

  中国科技大学 https://pypi.mirrors.ustc.edu.cn/simple/ 

  豆瓣(douban) https://pypi.douban.com/simple/ 

  清华大学 https://pypi.tuna.tsinghua.edu.cn/simple/ 

  中国科学技术大学 https://pypi.mirrors.ustc.edu.cn/simple/

### 2. windows下pip换源

①. 使用`{win}`+`{R}`键调用运行框, 输入`%HOMEPATH%`并回车 (win按键就是键盘上的)

![image-20220127160454444](https://img.xbtx666.cn/blogs/image-20220127160454444.png)

②. 进入文件夹后, 右键新建文件夹, 文件夹命名为`pip`

③. 进入`pip`文件夹, 在文件夹中空白处右键, 点击`通过code打开`, 如果是WIN11系统, 请`右键`->`显示更多选项`->`通过code打开`

![image-20220127161857546](https://img.xbtx666.cn/blogs/image-20220127161857546.png)

④. 打开VSCODE以后, 新建一个'pip.ini'的文件

![image-20220127162039057](https://img.xbtx666.cn/blogs/image-20220127162039057.png)



![image-20220127162120146](https://img.xbtx666.cn/blogs/image-20220127162120146.png)

⑤. 在文件中输入以下内容

```python
[global]
timeout = 6000
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
trusted-host = pypi.tuna.tsinghua.edu.cn
```

![image-20220127164502563](https://img.xbtx666.cn/blogs/image-20220127164502563.png)

⑥. 完成后按`{ctrl}`+`{S}`保存文件



至此, pip换源完成.

# 三. 后续步骤

### 1. 重新打开之前的学习文件夹(可选)

在上一篇 : [VsCode安装指南(windows版)](https://xbtx666.cn/34)文章中, 我们新建了一个同学们用来学习python的专用文件夹, 在`D盘`中, 我们找到并进入这个文件夹, 在文件夹中右键, 点击`使用code打开`, 如果是WIN11系统, 请`右键`->`显示更多选项`->`通过code打开`



# 辛苦了! 现在您的PIP换源完成
