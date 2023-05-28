
**在编程开发时遇到了一些棘手的问题：如何高效搭建开发环境、如何快速解决奇奇怪怪的的报错信息等等**

**为了避免自己再次走弯路和掉进坑里，也希望能够帮助到有缘人，所以将这些操作尽可能详细的记录下来**

**在不同的版本环境操作细节也许有别，如果按照笔记的方法操作未能通过，请您理解，更不要钻入牛角尖**


**[文档目录](#jump1)** 

- [ ] 开发避坑指南
- [ ] 基于CLion和CubeMx 的STM32开发
- [X] 基于CubeMx和KEIL的STM32开发
- [x] 基于VScode的C程序开发
- [x] 基于Pychram的python程序开发

&emsp;

![Open In Colab](https://img.shields.io/badge/update-2023.05.27-green.svg)
---
#### <a id="jump1"> [开发避坑指南](https://note.youdao.com/s/Ia47aSut)</a>
- 这篇笔记列出了笔者在进行开发时的踩过的坑

&emsp;
---
#### [基于CLion 和 CubeMx 的STM32开发](https://note.youdao.com/s/OiOrOPUA)
<details><summary>首先要确保在windows下搭建好这些环境</summary>
 <p>

  - [STM32CubeMX](https://www.st.com/zh/development-tools/stm32cubemx.html#get-software)   (用来自动化配置和生成代码)
  
 - [Clion](https://pan.baidu.com/s/1pZKVNuuSGjd25cT76oO70A?pwd=k04e)   [提取码：k04e]
  
 - [MinGW](https://sourceforge.net/projects/mingw-w64/files/mingw-w64/mingw-w64-release/mingw-w64-v11.0.0.tar.bz2/download)
  
 - [OpenOCD](https://sourceforge.net/projects/openocd/postdownload)     (用来下载仿真)
  
 - [arm-none-eabi-gcc](https://developer.arm.com/downloads/-/gnu-rm)    （用来提供交叉编译）
  
 - [Java jre](https://www.azul.com/downloads/?package=jdk#zulu)    (用来给STM32CubeMX提供Java环境)
 </p>
 </details>
 
- 这篇笔记对于上述开发环境
- 在这篇笔记中详细的介绍了针对 STM32 开发的 CLion 的配


&emsp;
---
#### [基于CubeMx 和 KEIL 的STM32开发](https://note.youdao.com/s/OiOrOPUA)
- 在这篇笔记介绍了如何使用CubeMx构建基于KEIL的STM32工程
- 在这篇笔记中也介绍了笔者对于调整工程文件夹结构的一些浅薄理解和操作
- 在这篇笔记中也介绍了keil的魔法棒详细配置
- 在这篇笔记中也介绍如何使用Jlink-OB和USB转TTL串口进行程序的下载和调试
- 里边有我找到两个很不错的构建视频，看起来很直观。 

&emsp;
---
#### [基于VScode的c程序开发](https://note.youdao.com/s/CisHoFe)

- 在这篇笔记中详细的介绍了单文件程序开发，例如：运行一个“hello world”程序
- 在这篇笔记中详细的介绍了多文件程序开发，例如：构造一个学生信息管理系统
- 多文件程序通常指包含多个头文件和源文件，他们彼此之间互相调用和依赖
- 在这篇笔记中也介绍了 vscode 终端打印乱码等常见故障的排除方法
- 看完这篇笔记你不会再有如何搭建一个C语言开发环境的困惑
- 搭建环境只是开始，等待你的将是优雅的界面和迷人的C世界 


&emsp;
---
#### [基于Pychram的python程序开发](https://note.youdao.com/s/QRXR7oEg)

-在这篇笔记中详细介绍了 anaconda、opencv、pycharm 的详细安装\激活
-在这篇笔记中也介绍了 pip 的快速加载、jupyter notebook 的简单操作









