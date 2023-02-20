## Binary Tree

:alarm_clock: Feb 20

[reference link](https://mp.weixin.qq.com/s?__biz=MzAxODQxMDM0Mw==&mid=2247496551&idx=1&sn=c6859fe37229a39e240a3b9323106bb4&scene=21#wechat_redirect)

Traverse Order:
- Pre-order
- In-order
- Post-order
(depends on where is *root*)

Two ways to solve:
- Traverse whole tree for once
- Decompose the question

Location:
- Pre-order (before going into a node)
- In-order (between jump from left to right subtree)
- Post-order (when about to leave a node)

![IMG_1369](https://user-images.githubusercontent.com/51430523/220160018-3f41bf56-0245-46ee-addc-9edcbefa437f.jpg)

Pre-order only has parent node's information, while post-order has subtree's information.
-> when it comes to "subtree's info", consider write code on post-order location.

"recursion in recursion" may not be optimized, then optimized it to be only O(N)
