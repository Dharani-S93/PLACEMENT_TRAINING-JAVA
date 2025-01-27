# PLACEMENT_TRAINING-JAVA-
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

# Trim
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = " Hello  dharuuu ";
        System.out.println("Print the statement: " + s1.trim());
    }
}
OUTPUT
Print the statement: Hello  dharuuu
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


# split()
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello World";
        System.out.println("Print the statement: " + s1.substring(6));
    }
}
OUTPUT
Print the statement: World
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
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello World";
        System.out.println("Print the statement: " + s1.matches(".*World.*"));
    }
}
OUTPUT
Print the statement: true
````












