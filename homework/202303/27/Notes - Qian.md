# Sum of all paths in a binary tree

```
public List<List<Integer>> binaryTreePathSum(TreeNode root, int target) {
    List<List<Integer>> res = new ArrayList<>();
    if (root == null){
        return res;
    }
    ArrayList<Integer> path = new ArrayList<Integer>();
    dfs(root, target, path, res);
    return res;
}

private void dfs(TreeNode root, int target, ArrayList<Integer> path, List<List<Integer>> res) {
    if (root == null) {
        return;
    }
    
    path.add(root.val);
    if (root.left == null && root.right == null) {
        if (target == root.val) {
            res.add(new ArrayList<>(path));
        }
        path.remove(path.size() - 1);
        return;
    }
    
    dfs(root.left, target - root.val, path, res);
    dfs(root.right, target - root.val, path, res);
    path.remove(path.size() - 1);
}
```
