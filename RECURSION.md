### FACTORIAL OF A NUMBER USING RECURION
````
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
````

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
