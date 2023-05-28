**在编程开发时遇到了一些棘手的问题：如何高效搭建开发环境、如何快速解决奇奇怪怪的的报错信息等等**

**为了避免自己再次走弯路和掉进坑里，也希望能够帮助到有缘人，所以将这些操作尽可能详细的记录下来**

**在不同的版本环境操作细节也许有别，如果按照笔记的方法操作未能通过，请您理解，更不要钻入牛角尖**
![Github](https://img.shields.io/badge/更新日期23.5.27-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
**[文档目录](#jump1)** 

- [ ] 开发避坑指南
- [ ] 基于CLion和CubeMx 的STM32开发
- [X] 基于CubeMx和KEIL的STM32开发
- [x] 基于VScode的C程序开发
- [x] 基于Pychram的python程序开发
 

![Open In Colab](https://img.shields.io/badge/version-2023.05.27-green.svg)

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




