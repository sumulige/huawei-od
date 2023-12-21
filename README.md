# 📝 华为OD算法记录

刷题进度：[![牛客网](https://img.shields.io/github/issues/sumulige/huawei-od?style=flat&label=%F0%9F%8C%B8%20牛客网%20Record&labelColor=%20%236DB9EF&color=%23FF90BC&link=https%3A%2F%2Fgithub.com%2Fsumulige%2Fhuawei-od
)](https://github.com/sumulige/huawei-od)

## 🎄 How to Use

❗ 请注意，不要在本项目下提交刷题记录，正确方法如下：

查看[Usage](Usage.md)文档，创建并使用一个个人专属的记录博客。

##  Issue 模板

-   给你一个二叉树的根节点 `root`， 检查它是否轴对称。
-   递归遍历+问题分解+分类讨论
    -   子结构: 两棵小树p和q, 同步遍历两棵树
    -   终止条件：p和q其中一方为空 或者 p 和 q不相等 return false
    -   否则: 递归判定: (左子树,右子树) (右子树,左子树)
```
class Solution {
public:
    //递归遍历+分类讨论:
    //子结构: 两棵小树p和q, 同步遍历两棵树
    //p和q其中一方为空 或者 p 和 q不相等 return false
    //否则: 递归判定: (左子树,右子树) (右子树,左子树)
    bool dfs(TreeNode *p, TreeNode *q){
        if(!p && !q) return true;
        if(p && q && p->val == q->val) return dfs(p->left, q->right) && dfs(p->right, q->left);
        return false;
    }
    bool isSymmetric(TreeNode* root) {
        if(!root) return true;
        return dfs(root->left, root->right);
    }
};
```

## 🎯 Calendar



* 2023/12

|Mon|Tue|Wed|Thu|Fri|Sat|Sun|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|27|28|29|30|1|2|3|
|4|5|6|7|8|9|10|
|11|12|13|14|15|16|17|
|18|19|20|21🌟|22|23|24|
|25|26|27|28|29|30|31|


## 🍃 Records

|#|Title|Tag|Date|
|:-:|:-:|:-:|:-:|
|1|[HJ1 字符串最后一个单词的长度](https://github.com/sumulige/huawei-od/issues/1)|`字符串`|2023-12-21T14:45:40Z|
