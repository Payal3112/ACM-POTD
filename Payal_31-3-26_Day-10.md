//Middle of the LL

class Solution {

    public ListNode middleNode(ListNode head) {

        ListNode slow=head;
        
        ListNode fast= head;
        
        while(fast!=null && fast.next!=null){
        
            slow=slow.next;
            
            fast=fast.next.next;

 }
        return slow;
 }
}
//Time Complexity= O(N/2);
//Space Complexity = O(1)

<img width="1911" height="871" alt="image" src="https://github.com/user-attachments/assets/0b0a0128-39dd-4557-91db-0e0a2b9dbabc" />
