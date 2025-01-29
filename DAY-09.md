## LINKED LIST IN JAVA
## SINGLY LINKED LIST
## INSERT AT BEGINING AND END

# Code
````[JAVA]
import java.util.*;
// Create a class Node
class Node{
    int data;
    Node next;
    // Create a constructor
    Node(int data){
        this.data = data;
        this.next = null;
    }
}

// LinkedList class
class LinkedList{
    Node head, tail;
    public void insert(int data){
        Node newNode = new Node(data);
        if(head == null){
            head = newNode;
            tail = newNode;
        } else {
            tail.next = newNode;
            tail = newNode;
        }
    }
    public void display(){
        Node temp = head;
        while(temp != null){  
            System.out.println(temp.data);  
            temp = temp.next;
        }
    }
    public void insertAtBegin(int data){
        Node newNode = new Node(data);
        newNode.next = head;
        head = newNode;
    }
}


public class Main {
    public static void main(String[] args) {
        LinkedList link = new LinkedList();
        link.insert(100);
        link.insert(200);
        link.insert(300);
        link.display();
        System.out.println("INSERT AT BEGINNING");
        link.insertAtBegin(400);
        link.display();
    }
}

# OUTPUT
100
200
300
INSERT AT BEGINNING
400
100
200
300
...

````[JAVA]

