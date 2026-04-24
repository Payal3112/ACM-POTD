//house-robber


class Solution {
    public int rob(int[] nums) {
        int n = nums.length;
        if (n == 1) return nums[0];
        
        int[] dp = new int[n];
        dp[0] = nums[0];
        dp[1] = Math.max(nums[0], nums[1]);
        
        for (int i = 2; i < n; i++) {
            dp[i] = Math.max(dp[i-1], dp[i-2] + nums[i]);
        }
        
        return dp[n-1];
    }
}

<img width="1915" height="867" alt="image" src="https://github.com/user-attachments/assets/ad16759d-5e22-4785-873a-d9a5f81835b5" />
