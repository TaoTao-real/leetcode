<!--
 * @Author: your name
 * @Date: 2020-11-20 14:37:15
 * @LastEditTime: 2020-11-20 14:40:37
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 39. 数组中出现次数超过一半的数字.md
-->
```c++
class Solution {
public:
    int majorityElement(vector<int>& nums) {
        sort(nums.begin(), nums.end());
        return nums[nums.size()/2];
    }
};
```

```c++
class Solution {
public:
    int majorityElement(vector<int>& nums) {
        int cardcount = 1;
        int card = nums[0];
        for(int i = 1; i < nums.size(); ++i){
            if(cardcount == 0){
                card = nums[i];
                cardcount = 1;
            }else{
                if(card == nums[i]){
                    cardcount++;
                }else{
                    cardcount--;
                }
            }
        }
        return card;
    }
};
```