//climbing-stairs

class Solution {
    public int climbStairs(int n) {
        if(n == 1) return 1;
        
        int prev2 = 1; 
        int prev1 = 2; 
        
        for(int i = 3; i <= n; i++){
            int curr = prev1 + prev2;
            prev2 = prev1;
            prev1 = curr;
        }
        
        return prev1;
    }
}

<img width="1913" height="898" alt="image" src="https://github.com/user-attachments/assets/36aede3c-1a93-4e63-a8df-64c15f538488" />
