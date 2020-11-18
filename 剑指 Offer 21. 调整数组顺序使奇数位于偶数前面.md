<!--
 * @Author: your name
 * @Date: 2020-11-18 19:06:20
 * @LastEditTime: 2020-11-18 19:06:22
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 21. 调整数组顺序使奇数位于偶数前面.md
-->
class Solution {
public:
    bool static cmp(int a, int b){
        return a%2 > b%2;
    }
    vector<int> exchange(vector<int>& nums) {
        sort(nums.begin(), nums.end(), cmp);
        return nums;
    }
};