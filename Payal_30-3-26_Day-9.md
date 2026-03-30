//LL Cycle 

public class Solution {

    public boolean hasCycle(ListNode head) {
      
    ListNode slow = head;
    
    ListNode fast = head;

    while(fast != null && fast.next != null){

        slow = slow.next;
        
        fast = fast.next.next;

        if(slow == fast){
        
            return true;
        }
    }

    return false;
}
        }

Time complexity=O(N);

Space Complexity= O(1);

<img width="1913" height="861" alt="image" src="https://github.com/user-attachments/assets/591c2471-4783-495a-a38f-43e2720f69eb" />

