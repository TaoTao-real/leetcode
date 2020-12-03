<!--
 * @Author: your name
 * @Date: 2020-12-03 21:47:52
 * @LastEditTime: 2020-12-03 21:48:08
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 54. 二叉搜索树的第k大节点.md
-->
```c++
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    vector<int> res;
    void lmr(TreeNode* root){
        if(root == NULL) return;
        lmr(root->left);
        res.push_back(root->val);
        lmr(root->right);
    }
    int kthLargest(TreeNode* root, int k) {
        lmr(root);
        return res[res.size()-k];
    }
};
```