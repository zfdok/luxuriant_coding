# 一. 认识uPyCraft

在上一篇中, 我们通过uPyCraft软件向ESP32开发板中烧录了MicroPython固件, 这让我们的ESP32变得非常强大

![力速双A](https://img.xbtx666.cn/blogs/lisushuangA.png)

事实上uPyCraft不仅仅是一个烧录工具, 它还是一个**MicroPython IDE**, 可以用来编写程序, 并在ESP32中执行, 那么现在, 我们先来熟悉一下uPyCraft的界面吧



### 1. 先来做几个设置

1. 设置配套开发板为ESP32

![](https://img.xbtx666.cn/blogs/image-20220216084327830.png)

2. 设置ESP32开发板连接的COM端口

   ![](https://img.xbtx666.cn/blogs/image-20220215163759082.png)

3. 设置工作区

   我们编写的文件可以存在电脑上, 也可以下载到ESP32上, 设置工作区的意思是设置文件在电脑上存储的位置

   设置方法: 点击界面中的 文件系统中的 workspace 会弹出窗口, 我们选择自己向存放文件的文件夹即可

   ![](https://img.xbtx666.cn/blogs/image-20220216100713077.png)

### 2. 熟悉uPyCraft界面

![](https://img.xbtx666.cn/blogs/image-20220215163013330.png)

##### (1). 文件系统

![](https://img.xbtx666.cn/blogs/image-20220216100348551.png)

##### (2). 编辑区

编辑器部分是编写代码和编辑*.py*文件的地方。我们可以打开多个文件，编辑器将为每个文件打开一个新选项卡。

##### (3). 终端

在 MicroPython Shell 上，可以用 ESP32 板互动模式, 立即执行命令，而无需上传新文件。

终端还提供有关执行程序状态的信息，显示与上传相关的错误、语法错误、打印消息等……

##### (4). 工具栏

![](https://img.xbtx666.cn/blogs/image-20220216103945458.png)

# 二. 使用交互模式

当开发板连接好后, 终端窗口中出现**>>>**。这和我们python中的交互模式是一样的. 我们随意键入代码,就会立即执行

比如我们上一节输入过的 hello world

```python
print("hello world!")
```

写代码段也是可以的

```python
for i in range(100):
	print(i)
```

![](https://img.xbtx666.cn/blogs/image-20220216104650704.png)

如果写了死循环, 请使用 `停止执行`按钮停止执行

# 三. 使用文件模式

文件模式会创建一个.py文件, 这个文件先会保存在电脑上的工作区中, 我们也可以下载保存到ESP32中并执行, 现在我们就来体验一下:

1. 点击 ![image-20220216105651481](https://img.xbtx666.cn/blogs/image-20220216105651481.png)`新建文件`创建新文件

2. 使用`{ctrl}`+`{S}`保存文件, 会弹出保存窗口, 输入一个你想用的名字, 别忘记.py后缀, 点击`OK`保存

   ![](https://img.xbtx666.cn/blogs/image-20220216105931814.png)

3. 现在我们在文件中随便写一点代码, 比如

```python
for i in range(100):
  print(i)
```

4. 写完记得用`{ctrl}`+`{S}`保存文件
5. 点击![](https://img.xbtx666.cn/blogs/image-20220216110551958.png)`执行`

![](https://img.xbtx666.cn/blogs/image-20220216110532286.png)

6. 为了方便下一节内容的观察, 我们稍微修改一下程序加个延时, 重写下载运行一下试一试

   我们再从`workSpace`中找到我们的文件, 

   ![](https://img.xbtx666.cn/blogs/image-20220216115228048.png)

   修改文件(复制下面内容即可, 我们现在不用关心这个文件怎么写的), 按上面的方法再下载到ESP32中并执行, 我们会发现ESP32板上小灯闪亮了

   ```python
   from machine import Pin
   import time
   
   led = Pin(2, Pin.OUT)
   
   while True:
     led.value(not led.value())
     time.sleep(1)
   ```

   如果想停止运行, 请点击![](https://img.xbtx666.cn/blogs/image-20220216113354711.png)`停止运行`

# 四. 如何让ESP开机就自动执行程序?

刚刚我们体验文件模式时, 发现ESP32文件中还有一个默认文件`boot.py`, 这是MicroPython的自带启动文件, 如果在这个文件中导入我们的文件, 文件就会在设备启动时自动执行

1.  打开boot.py文件, 导入我们的文件, 按`{ctrl}`+`{S}`保存

![](https://img.xbtx666.cn/blogs/image-20220216111839210.png)

2. 点击![](https://img.xbtx666.cn/blogs/image-20220216110551958.png)`执行`, 会把新的boot.py文件下载到设备中

   ![image-20220216112213731](https://img.xbtx666.cn/blogs/image-20220216112213731.png)

3. 我们把ESP开发板拔掉, 再从新插上发现小灯在闪, 证明我们的文件启动就自动执行了

> 注意: 此时, ESP32并没有连接我们的软件uPyCraft, 如果我们想连接, 请按如下操作, 连接后程序会自动停止执行
>
> ![](https://img.xbtx666.cn/blogs/image-20220215163759082.png)

# 五. 除了uPyCraft之外的其他的选择

除了uPyCraft之外, 我们还有很多种方法来编写MicroPython程序并下载到ESP32并执行, 下面做个简单的介绍

### 1. Thonny

熟悉树莓派的同学可以尝试

下载地址: https://thonny.org/

![image-20220216115912724](https://img.xbtx666.cn/blogs/image-20220216115912724.png)

### 2. esplorer

[https://esp8266.ru/esplorer/](https://esp8266.ru/esplorer/) (官方英文版)
[https://blog.csdn.net/jackhuang2015/article/details/77676598](https://blog.csdn.net/jackhuang2015/article/details/77676598)
[http://pan.baidu.com/s/1c1MI2UO](http://pan.baidu.com/s/1c1MI2UO) (中文版)

这个软件是java的 需要安装并配置JAVA 运行环境, 推荐有较高基础的同学使用

![](https://img.xbtx666.cn/blogs/16670204-4a4f7d0a56c611e6.png)
