# 07 - 数据结构实战 (Data Structures in C)

用 C 语言手写基础数据结构是 408 和复试机试的核心基本功，也是理解指针和内存管理的最佳途径。

## 一、单链表 (Singly Linked List)

### 1. 节点定义
```c
struct Node {
    int data;
    struct Node *next;
};
```

### 2. 创建与连接
```c
struct Node *node1 = (struct Node *)malloc(sizeof(struct Node));
node1->data = 10;
node1->next = NULL;

struct Node *node2 = (struct Node *)malloc(sizeof(struct Node));
node2->data = 20;
node2->next = NULL;

node1->next = node2; // 连接
```

### 3. 遍历
```c
struct Node *p = node1; // 每次遍历前必须重新指向头节点
while (p != NULL) {
    printf("%d ", p->data);
    p = p->next;
}
```

### 4. 插入节点（在 node1 和 node2 之间插入 new_node）
```c
// 顺序绝对不能反，否则会丢失后继节点的地址
new_node->next = node1->next; // 1. 新节点指向后继
node1->next = new_node;       // 2. 前驱指向新节点
```

### 5. 删除中间节点（删除 node2）
```c
new_node->next = node2->next; // 1. 前驱跳过被删节点
free(node2);                  // 2. 释放内存
node2 = NULL;                 // 3. 置空防野指针
```

### 6. 删除头节点（标准三步）
```c
struct Node *temp = head; // 1. 临时指针保存旧头
head = head->next;        // 2. head 后移
free(temp);               // 3. 释放旧头
```

## 二、双链表 (Doubly Linked List)

### 1. 节点定义
```c
struct DNode {
    int data;
    struct DNode *prev;
    struct DNode *next;
};
```

### 2. 插入（在 p 之后插入 s）
```c
s->next = p->next;
s->prev = p;
if (p->next != NULL) {
    p->next->prev = s;
}
p->next = s;
```

### 3. 删除（删除 p 的后继 q）
```c
p->next = q->next;
if (q->next != NULL) {
    q->next->prev = p;
}
free(q);
```

## 三、栈和队列（C语言实现思路）

### 1. 顺序栈（数组实现）
```c
int stack[100];
int top = -1; // 栈顶指针

// 入栈
stack[++top] = x;

// 出栈
x = stack[top--];
```

### 2. 链队列（链表实现）
```c
struct QNode {
    int data;
    struct QNode *next;
};
struct Queue {
    struct QNode *front; // 队头
    struct QNode *rear;  // 队尾
};
```

## 四、数据结构学习心法
1. **画图**：写链表、树、图之前，一定要在纸上画出节点和指针的指向关系。
2. **先改指针，再改数值**：插入和删除时，指针操作顺序错了会直接导致断链。
3. **管理内存**：每次 `malloc` 都要在心里记一笔，最后要对应 `free`。
