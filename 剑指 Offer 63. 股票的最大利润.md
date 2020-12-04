<!--
 * @Author: your name
 * @Date: 2020-12-04 12:54:06
 * @LastEditTime: 2020-12-04 12:54:43
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 63. 股票的最大利润.md
-->
```c++
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        if(prices.size() <= 1) return 0;
        vector<int> benifit;
        for(int i = 1; i < prices.size(); ++i){
            benifit.push_back(prices[i]-prices[i-1]);
        }
        int maxbenifit = benifit[0];
        for(int i = 1; i < benifit.size(); ++i){
            if(benifit[i-1] > 0){
                benifit[i] += benifit[i-1];
            }
            if(benifit[i] > maxbenifit) maxbenifit = benifit[i];
        }
        return maxbenifit<0?0:maxbenifit;
    }
};
```