<!--
 * @Author: your name
 * @Date: 2020-11-24 14:55:07
 * @LastEditTime: 2020-11-24 14:55:19
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 47. 礼物的最大价值.md
-->
```c++
class Solution {
public:
    int dp[205][205] = {0};
    int maxv(vector<vector<int>>& grid, int starti, int startj){
        if(dp[starti][startj] != 0) return dp[starti][startj];
        if(starti == grid.size()-1&&startj == grid[0].size()-1){
            dp[grid.size() - 1][grid[0].size() - 1] = grid[grid.size() - 1][grid[0].size() - 1];
        }else if(starti == grid.size() - 1){
            dp[starti][startj] =  maxv(grid, starti, startj+1) + grid[starti][startj];
        }else if(startj == grid[0].size() - 1){
            dp[starti][startj] = maxv(grid, starti+1, startj) + grid[starti][startj];
        }else{
            dp[starti][startj] = max(maxv(grid, starti+1, startj), maxv(grid, starti, startj+1)) + grid[starti][startj];
        }
        return dp[starti][startj];
    }
    int maxValue(vector<vector<int>>& grid) {
        return maxv(grid, 0, 0);
    }
};
```