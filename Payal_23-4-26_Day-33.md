//min-cost-climbing-stairs

class Solution {
    public int minCostClimbingStairs(int[] cost) {
        int prev2 = 0; // cost to reach step i-2
        int prev1 = 0; // cost to reach step i-1
        
        for (int i = 0; i < cost.length; i++) {
            int curr = cost[i] + Math.min(prev1, prev2);
            prev2 = prev1;
            prev1 = curr;
        }
        
        return Math.min(prev1, prev2);
    }
}

<img width="1897" height="862" alt="image" src="https://github.com/user-attachments/assets/3d7f3e4c-8ce6-41a5-ae9c-6e3535d52850" />
