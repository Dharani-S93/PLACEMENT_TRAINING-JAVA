## DOUBLY LINKED LIST

````java
package Demo;

import java.util.*;

class Node{
    int data;
    Node next;
    Node prev;
    Node(int data){
        this.data=data;
        this.next=null;
        this.prev=null;
    }
}

class DL{
    Node head,tail,current;
    public void insertAtBegin(int data){
        Node newNode=new Node(data);
        if(head==null){
            head=tail=newNode;
        }
        else{
            newNode.next=head;
            head.prev=newNode;
            head=newNode;
        }
    }
    public void insetAtEnd(int data){
        Node newNode=new Node(data);
        if(tail==null){
            head=tail=newNode;
        }
        else {
            tail.next=newNode;
            newNode.prev=tail;
            tail=newNode;
            
        }
    }
    public void insertAtPos(int pos,int data){
        Node newNode=new Node(data);
		Node current=head;
        Node temp=null;
        for(int i=0;i<pos-1;i++) {
        	current =current.next;
        }
        	temp=current.next;
        	temp.prev=current;
        	current.next=newNode;
        	newNode.prev=current;
        	newNode.next=temp;
        	temp.prev=newNode;
        	
        }

    public void deleteAtBegin(){
        if(head==null)
        {
            System.out.println("List is Empty");
        }
        if(head==tail){//Delete the  Element in Beginning
        }
        else{
            head=head.next;
            head.prev=null;
        }
    }
   
    public void deleteAtEnd(){
        if(head==null)
        {
            System.out.println("List is Empty");
        }
        if(head==tail){                                   
            head=tail=null;
        }
        else{
            tail=tail.prev;
            tail.next=null;
        }
    }
    
    public void display()
    {
        Node temp=head;
        if(temp==null){
            System.out.println("LIST IS EMPTY");
        }
        while(temp!=null){
            System.out.println(temp.data);
            temp=temp.next;
        }

    }
    
}
public class DLL{
    public static void main(String[]args){
        DL link=new DL();
        link.insertAtBegin(100);
        link.insertAtBegin(200);
        link.insertAtBegin(300);
        link.insetAtEnd(400);
       link.insertAtPos(2, 250);
        link.display();
}
}
````

## INSERTION AND DELETION

````JAVA
package Demo;

import java.util.*;

class Node{
    int data;
    Node next;
    Node prev;
    Node(int data){
        this.data=data;
        this.next=null;
        this.prev=null;
    }
}

class DL{
    Node head,tail,current;
    public void insertAtBegin(int data){
        Node newNode=new Node(data);
        if(head==null){
            head=tail=newNode;
        }
        else{
            newNode.next=head;
            head.prev=newNode;
            head=newNode;
        }
    }
    public void insetAtEnd(int data){
        Node newNode=new Node(data);
        if(tail==null){
            head=tail=newNode;
        }
        else {
            tail.next=newNode;
            newNode.prev=tail;
            tail=newNode;
            
        }
    }
    public void insertAtPos(int pos,int data){
        Node newNode=new Node(data);
		Node current=head;
        Node temp=null;
        for(int i=0;i<pos-1;i++) {
        	current =current.next;
        }
        	temp=current.next;
        	temp.prev=current;
        	current.next=newNode;
        	newNode.prev=current;
        	newNode.next=temp;
        	temp.prev=newNode;
        	
        }

    public void deleteAtBegin(){
        if(head==null)
        {
            System.out.println("List is Empty");
        }
        if(head==tail){//Delete the  Element in Beginning
        }
        else{
            head=head.next;
            head.prev=null;
        }
    }
   
    public void deleteAtEnd(){
        if(head==null)
        {
            System.out.println("List is Empty");
        }
        if(head==tail){                                   
            head=tail=null;
        }
        else{
            tail=tail.prev;
            tail.next=null;
        }
    }
     public void deleteAtPos(int pos) {
    	 Node current=head;
         for(int i=0;i<pos;i++) {
         	current =current.next;
         }
     	
     	current.prev.next=current.next;
     	current.next.prev=current.prev;
         
    	 
     }
    public void display()
    {
        Node temp=head;
        if(temp==null){
            System.out.println("LIST IS EMPTY");
        }
        while(temp!=null){
            System.out.println(temp.data);
            temp=temp.next;
        }
        
    }
    
}
public class DLL{
    public static void main(String[]args){
        DL link=new DL();
        link.insertAtBegin(100);
        link.insertAtBegin(200);
        link.insertAtBegin(300);
        link.insetAtEnd(400);
       link.insertAtPos(2, 250);
       link. deleteAtPos(1);
        link.display();
}
}

````
## OUTPUT
300
250
100
400


### Reverse
 public void  reverse() {
    	 Node current=head;
    	 Node next=null;
    	 Node prev=null;
    	 while(current!=null) {
    		 next=current.next;
    		 current.next=prev;
    		 prev=current;
    		 current=next;
    		 
    	 }
    	 head=prev;
     }


### Search
````java
import java.util.*;
public class Main 
{
    static class DLLNode 
    {
        int data;
        DLLNode next;
        DLLNode prev;
        DLLNode(int data)
        {
            this.data = data;
            this.next = null;
            this.prev = null;
        }
    }
    static class DoublyLinkedList 
    {
        static DLLNode head = null;
        static DLLNode tail = null;
        void create_node(int num)
        {
            DLLNode newnode =  new DLLNode(num);
            if(head == null)
            {
                head = newnode;
                tail = newnode;
            }
            else
            {
                tail.next = newnode;
                newnode.prev = tail;
                tail = newnode;
            }
        }
        int search(int ele)
        {
          DLLNode temp=head;
          while(temp.next!=null){
          temp=temp.next;
          if(temp.data==ele){
            return 1;
          }
          }
          return 0;
    }
    }
    public static void main(String[] args) 
    {
        Scanner input = new Scanner(System.in);
        DoublyLinkedList DLL = new DoublyLinkedList();
        int num;
        while(true)
        {
            num = input.nextInt();
            if(num == -1) break;
            DLL.create_node(num);
        }
        int ele = input.nextInt();
        int res = DLL.search(ele);
        System.out.printf("%s",res==1 ? "Element Found" : "Element Not Found");
        input.close();
    }
}

````



