<!--
 * @Author: your name
 * @Date: 2020-11-23 11:31:33
 * @LastEditTime: 2020-11-23 11:31:42
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 64. 求1+2+…+n.md
-->
```c++
class Solution {
public:
    int sumNums(int n) {
        n && (n+=sumNums(n-1));
        return n;
    }
};
```