# LC-Python21

## Theory of backtracking, 77. Combinations

June 13, 2023  4h

Congratulations!\
This is the 21sh day for leetcode python study. Today we will learn about the backtracking!\
The challenges today are about the theory of backtracking and how to use backtracking to solve combination problems. Similar to the 3 steps in recursion, backtracking will firstly use a for loop to build up the width of the tree structure, which is iterating through the elements in the original array. Then will use recursion to construct the depth of the tree.\
Branch cutting can help us to save the processing time.


## Theory of backtracking
[Reading link](https://github.com/youngyangyang04/leetcode-master/blob/master/problems/%E5%9B%9E%E6%BA%AF%E7%AE%97%E6%B3%95%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80.md)\
[video](https://www.bilibili.com/video/BV1cy4y167mM/?spm_id_from=pageDriver&vd_source=63f26efad0d35bcbb0de794512ac21f3)\
Backtracking come together with recursion, it's under the recursion function's logic. Backtracking can be used to solve questions such as combination, cut and palindrome, subset, arrangement mode, checkerboard...\
> void backtracking(variables) {\
>    if (termination condition) {collect results at leaf nodes; return;}\
>    for(size of the set/subtree of the node){process the node; recursion function; backtracking(revoke the operations on the node)}\
>    return }


##  77. Combinations
[leetcode](https://leetcode.com/problems/combinations/)\
The thing that needs to pay attention to is the **branch cutting**.\
Backtracking can control the layers of loop using recursion. The number of loops' layers are the number of recursion we need.\
All the results are in the leaf nodes.\
3 steps of backtracking is the same as recursion.
```python
# ways 1:
class Solution:
    def combine(self, n: int, k: int) -> List[List[int]]:
        result = []  
        self.backtracking(n, k, 1, [], result)
        return result
    def backtracking(self, n, k, startIndex, path, result):
        if len(path) == k:
            result.append(path[:])
            return  
        for i in range(startIndex, n + 1):  # layers of loop is n, width of the tree
        #for i in range(startIndex, n - (k - len(path)) + 2): branch cutting
            path.append(i)  # process the node
            self.backtracking(n, k, i + 1, path, result)    #depth of the tree
            path.pop()  # backtracking, undo the node proccessed
```









