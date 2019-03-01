# lec1: 操作系统概述

---

## **提前准备**

（请在上课前完成）

* 完成lec1的视频学习和提交对应的在线练习
* git pull ucore\_os\_lab, ucore\_os\_docs, os\_tutorial\_lab, os\_course\_exercises in github repos。这样可以在本机上完成课堂练习。
* 知道OS课程的入口网址，会使用在线视频平台，在线练习/实验平台，在线提问平台\(piazza\)
  * [http://os.cs.tsinghua.edu.cn/oscourse/OS2019spring](http://os.cs.tsinghua.edu.cn/oscourse/OS2019spring)


* 会使用linux shell命令，如ls, rm, mkdir, cat, less, more, gcc等，也会使用linux系统的基本操作。
* 在piazza上就学习中不理解问题进行提问。



# 思考题

## 填空题

* 当前常见的操作系统主要用C编程语言编写。
* "Operating system"这个单词起源于Operator。
* 在计算机系统中，控制和管理各种资源 、有效地组织多道程序运行的系统软件称作操作系统 。
* 允许多用户将若干个作业提交给计算机系统集中处理的操作系统称为批处理操作系统
* 你了解的当前世界上使用最多的操作系统是安卓。
* 应用程序通过程序级接口获得操作系统的服务。
* 现代操作系统的特征包括并发 ， 共享 ， 虚拟 ，异步 。
* 操作系统内核的架构包括宏内核 ， 微内核 ， 外核 。


## 问答题

- 请总结你认为操作系统应该具有的特征有什么？并对其特征进行简要阐述。

  答：操作系统是一种软件，这个软件是为了更好的协调在这个基础上的软件和硬件之间的配合工作。正如填空题所言，我认为操作系统应该具有四个特征，即并发、共享、虚拟和异步。并发指的是在操作系统可以提供多个程序同时运行的环境。当然，每时每刻在运行的程序可能有且仅有一个，但操作系统通过调度的手段让用户看起来很多程序在同时运行。共享指的是软件硬件资源可以被多个应用使用，这些应用通过操作系统的调度调配，达到互不干涉共同运行的目的。虚拟指的是操作系统让每个用户和应用在使用计算机的时候都能感觉自己完全占有了该计算机，这是非常重要的，因为这样可以大大方便开发者和使用者对于计算机的操作，不需要担心干扰别的应用或个人。异步指的是每个程序在执行上并不是由同一个时钟连续控制的，而是允许资源使能或暂停，是一种异步的存在。

- 为什么现在的操作系统基本上用C语言来实现？为什么没有人用python，java来实现操作系统？

  答：操作系统在计算机行业的非常早期就存在了，比如最早期的dos，在那个时候python和java还不是主流的语言，自然大多数程序员和公司选择使用C语言来实现。另外python是解释性语言，而java通过java虚拟机实现，在运行效率上远没法达到C的效率，作为操作系统当然需要敏捷快速，不然非常影响用户体验。同时，操作系统作为软件和硬件交互的软件，需要大量的硬件开发，C语言中的asm类指令很好的支持了这一类开发，所以比python和java更加合适。最后，我私以为C语言比python和java好用得不要太多。

---

## 可选练习题

---

- 请分析并理解[v9\-computer](https://github.com/chyyuu/os_tutorial_lab/blob/master/v9_computer/docs/v9_computer.md)以及模拟v9\-computer的em.c。理解：在v9\-computer中如何实现时钟中断的；v9 computer的CPU指令，关键变量描述有误或不全的情况；在v9\-computer中的跳转相关操作是如何实现的；在v9\-computer中如何设计相应指令，可有效实现函数调用与返回；OS程序被加载到内存的哪个位置,其堆栈是如何设置的；在v9\-computer中如何完成一次内存地址的读写的；在v9\-computer中如何实现分页机制。


- 请编写一个小程序，在v9-cpu下，能够输出字符


- 输入的字符并输出你输入的字符


- 请编写一个小程序，在v9-cpu下，能够产生各种异常/中断


- 请编写一个小程序，在v9-cpu下，能够统计并显示内存大小



- 请分析并理解[RISC-V CPU](http://www.riscvbook.com/chinese/)以及会使用模拟RISC\-V(简称RV)的qemu工具。理解：RV的特权指令，CSR寄存器和在RV中如何实现时钟中断和IO操作；OS程序如何被加载运行的；在RV中如何实现分页机制。
  - 请编写一个小程序，在RV下，能够输出字符
  - 输入的字符并输出你输入的字符
  - 请编写一个小程序，在RV下，能够产生各种异常/中断
  - 请编写一个小程序，在RV下，能够统计并显示内存大小

## 参考资料
 - [Intel格式和AT&T格式汇编区别](http://www.cnblogs.com/hdk1993/p/4820353.html)
 - [x86汇编指令集  ](http://hiyyp1234.blog.163.com/blog/static/67786373200981811422948/)
 - [PC Assembly Language, Paul A. Carter, November 2003.](https://pdos.csail.mit.edu/6.828/2016/readings/pcasm-book.pdf)
 - [*Intel 80386 Programmer's Reference Manual*, 1987](https://pdos.csail.mit.edu/6.828/2016/readings/i386/toc.htm)
 - [IA-32 Intel Architecture Software Developer's Manuals](http://www.intel.com/content/www/us/en/processors/architectures-software-developer-manuals.html)
 - [v9 cpu architecture](https://github.com/chyyuu/os_tutorial_lab/blob/master/v9_computer/docs/v9_computer.md)
 - [RISC-V cpu architecture](http://www.riscvbook.com/chinese/)
 - [OS相关经典论文](https://github.com/chyyuu/aos_course_info/blob/master/readinglist.md)
