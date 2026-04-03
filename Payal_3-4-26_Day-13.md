//Intersection of 2 LL

public class Solution {

    public ListNode getIntersectionNode(ListNode headA, ListNode headB) {

        ListNode pA = headA;
        
        ListNode pB = headB;

        while(pA != pB){

            if(pA == null){
            
                pA = headB;
                
            }else{
            
                pA = pA.next;
            }

            if(pB == null){
            
                pB = headA;
                
            }else{
            
                pB = pB.next;
            }
        }

        return pA;
    }
}

<img width="1902" height="855" alt="image" src="https://github.com/user-attachments/assets/11f67539-933d-46a1-999d-f7057c943cb7" />
