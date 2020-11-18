<!--
 * @Author: your name
 * @Date: 2020-11-18 19:08:59
 * @LastEditTime: 2020-11-18 19:08:59
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/LCP 06. 拿硬币.md
-->
class Solution {
public:
    int minCount(vector<int>& coins) {
        int count = 0;
        for(int i : coins){
            if(i%2) count+=i/2+1;
            else count+=i/2;
        }
        return count;
    }
};