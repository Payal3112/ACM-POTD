// Best Time to Buy and Sell Stock

class Solution {

    public int maxProfit(int[] prices) {
        
        int n=prices.length;
    
        int mini=prices[0];
        int cost=0;
        
        if(n==0){return 0;}
        
        for(int i=1;i<n;i++){
        
            int profit = prices[i]-mini;

            cost=Math.max(profit,cost);
            
            mini=Math.min(mini,prices[i]);
            
        }
      
     return cost;   
     
    }
}


Time complexity =0(N)

Space Complexity=0(1)

<img width="1907" height="857" alt="image" src="https://github.com/user-attachments/assets/7415cb84-b661-4727-9dae-8f72948bf9e7" />
