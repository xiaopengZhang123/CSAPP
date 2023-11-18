## 1-1

从最简单的的hello.c开始，我们可以使用gcc -o hello hello.c,分为四个阶段，预处理，编译，汇编，链接

1. 预处理(pre-processor)
预处理命令就是'#'包含的,包括有宏等,经过预处理,hello.c就变为了hello.i文件。\
移除注释。\
处理宏定义。\
处理条件编译指令（例如 #ifdef、#ifndef）。\
展开头文件（#include）
2. 编译(compiler)
hello.i文件经过编译之后会生成hello.s(汇编文件).

3. 汇编(assemble)
将上一步的hello.s编译为hello.o文件,这是一个可重定向的文件

4.链接(link)
将我们hello.c文件中的printf.o文件与hello.o文件合并,最终生成我们想要的结果

## 1-2
顺便回顾一下gcc命令选项,默认什么都不加的话是生成a.out
```shell
# 这个意思是我不想要叫做a.out名字的程序,我把这个起了个我想要的名字 myFile
gcc -o myFile hello.c

#只编译源文件而不进行链接,有些东西在编译的时候是没问题的,链接就会有问题,这个会生成.o文件
gcc -c hello.c

#编译时可生成调试信息
gcc -g hello.c

#还有就是编译标准,就是使用c11标准来编译源文件

gcc -std=c11 hello.c
```
个人认为这就是比较有用的命令.


