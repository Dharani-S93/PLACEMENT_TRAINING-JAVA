
## **Approach:**

Today Problem Solving - 05.02.2025
Given a linked list and two integers M and N. Traverse the linked list such that you retain M nodes then delete next N nodes, continue the same till the end of the linked list. 
For example, an input of M = 2, N = 2 Linked List: 1->2->3->4->5->6->7->8 should return Linked List: 1->2->5->6

```java
import java.util.Scanner;

class LinkedList {
    static class Node {
        int data;
        Node next;
        
        Node(int data) {
            this.data = data;
            this.next = null;
        }
    }

    Node head;
    public void insert(int data) {
        Node newNode = new Node(data);
        if (head == null) {
            head = newNode;
            return;
        }
        Node temp = head;
        while (temp.next != null) {
            temp = temp.next;
        }
        temp.next = newNode;
    }
    public void retainAndDelete(int M, int N) {
        Node current = head;
        
        while (current != null) {
            for (int i = 1; i < M && current != null; i++) {
                current = current.next;
            }
            
            if (current == null) return; // If end reached
            
            Node temp = current.next;
            for (int i = 0; i < N && temp != null; i++) {
                temp = temp.next;
            }
                        current.next = temp;
            current = temp;
        }
    }

    public void display() {
        Node temp = head;
        while (temp != null) {
            System.out.print(temp.data + " -> ");
            temp = temp.next;
        }
        System.out.println("NULL");
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        LinkedList list = new LinkedList();

        System.out.println("Enter number of elements in the linked list:");
        int n = scanner.nextInt();
        
        System.out.println("Enter elements:");
        for (int i = 0; i < n; i++) {
            list.insert(scanner.nextInt());
        }

        System.out.println("Enter M (retain count):");
        int M = scanner.nextInt();
        System.out.println("Enter N (delete count):");
        int N = scanner.nextInt();

        System.out.println("Original Linked List:");
        list.display();

        list.retainAndDelete(M, N);

        System.out.println("Modified Linked List:");
        list.display();

        scanner.close();
    }
}
```
---

#### **Input:**
```
Enter number of elements in the linked list:
8
Enter elements:
1 2 3 4 5 6 7 8
Enter M (retain count):
2
Enter N (delete count):
2
```
#### **Output:**
```
Original Linked List:
1 -> 2 -> 3 -> 4 -> 5 -> 6 -> 7 -> 8 -> NULL
Modified Linked List:
1 -> 2 -> 5 -> 6 -> NULL
```

---

