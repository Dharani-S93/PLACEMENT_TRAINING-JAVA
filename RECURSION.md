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
