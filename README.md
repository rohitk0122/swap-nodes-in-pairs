class Solution {
    public ListNode swapPairs(ListNode head) {
        ListNode temp = new ListNode(0);
        temp.next = head;
        ListNode returnhead = temp;

        while(temp.next!=null && temp.next.next!=null){
            ListNode curr = temp.next;
            ListNode nex = temp.next.next;
            temp.next = nex;
            curr.next = nex.next;
            nex.next = curr;
            temp = curr;
        }

        return returnhead.next;
        
    }
}
