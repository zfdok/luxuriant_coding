> 注意: 本文只适合 **windows7 64位系统** 
>
> 如果您是`windows10` / `windows11`系统: 请看这篇 : [Python安装指南(windows10/11版)]( https://xbtx666.cn/33)
>
> 如果您是`苹果Mac OS`系统: 请查看这篇 : 
>
> 如果您是`windows XP系统`,  这个系统实在是太旧了, 无法提供良好的编程学习环境了, 建议您先升级到较新的`win10/win11系统` 
>
> 如果您是`win7 32位系统`,  这个系统实在是太旧了, 无法提供良好的编程学习环境了, 建议您先升级到较新的`win10/win11系统 `

# 一. 如何查看自己的win7系统是64位还是32位?

在桌面上找到`计算机`图标, 在图标上右键弹出菜单, 选择`属性`

![](https://img.xbtx666.cn/blogs/image-20220210104701777.png)

在弹出的系统属性中, 我们可以看到系统类型

![](https://img.xbtx666.cn/blogs/image-20220210104818760.png)

如果您发现自己的系统是64位的, 就可以继续往下进行安装, 如果您的系统是32位的(x86), 推荐您先升级到win10系统, 再进行安装

# 二. win7的python版本问题

**注意: ** 即使是最新的win7 64位系统, 也已无法使用最新的python版本了, 只能使用python 3.8版本, 目前看来还没有太大问题, 但还是建议您升级到较新的`win10/win11系统 `

# 三. 下载python安装包

请使用百度网盘下载链接

👇👇👇👇👇

链接：https://pan.baidu.com/s/1ePTOww-U_7uKRlqWA55CKg?pwd=xbtx 
提取码：xbtx

下载完成后建议拖到桌面上, 方便找到

# 二. 安装python

### 1. 找到安装包位置

![](https://img.xbtx666.cn/blogs/image-20220210111450381.png)

### 2. 安装包安装

在安装包上右键, 选择 `以管理员身份运行`

![image-20220210111523564](https://img.xbtx666.cn/blogs/image-20220210111523564.png)

如果弹出提示框, 点击`是`

![image-20220210111723304](https://img.xbtx666.cn/blogs/image-20220210111723304.png)



> 如果出现下面的错误, 证明您的系统缺少补丁, 请献给系统打好补丁再进行安装, 方法见文末问题解答![image-20220210112434193](https://img.xbtx666.cn/blogs/image-20220210112434193.png)

先点击 `Add Python 3.xx to PATH`, 再点击`Install Now`

![image-20220126103611813](https://img.xbtx666.cn/blogs/image-20220126103611813.png)

### 3. 等待安装完成

等待安装完成, 直至出现`Setup was successful`

![image-20220126103832942](https://img.xbtx666.cn/blogs/image-20220126103832942.png)



![](https://img.xbtx666.cn/blogs/image-20220209123233670.png)

点击`Disable path length limit`再点击`Close`关闭安装窗口

# 后续步骤

### 1. 删除安装包

点击桌面上的安装包删除即可

### 2. 验证安装是否成功(可选)

1. 使用 `{win}` + `{R}` 键弹出运行框  (win按键就是键盘上的画着窗户的按键)

   ![image-20220127091350792](https://img.xbtx666.cn/blogs/image-20220127091350792.png)

2. 输入`cmd`, 然后回车, 会进入windows终端

   ![image-20220127091500261](https://img.xbtx666.cn/blogs/image-20220127091500261.png)

3. 在终端中输入`python --version`, 如果显示python相关版本信息, 则证明python安装成功

   ![image-20220127140311040](https://img.xbtx666.cn/blogs/image-20220127140311040.png)

4. 验证PIP(python包管理工具), 在终端中输入`pip --version`, 如果显示pip相关版本信息, 则证明PIP安装成功

   ![image-20220127092544811](https://img.xbtx666.cn/blogs/image-20220127092544811.png)

# 常见问题

### 1. 安装时出现下述问题:

![](https://img.xbtx666.cn/blogs/image-20220210112633532.png)

这是因为您的系统缺少win7 sp1补丁, 请下载此补丁并安装.

下载地址: 

下载完成后, 找到windows6.1-KB976932-X64.exe, 右键弹出菜单, 点击以管理员身份运行

![image-20220210115210837](https://img.xbtx666.cn/blogs/image-20220210115210837.png)

选择`是`

![image-20220210115341997](https://img.xbtx666.cn/blogs/image-20220210115341997.png)

选择 `下一步`

![image-20220210115428159](https://img.xbtx666.cn/blogs/image-20220210115428159.png)

点击 `安装`

![image-20220210115506558](https://img.xbtx666.cn/blogs/image-20220210115506558.png)

系统会自动安装

![image-20220210115814798](https://img.xbtx666.cn/blogs/image-20220210115814798.png)

如果提示安装不成功, 就重启后安装

![image-20220210115541730](https://img.xbtx666.cn/blogs/image-20220210115541730.png)

安装完成后, 就可以继续安装python了

# 帮助

> - 如果python官网改版或安装方式改变, 请在下方留言, 我会更新此文章
> - 如果您安装中出现任何问题, 请在下方留言
> - 此教程不适合**windows XP或win7 32位**操作系统
> - 如果百度网盘链接失效, 请在下方留言