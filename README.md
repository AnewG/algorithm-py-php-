algorithm [ python 实现 ] - PEP8
=================

 * insert sort 
 * merge sort (sub)
 * random list
 * heap sort
 * quick sort
 * counting sort
 * radix sort

 * linked list

=================

红黑树

黑树虽然本质上是一棵二叉查找树，但它在二叉查找树的基础上增加了着色和相关的性质使得红黑树相对平衡，从而保证了红黑树的查找、插入、删除的时间复杂度最坏为O(log n)。

当在对红黑树进行插入和删除等操作时，对树做了修改可能会破坏红黑树的性质。为了继续保持红黑树的性质，可以通过对结点进行重新着色，以及对树进行相关的旋转操作，即通过修改树中某些结点的颜色及指针结构，来达到对红黑树进行插入或删除结点等操作后继续保持它的性质或平衡的目的。

MySQL Index B+Tree ：http://blog.codinglabs.org/articles/theory-of-mysql-index.html
http://blog.csdn.net/v_july_v/article/details/6530142

MySQL MyISAM Innodb：http://blog.csdn.net/php10086/article/details/6334164

动态规划

```
CUT-ROD(p,n) // p为价格数组 p[1..n],n为长度
  if n==0
    return 0
  q=-oo
  for i = i to n
    q=max(q,p[i]+CUT-ROD(p,n-i))
  return q
```

这种情况将反复地用相同的参数对自身进行递归调用，即反复求解相同的子问题

假设n＝4

```
        4
     /  \  \ \    
    3    2  1 0
  / \\  /\  |  
 2  1 0 1 0 0
/\  |   |
1 0 0   0
|
0
```
