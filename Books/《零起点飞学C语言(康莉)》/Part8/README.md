
## 第十章 构造数据类型及其应用



1.结构体，链表，共用体，枚举。

---

2.变量不能反映内在联系，数组不能存放不同类型的数据，所以，C语言提供了另外一种构造类型数据：结构体。

---


3.定义一个结构体类型的一般形式：

---

```
struct 结构体类型名
{ 

  类型名1 结构体成员名1；

  类型名2 结构体成员名2；

  …

  类型名n 结构体成员名n；

}
```

例：
```
struct employee
{

  char name[20];  //姓名

  int age;        //年龄

  char sex;       //性别

  float salary;   //工资

}
```

---


4.定义结构体变量

- struct 结构体类型名 结构体变量名;

例：```struct employee emp1,emp2;```


---

5.C语言引用结构体成员的方式：用结构体成员运算符方式和指针方式。


---

6.结构体成员运算符引用结构体成员的形式：


- <结构体类型变量名>.<成员名>

---


7.结构体变量初始化一般形式：

- struct 结构体名 结构体变量名={各成员初始数据}

---


8.结构体数组：

- struct 结构体类型名 结构体数组;

---


9.类型转换函数：(头文件-stdlib.h)

- atoi()-字符串转整形

- atof()-字符串转实型

- atol()-字符串转长整形


---

10.结构体指针：

- struct 结构体名 *结构体指针名;


---

11.通过结构体指针来引用结构体变量的成员：

- (*结构体指针名).成员名  或

- 结构体指针名->成员名

---


12.链表：常见的重要数据结构，是动态的进行存储单元分配的一种结构。


---

13.分配内存空间函数malloc()

```void malloc (unsigned int size)```

或

```(类型说明符 *) malloc (unsigned int size)```

---


14.分配内存空间函数calloc()

```void *calloc(unsigned int n, unsigned int size)```

或

```(类型说明符 *) calloc (unsigned int n, unsigned int size)```


calloc()与malloc()的区别仅在于一次可以分配n块区域。


---

15.释放内存空间函数free()

```free(void *ptr);```

---


16.改变已分配内存空间长度函数realloc()

```void realloc (void *ptr, unsigned int size)```

或

```(类型说明符 *) realloc (void *ptr,unsigned int size)```


---

17.链表的主要操作有4种：

- 建立链表
- 结构的查找与输出
- 插入一个结点
- 删除一个结点。


---

18.共用体
```
union 共用体名
{

  成员表列;

}
```

---

19.共用体中，各成员共享一段内存空间，长度等于各成员中最长的长度。


---

20.共用体变量的地址和它的各个成员的地址都是同一个地址。

---


21.枚举
```
enum 枚举名
{

  枚举值表;

};
```

---

22.自定义类型-typedef

- typedef 原类型名 新类型名
