### BUBBLESORT

````JAVA
import java.util.*;

public class Main {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		int n = s.nextInt();
		int a[] = new int[n];
		for (int i = 0; i < n; i++) {
			a[i] = s.nextInt();
		}
		bubbleSort(a);
		for (int i = 0; i < n; i++) {
			System.out.print(a[i]);
		}
	}

	public static void bubbleSort(int a[]) {
		for (int i = 0; i < a.length; i++) {
			for (int j = 0; j < a.length - 1 - i; j++) {
				if (a[j] > a[j + 1]) {
					int temp = a[j];
					a[j] = a[j + 1];
					a[j + 1] = temp;
				}
			}
		}
	}
}
````

### OUTPUT
````
ENTER THE SIZE
5
ENTER ELEMENTS
9
5
2
7
1
SORTED ARRAY
1 2 5 7 9


````


