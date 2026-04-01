//SORT LL 
class Solution {
    public ListNode sortList(ListNode head) {

        if(head == null || head.next == null){
            return head;
        }

        ListNode middle = findMiddle(head);
        ListNode right = middle.next;
        middle.next = null;

        ListNode left = head;

        left = sortList(left);
        right = sortList(right);

        return mergeTwoLL(left, right);
    }

    ListNode mergeTwoLL(ListNode list1, ListNode list2){

        ListNode dummyNode = new ListNode(-1);
        ListNode temp = dummyNode;

        while(list1 != null && list2 != null){

            if(list1.val < list2.val){
                temp.next = list1;
                list1 = list1.next;
            }
            else{
                temp.next = list2;
                list2 = list2.next;
            }

            temp = temp.next;
        }

        if(list1 != null){
            temp.next = list1;
        }
        else{
            temp.next = list2;
        }

        return dummyNode.next;
    }

    ListNode findMiddle(ListNode head){

        ListNode slow = head;
        ListNode fast = head.next;

        while(fast != null && fast.next != null){
            slow = slow.next;
            fast = fast.next.next;
        }

        return slow;
    }
}

<img width="1910" height="846" alt="image" src="https://github.com/user-attachments/assets/b8750d75-e599-4db3-9eb0-7b4d439e33c5" />

 
