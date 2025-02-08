## JAVA COLLECTIONS

## ARRAYLIST PROGRAMS

### 1) TO SORT AN ARRAYLIST
````JAVA
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        ArrayList<Integer> set=new ArrayList<>();
        set.add(10);
        set.add(5);
        set.add(30);
        set.add(10);
        Collections.sort(set);
        System.out.println(set);
        
    }
}
````

### OUTPUT

after sorting
[5, 10, 10, 30]



## 2) MAX ELEMENT FROM ARRAYLIST
````JAVA
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        ArrayList<Integer> set=new ArrayList<>();
        set.add(10);
        set.add(5);
        set.add(30);
        set.add(10);
        System.out.println("MAXIMUM IS");
        System.out.println(Collections.max(set));
        
    }
}
````

### OUTPUT
MAXIMUM IS
30


