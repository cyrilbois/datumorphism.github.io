---
title: "Data Structure: Tree"
excerpt: "mind the data structure: here comes the tree"
date: 2018-03-27
toc: true
category:
- 'Algorithms'
tag:
- 'Tree'
- 'Data Structure'
- 'Basics'
weight: 11
---


## BST: Binary Search Tree

1. Left sub-tree key <= parent node's key
2. Right sub-tree key >= parent node's key

Or

left sub-tree key <= node key <= right sub-tree key


### Validate


```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None


class Solution:
    def isValidBST(self, root):
        """
        :type root: TreeNode
        :rtype: bool
        """
        return self.BST(root, -2147483649, 2147483648)

    def BST(self, root, min, max):
        if root == None:
            return True
        if root.val <= min or root.val >= max:
            return False
        else
        return self.BST(root.left, min, root.val ) and self.BST(root.right, root.val, max)
```