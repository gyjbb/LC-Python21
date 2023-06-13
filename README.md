# LC-Python21

## Theory of backtracking

June 13, 2023  4h

Congratulations!\
This is the 21th day for leetcode python study. Today we will learn more about the backtracking!\
The challenges today are about ~~need to delete later~~.


## Theory of backtracking
[Reading link](https://github.com/youngyangyang04/leetcode-master/blob/master/problems/%E5%9B%9E%E6%BA%AF%E7%AE%97%E6%B3%95%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80.md)\
[video](https://www.bilibili.com/video/BV1cy4y167mM/?spm_id_from=pageDriver&vd_source=63f26efad0d35bcbb0de794512ac21f3)\
Backtracking come together with recursion, it's under the recursion function's logic. Backtracking can be used to solve questions such as combination, cut and palindrome, subset, arrangement mode, checkerboard...\
> void backtracking(variables) {\
>    if (termination condition) {collect results at leaf nodes; return;}\
>    for(size of the set/subtree of the node){process the node; recursion function; backtracking(revoke the operations on the node)}\
>    return }


##  77. 
组合
对着 在 回溯算法理论基础 给出的 代码模板，来做本题组合问题，大家就会发现 写回溯算法套路。
在回溯算法解决实际问题的过程中，大家会有各种疑问，先看视频介绍，基本可以解决大家的疑惑。
本题关于剪枝操作是大家要理解的重点，因为后面很多回溯算法解决的题目，都是这个剪枝套路。 
