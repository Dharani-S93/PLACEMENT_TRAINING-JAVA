## QUEUE-ARRAY_IMPLEMENTATION

````java
package dharuu_Queue;

class Queue{
	int a[]=new int[5];
	int front=-1;
	int rear=-1;

public void Enqueue(int data) {
	if(rear>=a.length-1) {
		System.out.println("queue is full");
	}
	else {
		if(front==-1) {
			front=0;
		}
		rear++;
		a[rear]=data;
	}
}

public void Deque() {
	if(front==-1 || front >rear) {
		System.out.println("queue is empty");
	}
		else {
		front++;
		
	}
}
	public void display() {
		for(int i=front;i<=rear;i++) {
			System.out.println(a[i]);
		}
	}
	
}
public class Main {

	public static void main(String[] args) {
      Queue s=new Queue();
      s.Enqueue(100);
      s.Enqueue(200);
      s.Enqueue(300);
      s.Enqueue(400);
      s.Enqueue(500);
      s.Deque();
      s.display();
	}

}
````

## OUTPUT
200
300
400
500
