//19. Remove Nth Node From End of List

class Solution {

    public ListNode removeNthFromEnd(ListNode head, int n) {
    
        int length = 0;
        
        ListNode temp = head;
        
         while (temp != null) {
         
            length++;
            
            temp = temp.next;
        }
        if (length == n) {
        
            return head.next;
        }

        temp = head;
        
        for (int i = 1; i < length - n; i++) {
        
            temp = temp.next;
        }

        temp.next = temp.next.next;

        return head;
    }
}



<img width="1896" height="847" alt="image" src="https://github.com/user-attachments/assets/0eed09e2-d906-44f2-94bf-12dd645af573" />
