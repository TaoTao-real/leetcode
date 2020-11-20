<!--
 * @Author: your name
 * @Date: 2020-11-20 15:58:02
 * @LastEditTime: 2020-11-20 15:58:32
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 59 - II. 队列的最大值.md
-->
```c++
class MaxQueue {
public:
    deque<int> q;
    MaxQueue() {
        
    }
    int max_value() {
        if(q.empty()) return -1;
        int maxone = -1;
        for(int i= 0; i < q.size(); ++i){
            if(q[i]>maxone) maxone = q[i];
        }
        return maxone;
    }
    
    void push_back(int value) {
        q.push_back(value);
    }
    
    int pop_front() {
        if(q.empty()) return -1;
        else{
            int temp = q.front();
            q.pop_front();
            return temp;
        }
    }
};

/**
 * Your MaxQueue object will be instantiated and called as such:
 * MaxQueue* obj = new MaxQueue();
 * int param_1 = obj->max_value();
 * obj->push_back(value);
 * int param_3 = obj->pop_front();
 */
```