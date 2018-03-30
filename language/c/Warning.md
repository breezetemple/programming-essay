# 编译警告

<!-- toc -->

### 多维数组初始化

> 没有用大括号明确的区分出初始化数据的归类

```bash
warning: missing braces around initializer : (near initialization for 's1[0]')
```

```c
//int num[2][2] = {0, 1, 2, 3};
//int num[2][2] = {0};
int num[2][2] = {
    {0, 1}, 
    {2, 3}
};
int num[2][2] = {
    {0}, 
};
```

### 函数未定义

```bash
warning: implicit declaration of function 'Example()'
```

### 参数未使用

```bash
warning: unused variable 'param'
```

### 判断无效

```bash
warning: comparison is always 0 due to limited range of data type
```

```c
unsigned int min_num = 0;
if(min_num < 0) {
    //TODO
}
```

### 函数无返回值

```bash
warning: control reaches end of non-void function
```

### 数值变换丢失

> 变量的变换有可能导致数值的越界

```bash
warning: overflow in implicit constant conversion
```

### 变量未初始化

```bash
warning: 'ulParam' might be used uninitialized in this function
```

### 重定义 

```bash
warning: `MY_DEBUG'  redefined
```

### 变量未使用

```bash
warning: value computed is not used
```

### 类型不一致

```bash
warning: int format, long int arg (arg 3)
```

### 指针类型

> 指针变量复制给int变量

```bash
warning：make pointer from integer without a cast
```

```c
//SaveBuffer2(0, t, 1);
SaveBuffer2(0, &t, 1);
```

