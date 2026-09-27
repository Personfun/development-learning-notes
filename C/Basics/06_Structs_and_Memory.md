# 06 - 结构体与动态内存 (Structs and Dynamic Memory)

结构体让我们可以自定义数据类型，而动态内存让程序在运行时可以按需申请空间。两者结合，是链表、树等所有高级数据结构的基础。

## 一、结构体 (struct)

### 1. 定义新类型
```c
struct Node {
    int data;
    struct Node *next;
};
```
- `struct Node` 是一种**自定义数据类型**，类似于 `int`、`float`。
- 花括号 `{}` 内部包含了该类型的成员变量。
- **末尾必须加分号 `;`**（这是新手高频错误）。

### 2. 使用结构体
- **结构体变量**访问成员用 `.`：
  ```c
  struct Node n1;
  n1.data = 10;
  n1.next = NULL;
  ```
- **结构体指针**访问成员用 `->`：
  ```c
  struct Node *p = (struct Node *)malloc(sizeof(struct Node));
  p->data = 10;
  p->next = NULL;
  ```
  `p->data` 等价于 `(*p).data`。

## 二、动态内存管理 (malloc / free)

### 1. 为什么需要动态内存？
链表节点数量不固定。如果写成 `struct Node n1;` 只能固定创建一个，无法按需增加。所以必须在程序运行时“按需申请内存”。

### 2. malloc：申请内存
```c
struct Node *p = (struct Node *)malloc(sizeof(struct Node));
```
拆解：
- `sizeof(struct Node)`：计算这个结构体占多少字节。
- `malloc(...)`：向系统申请这么多字节的内存，返回首地址（类型是 `void *`）。
- `(struct Node *)`：把无类型指针强制转换为具体的结构体指针类型。
- `p`：接收这个地址，指向新申请的内存。

### 3. free：释放内存
```c
free(p);
p = NULL; // 释放后置为 NULL，防止变成野指针
```
**注意**：`malloc` 和 `free` 必须成对出现。申请了内存却不释放，会导致**内存泄漏**，长时间运行的程序会耗尽系统内存。

## 三、内存泄漏与野指针

### 1. 内存泄漏 (Memory Leak)
- 原因：`malloc` 申请了内存，但忘记 `free`；或者丢失了指向该内存的指针（如链表断链）。
- 后果：内存越占越多，程序最终崩溃。

### 2. 野指针 (Wild Pointer)
- 原因：指针未初始化，或者 `free` 后没有置空。
- 后果：操作野指针会修改未知的内存区域，导致程序崩溃（段错误）。

## 四、链表实战模板（所有数据结构的基础）
```c
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node *next;
};

int main() {
    // 1. 创建节点
    struct Node *node1 = (struct Node *)malloc(sizeof(struct Node));
    struct Node *node2 = (struct Node *)malloc(sizeof(struct Node));
    
    // 2. 赋值
    node1->data = 10;
    node2->data = 20;
    
    // 3. 连接
    node1->next = node2;
    node2->next = NULL;
    
    // 4. 遍历
    struct Node *p = node1;
    while (p != NULL) {
        printf("%d ", p->data);
        p = p->next;
    }
    
    // 5. 释放内存（先保存下一个，再释放当前）
    free(node1);
    free(node2);
    
    return 0;
}
```

## 五、踩坑记录
1. `sizeof` 不要写成 `sizeof(struct Node)` 以外的类型，尤其是指针类型要注意。
2. 删除链表节点时，一定要先用临时指针保存被删节点，再断链，最后 `free`。
3. `free` 之后，指针里存的地址仍存在，但内存已经无效，一定要置 `NULL`。
