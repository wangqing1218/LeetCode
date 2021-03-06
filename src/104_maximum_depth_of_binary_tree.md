## Maximum Depth of Binary Tree


### Description

```Python
Given a binary tree, find its maximum depth.

The maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.

Note: A leaf is a node with no children.

Example:

Given binary tree [3,9,20,null,null,15,7],

    3
   / \
  9  20
    /  \
   15   7
return its depth = 3.
```

### Python Solutions

#### Approach : Recursive

* Time complexity : O(n)
* Space complexity : O(n)


```Python
class Solution(object):
    def max_depth(self, root):
        """
        Given a binary tree, find its maximum depth

        Args:
            root(TreeNode): The root of tree
        
        Returns:
            The maximum depth of the tree(int)
        """
        return 1 + max(map(self.maxDepth, (root.left, root.right))) if root is not None else 0
```

