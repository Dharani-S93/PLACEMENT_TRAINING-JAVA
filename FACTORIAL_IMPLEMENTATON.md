## Problem Statement for the day - 03.02.2025
## Given  two integers M and N, calculate the  sum of the factorials of all the integers from M and N inclusive* .if M is greater than N , return 0 or display an appropriate message.
````
Test Case 01 : M = 3, N = 5
Test Case 02 : M = 0, N = 4
Test Case 03 : M = 5, N = 5
Test Case 04 : M = 6, N = 4

````
```java

import java.util.Scanner;

public class FactorialSum {
    public static long factorial(int num) {
        long fact = 1;
        for (int i = 1; i <= num; i++) {
            fact *= i;
        }
        return fact;
    }
    public static long sumOfFactorials(int M, int N) {
        if (M > N) {
            System.out.println("Invalid input");
            return 0;
        }
        long sum = 0;
        for (int i = M; i <= N; i++) {
            sum += factorial(i);
        }
        return sum;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter M: ");
        int M = scanner.nextInt();
        System.out.print("Enter N: ");
        int N = scanner.nextInt();
        scanner.close();

        long result = sumOfFactorials(M, N);
        System.out.println("Sum of factorials from " + M + " to " + N + " is: " + result);
    }
}
```

## OUTPUT
````
Enter M: 24
Enter N: 65
Sum of factorials from 24 to 65 is: -4183792028426960896
````
