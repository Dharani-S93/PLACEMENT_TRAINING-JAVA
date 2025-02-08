### BINARY SEARCH


### CODE
````JAVA
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("ENTER THE SIZE");
        int n = sc.nextInt();
        System.out.println("ENTER THE ELEMENTS");
        int a[] = new int[n];

        for (int i = 0; i < n; i++) {
            a[i] = sc.nextInt();
        }
        System.out.println("TARGET");
            int key=sc.nextInt();
            int s=0;
            int e=n;
            int flag=0;
            
            while(s<=e){
                int mid=(s+e)/2;
            
            if(a[mid]==key){
                System.out.println("Element Found At Index   " +mid);
                flag=1;
                break;
            }
            else if(a[mid]<key){
                s=mid+1;
            }
            else{
                e=mid-1;
            }
            }
    
        if(flag==0){
            System.out.println("Element Not Found");
        }
    }
}

````

## OUTPUT

````
ENTER THE SIZE
5
ENTER THE ELEMENTS
1
2
3
4
5
TARGET
4
Element Found At Index   3

````

## LINEAR SEARCH

## CODE
````JAVA

import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("ENTER THE SIZE");
        int n = sc.nextInt();
        System.out.println("ENTER THE ELEMENTS");
        int a[] = new int[n];

        for (int i = 0; i < n; i++) {
            a[i] = sc.nextInt();
        }
        System.out.println("TARGET");
        int key=sc.nextInt();
        for(int i=0;i<n;i++){
            if(a[i]==key){
            System.out.println(i);
            
        }
        }
        }
    }


````

## OUTPUTT
````

ENTER THE SIZE
5
ENTER THE ELEMENTS
1
5
3
7
4
TARGET
3
INDEX
2

````
