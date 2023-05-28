**在编程开发时遇到了一些棘手的问题：如何高效搭建开发环境、如何快速解决奇奇怪怪的的报错信息等等**

**为了避免自己再次走弯路和掉进坑里，也希望能够帮助到有缘人，所以将这些操作尽可能详细的记录下来**

**在不同的版本环境操作细节也许有别，如果按照笔记的方法操作未能通过，请您理解，更不要钻入牛角尖**

![Open In Colab](https://img.shields.io/badge/update-2023.05.27-green.svg)

**[文档目录](#jump1)** 

- [ ] 开发避坑指南
- [ ] 基于CLion和CubeMx 的STM32开发
- [X] 基于CubeMx和KEIL的STM32开发
- [x] 基于VScode的C程序开发
- [x] 基于Pychram的python程序开发




&emsp;

#### <a id="jump1"> [开发避坑指南](https://note.youdao.com/s/Ia47aSut)</a>
- 这篇笔记列出了笔者在进行开发时的踩过的坑

&emsp;
---
#### [基于CLion 和 CubeMx 的STM32开发](https://note.youdao.com/s/OiOrOPUA)
- 这篇笔记介绍了在CLion中调试STM32单片机需要的环境
 <details><summary>在windows下需要安装如下软件：</summary>
 <p>
 STM32CubeMX   (用来自动化配置和生成代码)
  
 Clion    (笔记中给出了一些破解方法[仅供交流学习，切勿用作商业途径])
  
 MinGW    (用来给CLion中的工具链配置环境)
  
 OpenOCD     (用来下载仿真)
  
 arm-none-eabi-gcc    （用来提供交叉编译）
  
 Java jre    (用来给STM32CubeMX提供Java环境)
 </p>
 </details>

- 在这篇笔记中详细的介绍了针对 STM32 开发的 CLion 的配

&emsp;
---
#### [基于CubeMx 和 KEIL 的STM32开发](https://note.youdao.com/s/OiOrOPUA)
- 在这篇笔记介绍了如何使用CubeMx构建基于KEIL的STM32工程
  - 里边有我找到两个很不错的构建视频，看起来很直观。 
- 在这篇笔记中也介绍了笔者对于调整工程文件夹结构的一些浅薄理解和操作
- 在这篇笔记中也介绍了keil的魔法棒详细配置
- 在这篇笔记中也介绍如何使用Jlink-OB和USB转TTL串口进行程序的下载和调试

&emsp;
---
#### [基于vscode的c程序开发](https://note.youdao.com/s/CisHoFe)
- 在这篇笔记中详细的介绍了单文件程序开发，例如：运行一个“hello world”程序

- 在这篇笔记中详细的介绍了多文件程序开发，例如：构造一个学生信息管理系统
- 多文件程序通常指包含多个头文件和源文件，他们彼此之间互相调用和依赖
- 在这篇笔记中也介绍了 vscode 终端打印乱码等常见故障的排除方法
- 看完这篇笔记你不会再有如何搭建一个C语言开发环境的困惑
- 搭建环境只是开始，等待你的将是优雅的界面和迷人的C世界 

&emsp;
---
#### [基于Pychram的python程序开发](https://note.youdao.com/s/QRXR7oEg)
- 在这篇笔记中详细介绍了 anaconda、opencv、pycharm 的详细安装\激活
- 在这篇笔记中也介绍了 pip 的快速加载、jupyter notebook 的简单操作



# Dummy-Robot: Super compact smart robotic-arm
> **我的超迷你机械臂机器人项目。**
>
> 视频介绍：[【自制】我造了一台 钢 铁 侠 的 机 械 臂 ！【硬核】](https://www.bilibili.com/video/BV12341117rG)
>
> Video : [I made a DUMMY ROBOTIC ARM from scratch！ - YouTube](https://www.youtube.com/watch?v=F29vrvUwqS4)

![](5.Docs/1.Images/dummy1.jpg)

![](5.Docs/1.Images/case.png)





> 这是视频中原版机械臂的完整设计方案，该方案成本和制作难度都比较高，因此想复现的同学建议再等等我后面会发布的**Dummy青春版**，该版本会有如下改进：
>
> 1. 整机重新设计结构，改用3D打印作为制造方案（原版为铝CNC），大幅降低制造成本
> 2. 采用我自己设计的小型摆线针轮减速器替代原版的谐波减速器，大幅降低零件成本
> 3. 所有软件和固件和原版通用，功能也完全一致
> 4. 添加我自己设计的PC端上位机和手机端APP（争取把用户初始化设置引导加进去）
> 5. 改进原版电机驱动器的走线方式，原版电源走线采用焊接的形式，不便于安装和拆卸，后面的青春版会使用4p接插件（电源+CAN总线）连接
> 6. 整机成本争取做到2000以内
> 7. **最重要的，会找人出一个保姆级的视频教程！**



## 关于结构设计

我视频中原版设计使用的`步进电机`+Harmonic的`谐波减速模组`，其中后者成本较高（我买的二手大概是600元一个），因此为了能让大家尽量复现本项目，我后期会添加一个`自制摆线针轮减速器`+`3D打印`的低成本方案。

> 目前摆线减速器已经设计好了正在验证，预期会使用PC（或者亚克力）切割结合3D打印制作，精度有所下降但是功能都保持不变，整机硬件成本希望控制在2000元以内。

设计好的摆线减速器见我的另一个仓库：[peng-zhihui/CycloidAcuratorNano ](https://github.com/peng-zhihui/CycloidAcuratorNano)

![](5.Docs/1.Images/cycliod-nano.jpg)

## 关于电路模块

电路为了实现主要的机械臂运动控制功能其实核心就4块板子：

* REF核心板
* REF底板（也就是机械臂底座里面的控制器电路板）
* 步进电机驱动
* Peak示教器






