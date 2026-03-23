2SUM

class Solution {

    public int[] twoSum(int[] nums, int target) {
    
        int n= nums.length;
        
        HashMap <Integer,Integer> map=new HashMap<> ();
        
        int res[]=new int [2];
        
        for(int i=0;i<n;i++){
        
            int rem= target-nums[i];
            
            if(map.containsKey(rem)){
            
                res[0]=i;
                
                res[1]=map.get(rem);
                
            }
            map.put(nums[i],i);
            
     }return res;
    }   
 
}

TimeComplexity=0(N);

Space Complexity=0(N);


<img width="1911" height="935" alt="image" src="https://github.com/user-attachments/assets/60eb68a8-4c8a-438a-9c3b-47f01d43a761" />
