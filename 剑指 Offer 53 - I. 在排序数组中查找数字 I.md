<!--
 * @Author: your name
 * @Date: 2020-12-04 13:02:52
 * @LastEditTime: 2020-12-04 13:03:00
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 53 - I. 在排序数组中查找数字 I.md
-->
```c++
class Solution {
public:
    int search(vector<int>& nums, int target) {
        return upper_bound(nums.begin(), nums.end(), target) - nums.begin() - (lower_bound(nums.begin(), nums.end(), target)-nums.begin());
    }
};
```