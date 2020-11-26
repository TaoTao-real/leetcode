<!--
 * @Author: your name
 * @Date: 2020-11-26 13:46:10
 * @LastEditTime: 2020-11-26 13:46:21
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /projects/leetcode/剑指 Offer 55 - II. 平衡二叉树.md
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
    int treeDeep(TreeNode* root){
        if(root == NULL) return 0;
        return max(treeDeep(root->left), treeDeep(root->right))+1;
    }
    bool isBalanced(TreeNode* root) {
        if(root == NULL) return true;
        return abs(treeDeep(root->left) - treeDeep(root->right)) <=1 && isBalanced(root->right) && isBalanced(root->left);
    }
};
```