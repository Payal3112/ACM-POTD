//Invert-binary-tree
class Solution {
    public TreeNode invertTree(TreeNode root) {
        if(root == null) return null;

        TreeNode temp = root.left;
        root.left = invertTree(root.right);
        root.right = invertTree(temp);

        return root;
    }
}

<img width="1903" height="902" alt="image" src="https://github.com/user-attachments/assets/5cb88a21-39b9-4e3e-b9b4-b2e2abb8e371" />
