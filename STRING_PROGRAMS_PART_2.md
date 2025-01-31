## date-29/01/2025
````java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        System.out.println("Print the statement: " + s1.toUpperCase());
    }
}
output
Print the statement: HELLO
````
````java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        System.out.print("Enter a character: ");
        String sc = s.next();  
           if (sc.matches("[a-zA-Z]+")) {
               System.out.println("Alphabet");
        } 
        else {
            System.out.println("Not an Alphabet");
        }

    }
}
Enter a character: dharuu
Alphabet
````

````java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        System.out.print("Enter Selling Price and Cost Price: ");
        int sp = s.nextInt();
        int cp = s.nextInt();

        if (sp > cp) {
            System.out.println("PROFIT: " + (sp - cp)); 
        } 
        else if (cp > sp) {
            System.out.println("LOSS: " + (cp - sp)); 
        } 
        else {
            System.out.println("NO PROFIT NO LOSS");
        }

       
    }
}
````
