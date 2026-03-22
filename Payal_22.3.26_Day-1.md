//Remove dublicate from the sorted array 

class Solution {
    public int removeDuplicates(int[] nums) {
     int i=0;
    int n=nums.length;
    for(int j=1;j<n;j++){
        if(nums[i]!=nums[j]){
            nums[i+1]=nums[j];
            i++;
            }
    }
    return i+1;
    }}

Time complexity=O(N)
Space Comlexity=O(1)

<img width="1902" height="865" alt="image" src="https://github.com/user-attachments/assets/7351ca54-cb83-4953-bf6a-280f8509b3c4" />
