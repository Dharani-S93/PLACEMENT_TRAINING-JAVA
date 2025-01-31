## Stack in java

````java
package dharuu;


class Stack{
	int a[]=new int[5];
	int top=-1;

public void push(int data) {
	if(top==a.length-1) {
		System.out.println("OVERFLOWW");
	}
	else {
		top++;
		a[top]=data;
	}
}

public void pop() {
	if(top==-1) {
		System.out.println("UNDERFLOWW");
	}
	else {
		top--;
	}
}

public void peek() {
	if(top==-1) {
		System.out.println("UNDERFLOWW");
	}
	else {
		System.out.println(a[top]);
}
}
	
	public void display() {
		for(int i=top;i>=0;i--) {
			System.out.println(a[i]);
		}
	}
	
}
public class Main {

	public static void main(String[] args) {
      Stack s=new Stack();
      s.push(100);
      s.push(200);
      s.push(300);
      s.push(400);
      s.push(500);
      s.pop();
      s.peek();
      s.display();
	}

}
````
## OUTPUT
400-------it is the top most element
elements after pop
400
300
200
100
