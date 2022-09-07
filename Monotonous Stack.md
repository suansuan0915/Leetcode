# Monotonous Stack

[Useful Link](https://mp.weixin.qq.com/s?__biz=MzAxODQxMDM0Mw==&mid=2247497113&idx=1&sn=36517e8b999d6da6e2042c1f03f9e8e2&scene=21#wechat_redirect)

### attention
- subset (not necessarily consecutive) != subarray (consecutive)
- if xxx vs. if xxx is not None\
[link](https://stackoverflow.com/questions/3901144/difference-between-if-x-and-if-x-is-not-none)\
false, 0, None -> `if xxx` #False  `if not xxx`\
is -> test for identity/memory location. `id(test) == id(None) #False`  equals to  `test is not None`

### Basic - Find Next Closest Larger Number
![image](https://user-images.githubusercontent.com/51430523/188715024-e58de521-804b-4be4-8a29-236b5fc425e7.png)
- code\
![IMG_1347](https://user-images.githubusercontent.com/51430523/188728454-c5749939-57dd-4556-b915-8079b45b1a5f.jpg)
```python
n = len(nums)
ans = [0] * n  # coz we get ans from end to start 
s = list()  # monotonous stack for nextLarger# (so keep increasing trend)

for i in range(n-1, -1, -1):
    while s is not None and nums[i] >= s[-1]:
        s.pop()
    ans[i] = -1 if s is None else s[-1]
    s.append(nums[i])

return ans
```

### 496. Next Greater Element I
easy\
[Link](https://leetcode.com/problems/next-greater-element-i/)
