<!--
 * @Author: your name
 * @Date: 2020-11-28 19:13:46
 * @LastEditTime: 2020-11-28 19:13:56
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 38. 字符串的排列.md
-->
```c++
class Solution {
public:
    vector<string> permutation(string s) {
        vector<string> res;
        res.push_back(s);
        string temp = s;
        next_permutation(s.begin(), s.end());
        while(temp != s){
            res.push_back(s);
            next_permutation(s.begin(), s.end());
        }
        return res;
    }
};
```