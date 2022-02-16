嗨! 同学们大家好, 我是你们的python老师熊爸天下.

![image-20220215131605138](https://img.xbtx666.cn/blogs/image-20220215131605138.png)

通过不断的学习, 同学们已经有了 一定的python基础了, 也学会如何使用各种库和模块了, 是不是感觉自己有些无所不能了呢? 那是当然的了! 

![](https://img.xbtx666.cn/blogs/20191113173153VUWJDSGA897VX4P3_m_mc.gif)

请记住:  **Python已经不再是单纯的一门计算机编程语言了，现在它是一个无所不能的工具，我们可以使用Python让一些复杂的事情，变得简单**。

学习完python基础之后, 我们可以做的事数不胜数, 比如*Web开发；数据科学研究；网络爬虫；智能硬件开发；游戏开发；桌面应用开发* 等等

![](https://img.xbtx666.cn/blogs/image-20220215151636160.png)

现在, 我们就来开始学习一个船新的系列, 船新的python分支 -- 智能硬件, 

这是一个庞大的分支, 里面充满了各种知识和创意, 可谓是"其乐无穷". 现在我们从认识软/硬件开始.

# 一. 什么叫硬件?

### 1. 硬件和软件

**硬件:** 就是由电子，机械和光电元件等组成的各种物理装置的总称。这些物理装置按系统结构的要求构成一个有机整体为软件运行提供物质基础。

我们可以这样理解, 平时用的电脑就是硬件

![](https://img.xbtx666.cn/blogs/image-20220215132938774.png)

**软件:** 运行在硬件的基础上实现专用的功能的各种程序, 一般被划分为系统软件、应用软件等等...

在电脑上的程序就是各种软件, 像windows, 我们平时叫它操作系统, 但说白了, 操作系统也是个软件



**总结**

- 硬件就是电脑本体

- 软件就是运行在电脑上的看得见摸不着的程序 

硬件就像人的身体, 软件就像人的灵魂, 他们两者是和谐统一的存在的

如果没有了硬件, 你就变成了👇

![](https://img.xbtx666.cn/blogs/image-20220215134409660.png)

如果没有了软件, 你就变成了👇

![](https://img.xbtx666.cn/blogs/image-20220215134353408.png)

### 2. 硬件并不单指计算机硬件

所谓的硬件, 是一个很大的概念, 可不仅仅是计算机上的各种硬件, 我们在日常生活中一定见过下面的这些硬件

![](https://img.xbtx666.cn/blogs/image-20220215135658510.png)

![](https://img.xbtx666.cn/blogs/image-20220215135733331.png)

其实还有: 

![image-20220215135842171](https://img.xbtx666.cn/blogs/image-20220215135842171.png)

![](https://img.xbtx666.cn/blogs/image-20220215140000319.png)

![](https://img.xbtx666.cn/blogs/image-20220215140107475.png)



![](https://img.xbtx666.cn/blogs/image-20220215140443580.png)

这些硬件, 有的非常简单, 只能实现单一的功能, 或者特定的用途, 有些则运行着操作系统, 可以安装软件, 实现意想不到的功能, 关于硬件的分类在此我们不做过多的描述, 我们只需要知道, 

> 硬件不仅仅是指计算机硬件, 我们的python也不仅仅只能运行在计算机上 

![惊不惊喜](https://img.xbtx666.cn/blogs/20190909175137Y90EXBMS77AGUFNQ_m_mc.gif)

# 三. 我们的硬件主角: ESP32

ESP32是乐鑫信息科技(以下简称乐鑫)推出的一款主控芯片。性能强悍，物美价廉,  深受全球电子爱好者的好评! 而且是我国自助研发的芯片 👍👍👍

ESP32的芯片自带WIFI和蓝牙模块，很适合做物联网通信类产品



ESP32开发板是一款基于 ESP32 模组的小型开发板，支持 Wi-Fi 和蓝牙功能。开发板具有丰富的外设，让用户可轻松实现产品开发.

![](https://img.xbtx666.cn/blogs/image-20220215142912240.png)

ESP32是系列化的产品, 我们现在不需要关心各个产品间的区别, 只要是ESP32系列就可以



# 四. 我们的软件主角: MircoPython

### 1. 什么是MicroPython?

MicroPython 是python迷你版, 是一个可以运行在 **微处理器**上的 **Python解释器**，

通过上面的介绍, 我们已经认识了硬件主角ESP32, 看看ESP32那小巧的身材, 它的运算能力肯定是不如我们使用的计算机那么强大的, 所以**原版的python是无法运行在这么小的设备上的**

![力速双A](https://img.xbtx666.cn/blogs/lisushuangA.png)

使用迷你版的`MicroPython `需要的硬件资源比原版python小的多, 而且它还做了对针对性的硬件支持, 支持我们使用**Python脚本**来控制硬件



现在让我们给硬件烧录好MicroPython, 体会一下使用Python去控制硬件的乐趣吧

# 五. 在ESP32上安装MircoPython

现在大家一起来学习如何在ESP32上安装MircoPython吧!

### 1. 连接并驱动ESP32

1. 下载下述软件

   链接：https://pan.baidu.com/s/14IF3q9xfEWy_gb9tCSUR-g?pwd=xbtx 
   提取码：xbtx 

2. 安装驱动, 下载包中有CP2102和CH340两款驱动, 具体安装那一版和您的开发板USB串口芯片有关, 如果你不知道自己的ESP开发板是哪一款驱动, 就两个都安装上吧

   ![](https://img.xbtx666.cn/blogs/image-20220215160016449.png)

   

3. 现在, 我们用一根数据线将ESP32开发板连接在计算机的USB口上

4. 使用`{win}`+`R`键调出运行窗口, 输入`devmgmt.msc`并回车

![](https://img.xbtx666.cn/blogs/image-20220215152322577.png)

5. 在弹出的设备管理器中, 找到`端口`, 就能看到我们的ESP设备连上了电脑 这里设备的名字也是随着开发板USB串口芯片改变的, 可能是下面的任意一种情况

   ![](https://img.xbtx666.cn/blogs/image-20220215160438710.png)

![image-20220215160218712](https://img.xbtx666.cn/blogs/image-20220215160218712.png)

![image-20220215160633749](https://img.xbtx666.cn/blogs/image-20220215160633749.png)

> 在设备管理器中, 我们的设备会被分配一个COM口, 大家要记住这个COM口, 后面需要用
>
> ![](https://img.xbtx666.cn/blogs/image-20220215160747805.png)



6. 如果出现黄色叹号, 证明没安装好
7. ![image-20220215162124175](https://img.xbtx666.cn/blogs/image-20220215162124175.png)

6. 现在我们已经连接好了ESP32, 大家可以插拔几次ESP32开发板, 看看端口能不能识别设备

### 2. 安装uPyCraft

在上面下载的安装包里, 有一个uPyCraft程序, 我们把这个程序拖放在桌面上, 然后双击打开

如果出现下面的提示, 就点击OK

![image-20220215161319056](https://img.xbtx666.cn/blogs/image-20220215161319056.png)

此时弹出软件主界面

![](https://img.xbtx666.cn/blogs/image-20220215163013330.png)

### 3. 烧录固件

我们打开 菜单中的 Tools 选项, 再点击 `BurnFirmware`

![](https://img.xbtx666.cn/blogs/image-20220215163120261.png)

在弹出的界面中按下面的步骤选择

![](https://img.xbtx666.cn/blogs/image-20220215163334791.png)

然后软件会自动帮我们把MicroPython烧录到ESP32中

![](https://img.xbtx666.cn/blogs/image-20220215163644893.png)

烧录完成后, 我们点击 Tools 再点击 Serial 再选择你的COM口

![image-20220215163759082](https://img.xbtx666.cn/blogs/image-20220215163759082.png)

当一切完成后, 我们可以看到终端区出现了熟悉的 `>>>`

![](https://img.xbtx666.cn/blogs/image-20220215163904411.png)

至此, 我们的MicroPython安装完成了! 

### 4. 写个hello world试一试

现在我们输入个`hello world`试一试吧

![](https://img.xbtx666.cn/blogs/image-20220215164051315.png)

> 要注意!!! 这里的hello world 不是用电脑的 Python 打印出来的, 是用ESP32开发板中的MicroPython打印的

现在, MicroPython环境已经搭建完成了! 让我们开始真正的学习吧!

![](https://img.xbtx666.cn/blogs/20220215164940.gif)

