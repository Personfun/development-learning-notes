# C 语言学习笔记

本目录记录我学习 C 语言的全过程，分为「基础」和「安全应用」两条主线。

- **基础线**：从语法、指针、内存管理到数据结构，打牢语言功底
- **安全线**：从 Windows API、Socket 到 Bof、Shellcode，走向红队工具开发

## 一、语言基础（Basics）

C 语言的核心语法、指针操作、动态内存管理，以及用 C 实现的基础数据结构。

- [01 - 基础语法](./Basics/01_Basics.md)：变量、数据类型、输入输出、运算符
- [02 - 控制流](./Basics/02_Control_Flow.md)：if-else、while、for、switch
- [03 - 函数](./Basics/03_Functions.md)：函数定义、参数、返回值、递归
- [04 - 数组与字符串](./Basics/04_Arrays_and_Strings.md)：数组、字符串、常用字符串函数
- [05 - 指针](./Basics/05_Pointers.md)：地址、解引用、指针与数组、二级指针
- [06 - 结构体与内存管理](./Basics/06_Structs_and_Memory.md)：struct、malloc/free、内存对齐
- [07 - 数据结构](./Basics/07_Data_Structures.md)：链表、栈、队列、树的 C 实现
- [08 - 踩坑记录](./Basics/08_Error_Log.md)：分号、野指针、内存泄漏、段错误

## 二、安全应用（Security）

C 语言在红队工具开发中的应用方向。等基础打牢后，逐步深入。

- Windows API 编程
- Socket 网络编程
- Bof（Beacon Object File）开发
- Shellcode 编写与加载
- PE 结构分析
- 免杀基础

## 三、学习目标

1. **基础阶段**：掌握 C 语言核心语法、指针、内存管理、数据结构
2. **安全阶段**：能读懂 CS 的 Bof 源码、能写简单的反弹 Shell、理解免杀原理

## 四、参考资料

- 《C Primer Plus》
- 《C 和指针》
- Cobalt Strike 官方文档
