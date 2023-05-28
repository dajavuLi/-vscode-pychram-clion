
**在编程开发时遇到了一些棘手的问题：如何高效搭建开发环境、如何快速解决奇奇怪怪的的报错信息等等**

**为了避免自己再次走弯路和掉进坑里，也希望能够帮助到有缘人，所以将这些操作尽可能详细的记录下来**

**在不同的版本环境操作细节也许有别，如果按照笔记的方法操作未能通过，请您理解，更不要钻入牛角尖**


**[文档目录](#jump1)** 

- [ ] 开发故障汇总[避坑指南]
- [ ] 基于 CLion 和 CubeMx 的STM32开发
- [X] 基于 KEIL 和 CubeMx 的STM32开发
- [x] 基于 VScode 的C程序开发
- [x] 基于 Pychram 的python程序开发

&emsp;

![Open In Colab](https://img.shields.io/badge/update-2023.05.27-green.svg)
---
#### <a id="jump1"> [开发故障汇总[避坑指南]](https://note.youdao.com/s/Ia47aSut)</a>
- 记录 CLion C程序开发时遇到的故障
- 记录 CLion\CubeMx\OpenOCD\Jlink-OB STM32项目开发时遇到的故障
- 记录 Keil\CubeMx\Jlink-OB\USB转TTL STM32项目开发时遇到的故障
- 记录 VScode C程序开发时遇到的故障

&emsp;
---
#### [基于CLion和CubeMx的STM32开发](https://note.youdao.com/s/OiOrOPUA)
- 笔记中记录了搭建开发环境所需软件的破解和一些重要设置
- 笔记中详细的介绍了开发STM32F103项目时 CubeMx的具体配置
- 笔记中详细的介绍了开发STM32F103项目时 CLion 的具体配置
- 笔记中详细的介绍了开发STM32F103项目时OpenOCD的具体配置
&emsp;
---
#### [基于KEIL和CubeMx的STM32开发](https://note.youdao.com/s/OiOrOPUA)
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

1.[STM32CubeMX](https://www.st.com/zh/development-tools/stm32cubemx.html#get-software) [ST公司提供的自动化配置和生成代码工具]
2.[Clion](https://pan.baidu.com/s/1pZKVNuuSGjd25cT76oO70A?pwd=k04e) [提取码:k04e][需要破解]
3.[MinGW](https://sourceforge.net/projects/mingw-w64/files/mingw-w64/mingw-w64-release/mingw-w64-v11.0.0.tar.bz2/download) [用来提供编译环境]
4.[OpenOCD](https://sourceforge.net/projects/openocd/postdownload) [用来下载仿真]
5.[arm-none-eabi-gcc](https://developer.arm.com/downloads/-/gnu-rm) [用来提供嵌入式调试环境]
6.[Java jre](https://www.azul.com/downloads/?package=jdk#zulu) [STM32CubeMx的依赖环境]







