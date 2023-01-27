## Binary Heap 二叉堆

:alarm_clock: Jan 27

[Link](https://mp.weixin.qq.com/s?__biz=MzAxODQxMDM0Mw==&mid=2247484495&idx=1&sn=bbfeba9bb5cfd50598e2a4d08c839ee9&scene=21#wechat_redirect)

*Complete* binary heap.

Similar to binary tree, but instead of using node as pointers and stored in tree, \
binary heap is stored in array, uses index as pointers.

![image](https://user-images.githubusercontent.com/51430523/215194038-1213ecfb-63a1-487b-9686-1e74ca4b1999.png)

### Heap Data Structure

Always maintain the structure and characteristics, whenever elements are pushed or popped.

- **Max Heap**\
all nodes are larger than their child nodes.
- **Min Heap**

### Binary heap Operations
`swim()`\
`sink()`

## Priority Queue
based on binary heap
- operations\
`insert` TC: O(log N)\
`delMax` or `delMin` TC: O(log N)\
`heapify`\
`peek`

## Python library
*heapq* module  ->  min heap\
`import heapq`

`heapq.heapify()`\
insert: `heappush(heap, ele)`\
pop min and return it: `heappop(heap)`\
push and pop: `heappushpop(heap, ele)`\
pop min and push, then return original min: `heapreplace(heap, ele)`\
Find the largest and smallest elements from Heap:\
`nlargest(k, iterable, key = fun)`\
`nsmallest(k, iterable, key = fun)`
