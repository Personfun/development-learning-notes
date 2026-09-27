# development-learning-notes

**阅读指引**：本仓库为个人编程语言学习笔记，持续更新中。建议从 [C 语言](#一-c-语言) 开始阅读，配合 [Python](#二-python)、[Java](#三-java) 和 [PHP](#四-php) 进行系统学习。

本仓库记录了我从零开始学习 C、Python、Java、PHP 等编程语言的全过程，以及这些语言在安全开发领域的应用实践。

## 一、C 语言

从语言基础到安全应用，分为两条主线。基础线覆盖指针、内存、数据结构；安全线覆盖 Windows API、Socket、Bof、Shellcode 等红队工具开发能力。

### 语言基础（Basics）

- [01 - 基础语法](./C/Basics/01-basics.md)
- [02 - 控制流](./C/Basics/02-control-flow.md)
- [03 - 函数](./C/Basics/03-functions.md)
- [04 - 数组与字符串](./C/Basics/04-arrays-and-strings.md)
- [05 - 指针](./C/Basics/05-pointers.md)
- [06 - 结构体与内存管理](./C/Basics/06-structs-and-memory.md)
- [07 - 数据结构](./C/Basics/07-data-structures.md)
- [08 - 踩坑记录](./C/Basics/08-error-log.md)

### 安全应用（Security）

- [Windows API 编程](./C/Security/)
- [Socket 网络编程](./C/Security/)
- [Bof 开发](./C/Security/)
- [Shellcode 编写](./C/Security/)
- [PE 结构分析](./C/Security/)
- [免杀基础](./C/Security/)

## 二、Python

涵盖 Python 语言基础及安全脚本开发。

- [语言基础（Basics）](./Python/Basics/)
- [安全应用（Security）](./Python/Security/)

## 三、Java

涵盖 Java 语言基础及安全代码审计。

- [语言基础（Basics）](./Java/Basics/)
- [安全应用（Security）](./Java/Security/)

## 四、PHP

涵盖 PHP 语言基础及 Web 安全代码审计。

- [语言基础（Basics）](./PHP/Basics/)
- [安全应用（Security）](./PHP/Security/)

## 五、学习路线

- C 语言基础 → 数据结构 → Windows API → Bof / Shellcode / 免杀
- Python 基础 → 安全脚本（端口扫描、目录爆破、Web 爬虫）
- Java 基础 → 代码审计 → 反序列化漏洞分析
- PHP 基础 → 代码审计 → 常见 Web 漏洞挖掘

## 六、说明

本仓库仅用于个人学习记录。所有代码和笔记均为原创或注明来源，仅供学习参考。

## 七、版权声明

本仓库所有代码采用 [MIT License](./LICENSE) 协议进行许可。
