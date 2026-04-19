//fibonacci-numberclass Solution {
    public int fib(int n) {
        if (n == 0) return 0;  
        if (n == 1) return 1;  

        int a = 0; 
        int b = 1; 
        int c = 0; 

        for (int i = 2; i <= n; i++) {
            c = a + b; 
            a = b;     
            b = c;    
        }
        return c;
    }
}




<img width="1907" height="852" alt="image" src="https://github.com/user-attachments/assets/00f10ed0-b9e2-4ef9-bc4d-d7d1d1b48ca0" />
