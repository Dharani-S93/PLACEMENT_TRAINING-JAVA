## JAVA BASIC PROGRAMS
### EVEN AND ODD
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        for (int i = 1; i <= n; i++) {
            if (i % 2 == 0) {
                System.out.println(+i);
            }
        }
        for (int i = 1; i <= n; i++) {
            if (i % 2 != 0) {
                System.out.println(+i);
            }
        }
    }
}
```
**Input:**  
5

**Output:**  
2  
4  
1  
3  
5  

---

### FACTORIAL
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        int fact = 1;
        for (int i = 2; i <= n; i++) {
            fact = fact * i;
        }
        System.out.print(fact);
    }
}
```
**Input:**  
5

**Output:**  
120

---

### MULTIPLICATION TABLE
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        for (int i = 1; i <= 10; i++) {
            System.out.println(i + "X" + n + "=" + i * n);
        }
    }
}
```
**Input:**  
5

**Output:**  
1X5=5  
2X5=10  
3X5=15  
4X5=20  
5X5=25  
6X5=30  
7X5=35  
8X5=40  
9X5=45  
10X5=50

---

### REVERSE OF A NUMBER
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        int s1 = 0, rev = 1;
        while (n > 0) {
            rev = n % 10;
            s1 = s1 * 10 + rev;
            n = n / 10;
        }
        System.out.print(s1);
    }
}
```
**Input:**  
12345

**Output:**  
54321

---

### COUNT DIGITS IN A NUMBER
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        int count = 0;
        while (n > 0) {
            n = n / 10;
            count++;
        }
        System.out.print(count);
    }
}
```
**Input:**  
12345

**Output:**  
5

---

### SUM OF EVEN NUMBERS
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        int sum = 0;
        for (int i = 1; i <= n; i++) {
            if (i % 2 == 0) {
                System.out.println(+i);
                sum += i;
            }
        }
        System.out.println(sum);
    }
}
```
**Input:**  
5

**Output:**  
2  
4  
6

---

### PALINDROME NUMBER
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        int s1 = 0, rev = 1;
        int temp = n;
        while (n > 0) {
            rev = n % 10;
            s1 = s1 * 10 + rev;
            n = n / 10;
        }
        System.out.print(s1);
        if (s1 == temp) {
            System.out.println("PALINDROME");
        }
    }
}
```
**Input:**  
121

**Output:**  
121  
PALINDROME

## 01.  Check if a number is positive
## Code:
````java
import java.util.*; 

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        if (num > 0) {
            System.out.println("Positive Number");
        }
    }
}
````
### Output:
Input: 5
Output: Positive Number


## 02. If-Else Statement - Check if a number is positive or negative  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        if (num > 0) {
            System.out.println("Positive Number");
        } else {
            System.out.println("Negative Number");
        }
    }
}
```
### Output:  
**Input:** `-3`  
**Output:** `Negative Number`  

---

## 03. If-Else If-Else Statement - Find the largest of three numbers  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();
        int c = s.nextInt();
        if (a >= b && a >= c) {
            System.out.println(a + " is the largest");
        } else if (b >= a && b >= c) {
            System.out.println(b + " is the largest");
        } else {
            System.out.println(c + " is the largest");
        }
    }
}
```
### Output:  
**Input:** `7 2 5`  
**Output:** `7 is the largest`  

---

## 04. Nested If-Else Statement - Check whether a year is a leap year or not  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int year = s.nextInt();
        if (year % 4 == 0) {
            if (year % 100 == 0) {
                if (year % 400 == 0) {
                    System.out.println("Leap Year");
                } else {
                    System.out.println("Not a Leap Year");
                }
            } else {
                System.out.println("Leap Year");
            }
        } else {
            System.out.println("Not a Leap Year");
        }
    }
}
```
### Output:  
**Input:** `2024`  
**Output:** `Leap Year`  

---

## 05. Switch Case - Print the name of a day based on input number (1 to 7)  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int day = s.nextInt();
        switch (day) {
            case 1: System.out.println("Sunday"); break;
            case 2: System.out.println("Monday"); break;
            case 3: System.out.println("Tuesday"); break;
            case 4: System.out.println("Wednesday"); break;
            case 5: System.out.println("Thursday"); break;
            case 6: System.out.println("Friday"); break;
            case 7: System.out.println("Saturday"); break;
            default: System.out.println("Invalid Input");
        }
    }
}
```
### Output:  
**Input:** `3`  
**Output:** `Tuesday`  

---

## 06. Switch Case with String Input - Print corresponding day name using switch case  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String day = s.next().toLowerCase();
        switch (day) {
            case "sunday": System.out.println(1); break;
            case "monday": System.out.println(2); break;
            case "tuesday": System.out.println(3); break;
            case "wednesday": System.out.println(4); break;
            case "thursday": System.out.println(5); break;
            case "friday": System.out.println(6); break;
            case "saturday": System.out.println(7); break;
            default: System.out.println("Invalid Input");
        }
    }
}
```
### Output:  
**Input:** `Monday`  
**Output:** `2`  

---

## 07. Ternary Operator - Check whether a number is even or odd  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        System.out.println((num % 2 == 0) ? "Even Number" : "Odd Number");
    }
}
```
### Output:  
**Input:** `6`  
**Output:** `Even Number`  

---

## 08. Nested Switch Case - Print day name for weekday/weekend  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int day = s.nextInt();
        switch (day) {
            case 1: case 7:
                System.out.println("Weekend");
                break;
            default:
                switch (day) {
                    case 2: case 3: case 4: case 5: case 6:
                        System.out.println("Weekday");
                        break;
                    default:
                        System.out.println("Invalid Input");
                }
        }
    }
}
```
### Output:  
**Input:** `5`  
**Output:** `Weekday`  

---
## 09. If with Logical Operators - Check if a number is divisible by both 3 and 5  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        if (num % 3 == 0 && num % 5 == 0) {
            System.out.println("Divisible by both 3 and 5");
        } else {
            System.out.println("Not divisible by both 3 and 5");
        }
    }
}
```
### Output:  
**Input:** `15`  
**Output:** `Divisible by both 3 and 5`  

---

## 10. If with Relational Operators - Compare two numbers  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();
        if (a > b) {
            System.out.println(a + " is greater than " + b);
        } else if (a < b) {
            System.out.println(a + " is less than " + b);
        } else {
            System.out.println(a + " is equal to " + b);
        }
    }
}
```
### Output:  
**Input:** `8 10`  
**Output:** `8 is less than 10`  

---

## 11. Find Largest of Three Numbers Using If-Else  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();
        int c = s.nextInt();
        if (a >= b && a >= c) {
            System.out.println(a + " is the largest");
        } else if (b >= a && b >= c) {
            System.out.println(b + " is the largest");
        } else {
            System.out.println(c + " is the largest");
        }
    }
}
```
### Output:  
**Input:** `5 9 3`  
**Output:** `9 is the largest`  

---

## 12. Check Prime Number Using If-Else  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        boolean isPrime = num > 1;
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }
        System.out.println(isPrime ? "Prime Number" : "Not a Prime Number");
    }
}
```
### Output:  
**Input:** `7`  
**Output:** `Prime Number`  

---

## 13. Check Divisibility by 5 and 3 Using If  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        if (num % 5 == 0 && num % 3 == 0) {
            System.out.println("Divisible by 5 and 3");
        } else {
            System.out.println("Not Divisible by 5 and 3");
        }
    }
}
```
### Output:  
**Input:** `30`  
**Output:** `Divisible by 5 and 3`  

---

## 14. Check Positive or Negative Number Using Nested If  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        if (num != 0) {
            if (num > 0) {
                System.out.println("Positive Number");
            } else {
                System.out.println("Negative Number");
            }
        } else {
            System.out.println("Zero");
        }
    }
}
```
### Output:  
**Input:** `-5`  
**Output:** `Negative Number`  

---

## 15. Find Grade Using Switch Case  
### Code:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int marks = s.nextInt();
        switch (marks / 10) {
            case 10:
            case 9: System.out.println("Grade A"); break;
            case 8: System.out.println("Grade B"); break;
            case 7: System.out.println("Grade C"); break;
            case 6: System.out.println("Grade D"); break;
            case 5: System.out.println("Grade E"); break;
            default: System.out.println("Fail");
        }
    }
}
```
### Output:  
**Input:** `85`  
**Output:** `Grade B`  

