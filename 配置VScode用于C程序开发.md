**完整版开发文档详见[有道云笔记](https://note.youdao.com/s/CisHoFe)**
##### GCC知识点详解：
*   ..  表示返回上一级目录		
    -o: 开启编译优化 
    -I: 添加头文件搜索路径		
    -g: 生成调试信息     		
*   gcc  main.c mystruct.c -o myprogram.exe   
    这行代码表示将 main.c文件、mystruct.c 文件编译成 'myprogram.exe' 可执行文件
*   gcc -g -I ..\include main.c mystruct.c -o ..\build\myprogram.exe   
    这行代码表示：生成一个可调试的 'myprogram.exe' 文件，生成后的可调试文件位于build文件夹，
    编译时的依赖文件有：include文件夹下的头文件，本目录下的源文件main.c、mystruct.c

##### GDB知识点详解
-   break 设置断点;     run 运行程序;    
    next 单步执行，不进入函数;    step 单步执行，进入函数
    continue 继续执行程序，直到下一个断点;      print 查看变量值;       backtrace 查看函数调用栈
-   例如：
    gdb myprogram.exe //加载可执行文件(myprogrm.exe)进行调试
    break main.c:9    //在main.c文件的第9行打上断点
    run               //启动加载的.exe文件，开始执行程序
    step              //进行单步调试
    q                 //即可结束调试。  

##### Makefile详解:
<!--Compiler settings--markdown注释--不会显示--> 
```makefile
.PHONY: all  # 可以理解为：告诉make工具，all是个伪目标，不用检查可执行文件是否存在，直接刷新生成。
```
```makefile
CC = gcc # CC变量被设置为gcc
         # <CompilerCollection用于指定编译器的名称或路径>
```

```makefile
CFLAGS = -Wall  -Werror  -g  -I include  -o     # CFLAGS变量用于指定编译选项
        # <这里的选项包括：开启警告、警告视错、生成调试信息、指定包含头文件的目录、指定输出文件的名称>
```  


```makefile
SRCS = src/main.c src/mystruct.c       ## SRCS= main.c  mystruct.c
        # <SRCS变量用于存储项目中的源代码文件列表>
```


```makefile
HDRS = include/mystruct.h    # HDRS = include\mystruct.h
        # <HDRS变量用于存储需要包含在编译过程中的头文件>
```


```makefile
OBJS = $(SRCS: .c=.o)        # OBJS = main.o mystruct.o
        # <$(SRCS:.c=.o)表示：将SRCS中的每个.c文件 替换成对应的目标文件.o>
```

```makefile
TARGET = myprogram.exe      # TARGET变量定义了最终生成的目标文件名为myprogram.exe
```

```makefile
all: $(TARGET)            # 执行make all命令时，all目标会生成 TARGET 指定的可执行文件
# all: $(TARGET) clean] ；  表示all目标先执行$(TARGET)子目标，然后执行clean子目标。这样写有个好处：make all时自动删掉.O文件。
```
>

```makefile
$(TARGET): $(OBJS)                      # 可执行文件由指定的目标文件链接生成
    $(CC)  $(CFLAGS)  $(TARGET)   $(OBJS)    # <由[CC变量指定的编译器]和[CFLAGS变量指定的编译选项] 提供规则>
 ```

```makefile
%.o: %.c $(HDRS)              # 目标文件由所有的.c文件编译生成，同时需要使用HDRS变量中的头文件作为依赖关系
    $(CC) $(CFLAGS) $@ -c $<  # <由[CC变量指定的编译器]和[CFLAGS变量指定的编译选项] 提供编译规则>
        # $@表示当前规则中的目标文件名；-c表示将源代码编译成目标文件；$< 表示当前需要编译的源代码文件
```

```makefile
clean:
    del /q $(OBJS)  # <在终端输入：make clean命令后,删除所有生成的目标文件
        # <可以保持项目的整洁和可维护性,不影响.exe可执行文件的调试>
```
