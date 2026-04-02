//remove dublicate from LL

class Solution {

    public ListNode deleteDuplicates(ListNode head) {
        
        ListNode temp = head;

        while(temp != null && temp.next != null){
            
            if(temp.val == temp.next.val){
            
                temp.next = temp.next.next;   // remove duplicate
            }
            else{
                temp = temp.next;             // move forward
            }
        }

        return head;
    }
}

Time Complexity: O(n)

Space Complexity: O(1)

<img width="1896" height="853" alt="image" src="https://github.com/user-attachments/assets/8bd12b10-6ce8-45bd-af37-5e436dfea12b" />

