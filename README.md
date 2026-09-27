# development-learning-notes

**阅读指引**：本仓库为个人编程语言学习笔记，持续更新中。建议从 [C 语言](#一-c-语言) 开始阅读，配合 [Python](#二-python) 和 [Java](#三-java) 进行系统学习。

本仓库记录了我从零开始学习 C、Python、Java 等编程语言的全过程，以及这些语言在安全开发领域的应用实践。

## 一、C 语言

从语言基础到安全应用，分为两条主线。基础线覆盖指针、内存、数据结构；安全线覆盖 Windows API、Socket、Bof、Shellcode 等红队工具开发能力。

### 语言基础（Basics）
涵盖变量、数据类型、控制流、函数、指针、结构体、动态内存及用 C 实现的数据结构。

- [01 - 基础语法（变量、数据类型、输入输出、运算符）](./C/Basics/01-basics.md)
- [02 - 控制流（if-else、while、for、switch）](./C/Basics/02-control-flow.md)
- [03 - 函数（定义、参数、返回值、递归）](./C/Basics/03-functions.md)
- [04 - 数组与字符串](./C/Basics/04-arrays-and-strings.md)
- [05 - 指针（地址、解引用、指针与数组）](./C/Basics/05-pointers.md)
- [06 - 结构体与内存管理（malloc / free）](./C/Basics/06-structs-and-memory.md)
- [07 - 数据结构（链表、栈、队列、树）](./C/Basics/07-data-structures.md)
- [08 - 踩坑记录（分号、野指针、内存泄漏）](./C/Basics/08-error-log.md)

### 安全应用（Security）
涵盖 C 语言在红队工具开发中的应用方向。

- [Windows API 编程](./C/Security/)
- [Socket 网络编程](./C/Security/)
- [Bof（Beacon Object File）开发](./C/Security/)
- [Shellcode 编写](./C/Security/)
- [PE 结构分析](./C/Security/)
- [免杀基础](./C/Security/)

## 二、Python

涵盖 Python 语言基础及安全脚本开发。

### 语言基础（Basics）
- 待补充

### 安全应用（Security）
- 待补充

## 三、Java

涵盖 Java 语言基础及安全代码审计。

### 语言基础（Basics）
- 待补充

### 安全应用（Security）
- 待补充

## 四、学习路线

- C 语言基础 → 数据结构 → Windows API → Bof / Shellcode / 免杀
- Python 基础 → 安全脚本（端口扫描、目录爆破、Web 爬虫）
- Java 基础 → 代码审计 → 反序列化漏洞分析

## 五、说明

本仓库仅用于个人学习记录。所有代码和笔记均为原创或注明来源，仅供学习参考。

## 六、版权声明

本仓库所有代码采用 [MIT License](./LICENSE) 协议进行许可。
