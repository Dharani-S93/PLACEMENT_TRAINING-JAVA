# PLACEMENT_TRAINING-JAVA
This repository features beginner-friendly Java programs showcasing essential string operations like concatenation, length, charAt(), case conversions, trimming, and substring handling. It also includes advanced examples such as string reversal, character counting, and replacements, with outputs for easy understanding.


# Concatenation in Java
```[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        String s2 = "Dharu";
        System.out.println("Print the statement: " + s1 + " " + s2);
    }
}
OUTPUT
Print the statement: Hello Dharu
````

# Finding Length in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        int length = s1.length();
        System.out.println("Print the statement: " + length);
    }
}
OUTPUT
Print the statement: 5
````


# charAt() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        char ch = s1.charAt(3);
        System.out.println("Print the statement: " + ch);
    }
}
OUTPUT
Print the statement: l
````

# Uppercase Conversion
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        System.out.println("Print the statement: " + s1.toUpperCase());
    }
}
OUTPUT
Print the statement: HELLO
````

# Lowercase Conversion
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        System.out.println("Print the statement: " + s1.toLowerCase());
    }
}
OUTPUT
Print the statement: hello
````

# indexOf() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        System.out.println("Print the statement: " + s1.indexOf('e'));
    }
}
OUTPUT
Print the statement: 1
````

# lastIndexOf() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        System.out.println("Print the statement: " + s1.lastIndexOf('o'));
    }
}
OUTPUT
Print the statement: 4
````

# startsWith() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello DHARUU";
        System.out.println("Print the statement: " + s1.startsWith("Hello"));
    }
}
OUTPUT
Print the statement: true
````

# endsWith() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello DHARUU";
        System.out.println("Print the statement: " + s1.endsWith("Hello"));
    }
}
OUTPUT
Print the statement: false
````

# Substring
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello DHARUU";
        System.out.println("Print the statement: " + s1.substring(3));
    }
}
OUTPUT
Print the statement: lo DHARUU
````


# Replace All
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello Dee";
        System.out.println("Print the statement: " + s1.replaceAll("el", "ae"));
    }
}
OUTPUT
Print the statement: Haelo Dee
````

# Trim in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "  Hello World  ";
        System.out.println("Print the statement: " + s1.trim());
    }
}
OUTPUT
Print the statement: Hello World
````

# Split in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello World";
        String[] words = s1.split(" ");
        System.out.println("Print the statement: " + words[0] + " " + words[1]);
    }
}
OUTPUT
Print the statement: Hello World
````


# valueOf() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        int num = 123;
        String s1 = String.valueOf(num);
        System.out.println("Print the statement: " + s1);
    }
}
OUTPUT
Print the statement: 123
````

# matches() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello World";
        System.out.println("Print the statement: " +s1.matches(".*World.*"));
    }
}
OUTPUT
Print the statement: true
````


# replaceFirst() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello World World";
        System.out.println("Print the statement: " + s1.replaceFirst("World", "Dharu"));
    }
}
OUTPUT
Print the statement: Hello Dharu World
````



# isEmpty() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "";
        System.out.println("Print the statement: " + s1.isEmpty());
    }
}
OUTPUT
Print the statement: true
````


# toCharArray() in Java
````
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        char[] chars = s1.toCharArray();
        System.out.println("Print the statement: " + chars[0] + chars[1] + chars[2] + chars[3] + chars[4]);
    }
}
OUTPUT
Print the statement: Hello
````

# equals() in Java
````
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello World";
        String s2 = "Hello World";
        System.out.println("Print the statement: " + s1.equals(s2));
    }
}
OUTPUT
Print the statement: true
````

# equalsIgnoreCase() in Java
````
public class Main {
    public static void main(String[] args) {
        String s1 = "hello world";
        String s2 = "Hello World";
        System.out.println("Print the statement: " + s1.equalsIgnoreCase(s2));
    }
}
OUTPUT
Print the statement: true
````


# IMPORTANT JAVA STRING PROBLEMS

# Reversing a String
````
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello Dee";
        String rev = "";
        for (int i = s1.length() - 1; i >= 0; i--) {
            rev += s1.charAt(i);
        }
        System.out.println("Print the statement: " + rev);
    }
}

OUTPUT
Print the statement: eeD olleH
````

# Occurrence of a Character in a String
````
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello dharuu";
        char ch = 'l';
        int count = 0;
        for (int i = 0; i < s1.length(); i++) {
            if (s1.charAt(i) == ch) {
                count++;
            }
        }
        System.out.println("Print the statement: " + count);
    }
}
OUTPUT
Print the statement: 2
````


# Check if a String Contains Only Alphabetic Characters
````
public class Main {
    public static void main(String[] args) {
        String s1 = "HelloDharu";
        if(s1.matches("[a-zA-Z]+")){
            
        System.out.println(" TRUE");
    }
    else{
        System.out.println("FALSE");
    }
}
}
OUTPUT
 HelloDharu-TRUE
 HelloDharu21-FALSE
````

# 













