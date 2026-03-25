**Missing Number**

import java.util.Arrays;

class Solution {

    public int missingNumber(int[] nums) {
    
        int n=nums.length;
        
        Arrays.sort(nums);
        
        int no=0;
        
        for(int i=0;i<n;i++){
        
            if(nums[i]!=no){
            
                return no;

            }
            no++;
            
        }
        return n;
    }
}

Time complexity **=O(nlogn) +O(n)**

                sorting + checking loop  
                
Spcae complexity=**O(1)**

<img width="1896" height="866" alt="image" src="https://github.com/user-attachments/assets/f5419233-5a50-43fd-a748-217be4dea527" />


//Optimal appraoch 
**int no=sum-actual;**

<img width="1911" height="820" alt="image" src="https://github.com/user-attachments/assets/98e969d0-6aa0-4e3d-963c-2985959ff4e4" />

// Two Sum II - Input Array Is Sorted
class Solution {

    public int[] twoSum(int[] num, int target) {
    
        HashMap <Integer,Integer>map=new HashMap <>();
        int n=num.length;
        
        for(int i=0;i<n;i++){
        
            int no=target-num[i];
            
            if(map.containsKey(no)){
            
                return new int []  {map.get(no)+1,i+1};
}
            map.put(num[i],i);
        }
        return new int [] {0,0};

        
    }
}

Time complexity =**O(n)**

               
                
Spcae complexity=**O(n)**


<img width="1911" height="820" alt="image" src="https://github.com/user-attachments/assets/cfb6e5dc-db63-4bfd-ae27-02c67fe0f7dd" />





