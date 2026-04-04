//Palindrom in LL

class Solution {
    public boolean isPalindrome(ListNode head) {
        
        ListNode slow = head, fast = head;
        while (fast != null && fast.next != null) {
            slow = slow.next;
            fast = fast.next.next;
        }
       
        ListNode reversedSecondHalf = reverse(slow);
        
       
        ListNode firstHalf = head;
        while (reversedSecondHalf != null) {
            if (firstHalf.val != reversedSecondHalf.val) {
                return false;
            }
            firstHalf = firstHalf.next;
            reversedSecondHalf = reversedSecondHalf.next;
        }
        
        return true;
    }
    
    private ListNode reverse(ListNode head) {
        ListNode prev = null, curr = head;
        while (curr != null) {
            ListNode nextNode = curr.next;
            curr.next = prev;
            prev = curr;
            curr = nextNode;
        }
        return prev;
    }
}

<img width="1918" height="860" alt="image" src="https://github.com/user-attachments/assets/a8982c25-a3e8-446f-910f-79443ae8ff7d" />
