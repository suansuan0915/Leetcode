# Backtrack

[Guidance Link](https://labuladong.github.io/algo/4/31/105/)

## Recursion TC & SC
TC = # of nodes * TC(each recursion)\
SC = depth of recursion tree + SC(apply during recursion)

## Depth First Traversals
(a) Inorder (Left, Root, Right)\
(b) Preorder (Root, Left, Right)\
(c) Postorder (Left, Right, Root)

## Basic Frame
- keywords:\
path\
choice\
choice_list\
![image](https://user-images.githubusercontent.com/51430523/189400762-106c9c84-dc66-45cf-b83f-2e6b0bcd45ec.png)

```python
def backtrack(self, choice_list, path):
  for choice in choice_list:
    # can also set to used list [0]*n
    remove choice from choice_list
    path.append(choice)

    backtrack(choice_list, path)

    choice_list.append(choice)
    path.remove(choice)
```

