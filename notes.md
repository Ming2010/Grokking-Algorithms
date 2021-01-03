## 常见O (Common time complexity)
O(logn)对数时间，二分查找  
O(n)线性时间，简单查找  
O(nlogn)较快，快速排序，合并排序  
O(n2)较慢，选择排序  
O(n!)非常慢，旅行商问题  



## 数据结构(data structure)

### 常见时间复杂度(Common time complexity)
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
Types:  
- there are directed graph and undirected graph;
- there are weighted graph and unweighted graph;

### 栈(stack)
栈: 先入后出(LIFO)的数据结构;  
递归使用调用栈(call stack)，调用栈可能很长，这将占用大量的内存;  

### 队列(queue)
队列: 先进先出(FIFO)的数据结构;




## 排序算法(sort algorithms)

### 选择排序(selection sort)
for i in n:  
	for j in n[i:]:  
O(n2)  

### 快速排序(quick sort)
partitioning  
O(nlogn)  



## 图算法--图广度优先搜索与迪克斯特拉算法

### 广度优先搜索(breadth first algorithm)
- 是否存在路径
- 搜索最短路径(段数最少)  
O(V+E)
- V: Number of vertice
- E: Number of edges

### 迪克斯特拉算法(Dijkstra’s algorithm)
- 搜索最短路径(总权重weight最小)  
步骤:
1. 找出最便宜的节点
2. 对于该节点的邻居，检查是否有前往它们的更短路径，如果有，就更新其开销
3. 重复这个过程，直到对图中的每个节点都这样做了
4. 计算最终路径  
适用范围:
- 仅适用于有向无环图(directed acyclic graph)
- 仅适用于所有权重都为正的图(贝尔曼-福德算法 Bellman-Ford algorithm)

## 复杂问题的近似最优解--贪心算法与NP完全问题

### 贪心算法(greedy algorithm)
贪心算法寻找局部最优解，企图以这种方式获得全局最优解。  
贪心算法是一种近似算法(approximation algorithm)，评判近似算法的标准为:	
- 速度有多快
- 得到的近似解与最优解的接近程度  
可用于解决NP完全问题

### NP完全问题(Non-deterministic Polynomial Problem)
- 涉及“所有组合”的问题通常是NP完全问题
- 不能将问题分成小问题，必须考虑各种可能的情况，则可能是NP完全问题
- 如果问题涉及序列(如旅行商问题中的城市序列)且难以解决，则可能是NP完全问题
- 如果问题涉及集合(如广播台集合)且难以解决，则可能是NP完全问题
- 如果问题可转换为集合覆盖问题或旅行商问题，则一定是NP完全问题

## 动态规划(Dynamic programming)
原理:先解决子问题，再逐步解决大问题  

局限:  
- 仅能考虑YesOrNo不能考虑部分
- 仅当每个子问题都是离散的，即不依赖于其他子问题时才可用
- 不可能包含两个以上的子背包

最长公共子串(最长的连续相同字符)与最长公共子序列(最多的相同字符)  
应用:
- DNA链的相似性
- git diff
- 编辑距离(levenshtein distance)
- 断字

## K最近邻算法(k-nearest neighbors algorithm)
特征提取:  
- 毕达哥拉斯公式计算距离
- 余弦相似度比较角度
应用:
- OCR(optical character recognition)
- spam email filter

## 其他

#### D&C
Divide and Conquer 分而治之

#### 并行算法(Parallel computing)
数个内核  
无法线性提速的原因:
- 并行性管理开销
- 负载均衡

#### 分布式算法(Distributed algorithm)
数百个内核  
MapReduce

#### 概率型算法(Probabilistic Algorithm)
常见的概率型算法有布隆过滤器(Bloom Filter)和HyperLogLog;  
布隆过滤器是一种概率型数据结构，可能出现错报的情况，但不可能出现漏报的情况;

#### SHA算法(secure hash algorithm)
局部不敏感  
目前最安全的密码散列函数为bcrypt  
应用:
- 比较文件
- 检查密码

#### 局部敏感的散列算法
Simhash  
对字符串做细微的修改，Simhash生成的散列值也只存在细微的差别  
应用:
- 检查两项内容的相似程度

#### Diffie-Hellman 密钥交换
使用两个密钥:公钥和私钥; 双方无需知道加密算法

#### 线性规划
Simplex算法  
用于在给定约束条件下最大限度地改善指定的指标








