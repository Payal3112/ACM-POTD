Maximum Depth of Binary Tree

class Solution {
    public int maxDepth(TreeNode root) {
        
        if(root == null){
            return 0;
        }

        int left = maxDepth(root.left);
        int right = maxDepth(root.right);

        return 1 + Math.max(left, right);
    }
}

<img width="1907" height="868" alt="image" src="https://github.com/user-attachments/assets/69cc0bf6-021b-4fd3-9e10-07b5de643079" />
