## 常见O
O(logn)对数时间，二分查找 <br>
O(n)线性时间，简单查找 <br>
O(nlogn)较快，快速排序，合并排序 <br>
O(n2)较慢，选择排序 <br>
O(n!)非常慢，旅行商问题 <br>



## 数据结构

### 常见时间复杂度
array {
	read: O(1);
	insert: O(n);
	delete: O(n);
}
linked-list {
	read: O(n);
	insert: O(1);
	delete: O(1);
}
hash-table {
	read: O(1);
	insert: O(1);
	delete: O(1);
}

数组只能存储相同的数据类型;
数组支持随机访问和顺序访问，而链表只支持顺序访问;

### 散列函数(hash function)
properties：
- 一致的，输入相同的输入，总是输出同样的输出
- 不同的输入返回不同的输出
Examples:
- DNS resolution
- avoid repetition
- Cache

### 散列表(hash table)
- avoid collision
- load factor = elementNumber/bucketNumber
Resize when load factor is large (0.7)
- hash function: SHA function

### 图(graph)
graph is built with nodes and edges;
The nodes that are connected with edge are called neighbor;
there are directed graph and undirected graph

### 栈(stack)
栈: 先入后出(LIFO)的数据结构;
递归使用调用栈(call stack)，调用栈可能很长，这将占用大量的内存;

### 队列(queue)
队列: 先进先出(FIFO)的数据结构;




## 排序算法

### 选择排序 selection sort
for i in n:
	for j in n[i:]:
O(n2)

### 快速排序 quick sort
partitioning
O(nlogn)



## 广度优先搜索
- 是否存在路径
- 计算最短距离(最短路径)
O(V+E)
- V: Number of vertice
- E: Number of edges






## D&C
Divide and Conquer 分而治之







