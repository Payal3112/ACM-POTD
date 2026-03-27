class Solution {
    public void rotate(int[] nums, int k) {
    
        int n = nums.length;
        k = k % n; 

        reverse(nums, 0, n - 1); 
        
        reverse(nums, 0, k - 1);
        
        reverse(nums, k, n - 1);    
    }

    public void reverse(int[] nums, int start, int end) {
    
        while (start < end) {
        
            int temp = nums[start];
            
            nums[start] = nums[end];
            
            nums[end] = temp;
            
            start++;
            
            end--;
            
        }
    }
}


<img width="1898" height="846" alt="image" src="https://github.com/user-attachments/assets/b94647bf-eaf4-427d-9896-c0942b9a3f60" />
