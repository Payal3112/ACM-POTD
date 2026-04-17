//Diameter-of-binary-tree

class Solution {

    int diameter = 0;

    public int diameterOfBinaryTree(TreeNode root) {
        height(root);
        return diameter;
    }

    public int height(TreeNode node) {
        if (node == null) return 0;

        int left = height(node.left);
        int right = height(node.right);

        // update diameter
        diameter = Math.max(diameter, left + right);

        // return height
        return 1 + Math.max(left, right);
    }
}
<img width="1917" height="877" alt="image" src="https://github.com/user-attachments/assets/96c56fc7-fda5-4f94-85c9-cebd92e97fe4" />
