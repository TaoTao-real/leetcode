<!--
 * @Author: your name
 * @Date: 2020-11-28 21:50:27
 * @LastEditTime: 2020-11-28 21:50:39
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 28. 对称的二叉树.md
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
    bool dfs(TreeNode* left, TreeNode* right){
        if(left==NULL && right==NULL){
            return true;
        }else if(left!=NULL && right!=NULL){
            if(left->val == right->val) return true&&dfs(left->left,right->right)&&dfs(left->right,right->left);
            else return false;
        }else{
            return false;
        }
    }
    bool isSymmetric(TreeNode* root) {
        if(root == NULL) return true;
        return dfs(root->left, root->right);
    }
};
```