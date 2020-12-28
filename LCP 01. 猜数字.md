/*
 * @Author: your name
 * @Date: 2020-12-28 19:40:43
 * @LastEditTime: 2020-12-28 19:40:57
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/LCP 01. 猜数字.cpp
 */
```c++
class Solution {
public:
    int game(vector<int>& guess, vector<int>& answer) {
        int res = 0;
        for(int i = 0; i < guess.size(); ++i){
            if(guess[i] == answer[i]){
                res++;
            }
        }
        return res;
    }
};
```