### FACTORIAL OF A NUMBER USING RECURION
````java
import java.util.*;
public class Main {

public static int factorial(int n){
    if(n<=1){
        return 1;
    }
    return n*factorial(n-1);
}


    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("ENTER");
        int n = sc.nextInt();
        System.out.println("FACTORIAL IS");
        System.out.println(factorial(n));
    }
}
````
### OUTPUT
````
ENTER
5
FACTORIAL IS
120
````java

### FIBANOCCI SERIES
````
import java.util.*;
public class Main {

public static int fibonacci(int n){
    if(n<=1){
        return n;
    }
    return fibonacci(n-1) +fibonacci(n-2);
}


    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("ENTER");
        int n= sc.nextInt();
        System.out.println("FIBONOCCI");
        for(int i=0;i<n;i++){
        System.out.println(fibonacci(i));
    }
}
}
````

### OUTPUT
````
ENTER
10
FIBONOCCI
0
1
1
2
3
5
8
13
21
34
````

### SUM OF N NUMBERS
````
import java.util.Scanner;

public class Main {
    public static int sum(int n) {
        if (n <= 1) {
            return n;
        }
        return n + sum(n - 1);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("ENTER N:");
        int n = sc.nextInt();
        System.out.println("SUM OF FIRST "  + sum(n));

    }
}
````

### REVERSING A NUMBER
````
    public class Main{
        static int sum=0;
        public static int reverse(int n){
            if(n==0){   // base case 
                return 0;
            }
            int temp=n%10;
            sum=sum*10+temp;
            reverse(n/10);
            return sum;// recursive 
        }
        
        public static void main(String[] args){
            int n = 12345;
            //for(int i=0;i<n;i++){
            System.out.println("reverse " + reverse(n));
            
        }
        
    }
}
````

## OUTPUT
````
reverse 54321
````
