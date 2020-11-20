<!--
 * @Author: your name
 * @Date: 2020-11-20 16:00:38
 * @LastEditTime: 2020-11-20 16:00:49
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/LCP 17. 速算机器人.md
-->
```c++
class Solution {
public:
    int calculate(string s) {
        int x = 1, y = 0;
        for(int i = 0; i < s.size(); ++i){
            if(s[i] == 'A'){
                x = 2*x+y;
            }else{
                y = 2*y+x;
            }
        }
        return x+y;
    }
};
```