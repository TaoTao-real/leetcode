<!--
 * @Author: your name
 * @Date: 2020-12-01 12:22:28
 * @LastEditTime: 2020-12-01 12:24:12
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 59 - I. 滑动窗口的最大值.md
-->
```c++
class Solution {
public:
    vector<int> maxSlidingWindow(vector<int>& nums, int k) {
        vector<int> res;
        if(nums.size() == 0) return res;
        for(int i = 0; i <= nums.size() - k; ++i){
            int max = INT_MIN;
            for(int j = i; j < i + k; ++j){
                if(nums[j] > max) max = nums[j];
            }
            res.push_back(max);
        }
        return res;
    }
};
```