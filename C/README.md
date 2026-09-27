# C 语言学习笔记

本目录记录我学习 C 语言的全过程，分为「基础」和「安全应用」两条线。

## 目录结构

```
C/
├── Basics/                          基础
│   ├── 01_Basics/                   变量、数据类型、输入输出、运算符
│   ├── 02_Control_Flow/             if-else、while、for、switch
│   ├── 03_Functions/                函数定义、参数、返回值、递归
│   ├── 04_Arrays_and_Strings/       数组、字符串
│   ├── 05_Pointers/                 指针基础、地址、解引用
│   ├── 06_Structs_and_Memory/       结构体、malloc/free
│   ├── 07_Data_Structures/          用 C 实现的数据结构（链表、树等）
│   └── 08_Error_Log/                踩坑记录（分号、野指针等）
└── Security/                        安全应用
    ├── 01_Windows_API/              Windows API 编程
    ├── 02_Socket/                   Socket 网络编程
    ├── 03_Bof/                      Beacon Object File 开发
    ├── 04_Shellcode/                Shellcode 编写
    ├── 05_PE_Structure/             PE 结构分析
    └── 06_Evasion/                  免杀基础
```

## 学习进度

### 基础（Basics）

| 编号 | 主题 | 状态 |
| :--- | :--- | :--- |
| 01 | [Basics](./Basics/01_Basics/) | 已完成 |
| 02 | [Control Flow](./Basics/02_Control_Flow/) | 待补充 |
| 03 | [Functions](./Basics/03_Functions/) | 待补充 |
| 04 | [Arrays and Strings](./Basics/04_Arrays_and_Strings/) | 待补充 |
| 05 | [Pointers](./Basics/05_Pointers/) | 已完成 |
| 06 | [Structs and Memory](./Basics/06_Structs_and_Memory/) | 已完成 |
| 07 | [Data Structures](./Basics/07_Data_Structures/) | 进行中 |
| 08 | [Error Log](./Basics/08_Error_Log/) | 待补充 |

### 安全应用（Security）

| 编号 | 主题 | 状态 |
| :--- | :--- | :--- |
| 01 | Windows API | 未来计划 |
| 02 | Socket | 未来计划 |
| 03 | Bof | 未来计划 |
| 04 | Shellcode | 未来计划 |
| 05 | PE Structure | 未来计划 |
| 06 | Evasion | 未来计划 |

## 代码目录

| 文件 | 说明 |
| :--- | :--- |
| [double_linked_list.c](./Basics/07_Data_Structures/codes/double_linked_list.c) | 双向链表的创建与遍历 |

## 学习目标

1. **基础阶段**：掌握 C 语言核心语法、指针、内存管理、数据结构
2. **安全阶段**：能读懂 CS 的 Bof 源码、能写简单的反弹 Shell、理解免杀原理

## 参考资料

- 《C Primer Plus》
- 《C 和指针》
- CS 官方文档
