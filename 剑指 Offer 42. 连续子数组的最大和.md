<!--
 * @Author: your name
 * @Date: 2020-11-29 22:45:30
 * @LastEditTime: 2020-11-29 22:45:41
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 42. 连续子数组的最大和.md
-->
```c++
class Solution {
public:
    int maxSubArray(vector<int>& nums) {
        int pre = 0;
        int res = INT_MIN;
        int n = nums.size();
        for(int i = 0; i < n; ++i){
            dp[i+1] = max(dp[i]+nums[i], nums[i]);
            if(dp[i+1] > res) res = dp[i+1];
        }
        return res;
    }
};
```