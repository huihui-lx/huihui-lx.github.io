---
title: C++做题常用STL
author: huihui-lx
avatar: https://cdn.jsdelivr.net/gh/huihui-lx/cdn@6.0/img/head_portrait/1.jpg
authorLink: huihui-lx.com
categories: 技术
date: 2021-9-16 19:00
comments: true
tags: 
    - 算法
keywords: Sakura
description: 忘了就看
photos: https://cdn.jsdelivr.net/gh/huihui-lx/cdn@6.0/img/background/1.jpg
---

# C++做题常用stl



## vector  
1. 初始化
	```C++
	vector<int> a;
   vector<int> a(10, 1); //初始化10个1
	vector<vector<int> > v (n, vector<int> (m));
	```
	
2. 常用函数

   ```C++
   length()/size()  //返回元素个数
   empty() 		//判断是否为空
   clear()			//清空
   front()/back()  //返回第一个/最后一个元素
   push_back()/pop_back() //往最后压入一个元素, 弹出最后一个元素
   begin()/end() //返回第一个/最后一个元素的迭代器
   resize(n, m) //调整容器大小, 使用其包含n个元素
   reverse(a.begin, a.end()) //翻转一个vector
   reverse(a + 1, a + n + 1) //翻转一个数组, 元素存放在下标1~n
   [] //随机访问
   ```
   

## string
1. 常用函数

   ```c++
   length()/size() //返回字符串长度
   empty() //判断是否为空
   clear() //清空
   substr(起始下标, 子串长度) //返回子串
   c_str() // 返回字符串所在字符数组的起始地址
   to_string(int x) // int 转 string 
   reverse(s.begin(), s.end()) //反转字符串, 无返回值
   atoi() //字符串(char*)转int   aoto(s.c_str())
   
   ```
   
## queue

1. 常用函数

   ```C++
   size()  //无length函数
   empty()
   push() //向队尾插入一个元素
   front() //返回队头元素
   back() //返回队尾元素
   pop() //弹出队头元素
   ```

## priority_queue

1. 常用函数

   ```C++
   size()
   empty()
   push()
   top() //返回堆顶元素
   pop() //弹出堆顶元素
   
   ```

2. 定义成小根堆

   ```c++
   //默认是大根堆, 定义成小根堆的方式为
   priority_queue<int, vecotr<int>, greater<int> > heap;
   ```



## stack

```C++
size()
empty()
push() //向栈顶插入元素
top() //返回栈顶元素
pop() //弹出栈顶元素
```



## deque

1. 常用函数

```c++
size()
empty()
clear()
front()/back //返回队头/队尾元素
push_back()/push_front() //队尾/队头压入
pop_back()/pop_front() //队尾/队头弹出
begin()/end()    
[] //随机访问
```

## set map multiset multimap

```C++
//基于红黑树实现 
1. 增删改查为o(logn)
2. set/map不允许重复元素/key, multiset/multimap允许重复元素/key
3. 有序,默认升序
size()
empty()
clear()
begin()/end()

set/multiset
    insert() //插入一个数
    find() //查找一个数 返回改元素的迭代器, 若不存在返回end()
    count() //返回一个数的个数 
    erase()
        (1) //输入一个数x, 删除所有的x o(k + logn)
        (2) //输入一个迭代器, 删除这个迭代器
    lower_bound/upper_bound
        lower_bound(x) //返回大于等于x的最小的数的迭代器
        upper_bound(x) //返回大于x的最小的数的迭代器
 
  map/multimap
  	insert() //插入一个pair
    erase() //输入的参数是pair或迭代器
    find() 
    []  注意multimap不支持此操作。 时间复杂度是 O(logn)
    lower_bound()/upper_bound()
```

## unorderd_set unorderd_map unordered_multiset unordered_multimap 

```C++
//基于哈希表实现
1. 增删改查为o(1)
2. 无序
3. 不支持lower_bound()/upper_bound
```
