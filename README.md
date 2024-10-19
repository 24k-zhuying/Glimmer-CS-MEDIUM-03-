# CS-MEDIUM-03 实验：Linux命令行实现

* linux环境配置：我是通过哔站上的黑马程序员的linux系统教学一步步配置，包括安装vmware，CentOS，finalshell等。

## 随之而来的挑战
[运行过程与运行结果](myls.png)

* 上述程序的头文件你见过哪些，没见过哪些？
答： 见过<stdio.h> <string.h> <stdlib.h> <time.h>，没见过<dirent.h> <sys/stat.h> <sys/types.h>
 
* 程序的运行从哪个地方开始？
答：从main函数开始。

* 哪些函数是自定义函数，哪些是库函数？这些库函数分别属于哪些库？
答：自定义函数：print_file_info，list_directory。库函数：opendir（stdio.h）、readdir（stdio.h）、stat（sys/stat.h）、closedir（stdio.h）、perror（stdio.h）、exit（stdlib.h）、strftime（time.h）、snprintf（stdio.h）

* argc，*argv[]作为主函数的运行参数，它们的含义是什么？是在哪里输入的？
答：argc代表命令行参数的个数，argv是一个字符指针数组，用于存储命令行参数的字符串。是在命令行中输入的

* 有哪些语法/语句段/函数是你不理解/不清楚的？如何借助资料与工具了解它们的含义？
答：strftime函数，“DIR *dir”，opendir函数，closedir函数，readdir函数，snprintf函数，localtime函数，其它的语法函数感觉还好。可以借助AI，CSDN，菜鸟社区，GitHub等等。

理解该程序过程：刚开始的时候看到这个程序两眼一黑，一堆没见过的东西，于是就想直接跳了不理解这个程序了但看到下一个题又两眼一黑不理解这个程序根本不知道怎么做。所以我从该程序的开头慢慢看，发现第一个函数内容比较简单，主要负责输出，但其中还是有一些陌生的东西，所以我决定先理解最主要的那个函数。当仔细看list_directory函数的时候又让我两眼一黑，开头三个结构体没看懂为什么直接定义了，于是问了ai知道了这是头文件里面的结构体和在目录流操作中各自的作用，后续我又在CSDN和ai上问了目录流操作的大概原理，又结合每个陌生函数的定义和作用（opendir函数，closedir函数，readdir函数等），我大致理解了该程序的运行过程。

## 举一反三

请你结合对上述的知识点以及对程序的研究成果，使用C语言完成对pwd命令（print work directory，命令用于显示工作目录）的实现，并将程序保存并命名为mypwd.c。如果实现结果令你满意，请附上运行成功的结果，如果实现效果不佳，请说明你遇到的问题和完成程度。

[代码展示](举一反三.md)

[运行截图(在linux系统下运行)](举一反三.png)
