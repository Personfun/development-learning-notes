# development-learning-notes

**阅读指引**：本仓库为个人编程语言学习笔记，持续更新中。建议从 [C 语言](#一-c-语言) 开始阅读，配合 [Python](#二-python)、[Java](#三-java) 和 [PHP](#四-php) 进行系统学习。

本仓库记录了我从零开始学习 C、Python、Java、PHP 等编程语言的全过程，以及这些语言在安全开发领域的应用实践。

## 一、C 语言

从语言基础到安全应用，分为两条主线。基础线覆盖指针、内存、数据结构；安全线覆盖 Windows API、Socket、Bof、Shellcode 等红队工具开发能力。

### 语言基础（Basics）

- [01 - 基础语法](./C/Basics/01_Basics.md)：变量、数据类型、输入输出、运算符
- [02 - 控制流](./C/Basics/02_Control_Flow.md)：if-else、while、for、switch
- [03 - 函数](./C/Basics/03_Functions.md)：函数定义、参数、返回值、递归
- [04 - 数组与字符串](./C/Basics/04_Arrays_and_Strings.md)：数组、字符串、常用字符串函数
- [05 - 指针](./C/Basics/05_Pointers.md)：地址、解引用、指针与数组、二级指针
- [06 - 结构体与内存管理](./C/Basics/06_Structs_and_Memory.md)：struct、malloc/free、内存对齐
- [07 - 数据结构](./C/Basics/07_Data_Structures.md)：链表、栈、队列、树的 C 实现
- [08 - 踩坑记录](./C/Basics/08_Error_Log.md)：分号、野指针、内存泄漏、段错误

### 安全应用（Security）

C 语言在红队工具开发中的应用方向。等基础打牢后逐步深入。

- Windows API 编程：调用系统底层 API
- Socket 网络编程：TCP/UDP 通信、反弹 Shell
- Bof 开发：Beacon Object File 插件编写
- Shellcode 编写：机器码提取与加载
- PE 结构分析：PE 文件格式、内存加载
- 免杀基础：绕过杀软的文件与内存扫描

## 二、Python

涵盖 Python 语言基础及安全脚本开发。

- [语言基础（Basics）](./Python/Basics/)：语法、函数、面向对象、常用库
- [安全应用（Security）](./Python/Security/)：端口扫描、目录爆破、Web 爬虫、自动化渗透

## 三、Java

涵盖 Java 语言基础及安全代码审计。

- [语言基础（Basics）](./Java/Basics/)：语法、面向对象、集合框架、IO 流
- [安全应用（Security）](./Java/Security/)：Java Web 代码审计、反序列化漏洞、中间件安全

## 四、PHP

涵盖 PHP 语言基础及 Web 安全代码审计。

- [语言基础（Basics）](./PHP/Basics/)：语法、函数、PDO 数据库操作
- [安全应用（Security）](./PHP/Security/)：代码审计、SQL 注入、文件包含、WebShell 免杀

## 五、学习路线

- C 语言基础 → 数据结构 → Windows API → Bof / Shellcode / 免杀
- Python 基础 → 安全脚本（端口扫描、目录爆破、Web 爬虫）
- Java 基础 → 代码审计 → 反序列化漏洞分析
- PHP 基础 → 代码审计 → 常见 Web 漏洞挖掘

## 六、说明

本仓库仅用于个人学习记录。所有代码和笔记均为原创或注明来源，仅供学习参考。

## 七、版权声明

本仓库所有代码采用 [MIT License](./LICENSE) 协议进行许可。
