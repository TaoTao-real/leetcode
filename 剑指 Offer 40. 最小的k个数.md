<!--
 * @Author: your name
 * @Date: 2020-11-20 14:35:28
 * @LastEditTime: 2020-11-20 14:35:36
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 40. 最小的k个数.md
-->
```c++
class Solution {
public:
    vector<int> getLeastNumbers(vector<int>& arr, int k) {
        sort(arr.begin(), arr.end());
        vector<int> res(arr.begin(), arr.begin()+k);
        return res;
    }
};
```