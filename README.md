# count_linkedNode

package elclipse;

public class Linkedlist {

	public static class ListNode{
		private int data;
		private ListNode next;

		public ListNode(int data) {
			this.data=data;
		}
	}

	public static int count(ListNode head) {
		int count=0;                                           ////Initializing count
		ListNode current=head;
		if(head==null) {
			return -1;
		}
		while(current!=null) {
			count++;
			current=current.next;
		}
		return count;                                          ////returning count
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		ListNode  head=new ListNode(1);
		ListNode  second=new ListNode(2);
		ListNode  third=new ListNode(3);
		ListNode  fourth=new ListNode(4);
		ListNode  fifth=new ListNode(5);

		head.next=second;
		second.next=third;
		third.next=fourth;
		fourth.next=fifth;
		Linkedlist linked=new Linkedlist();
		int c=linked.count(head);                             ////storing count in c variable
		System.out.print(c);                                 ////printing count
	}

}
