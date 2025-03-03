# Java Exception Handling (Try-catch)

* [Java Exception Handling](https://www.hackerrank.com/challenges/java-exception-handling-try-catch/problem) `easy`

Java has built-in mechanism to handle exceptions. Using the try statement we can test a block of code for errors. The catch block contains the code that says what to do if exception occurs.

This problem will test your knowledge on try-catch block.

You will be given two integers `x` and `y` as input, you have to compute `x/y`. If `x` and `y` are not 32 bit signed integers or if `y` is zero, exception will occur and you have to report it. Read sample Input/Output to know what to report in case of exceptions.

**Sample Input 0:**

```txt
10
3
```

**Sample Output 0:**

```txt
3
```

**Sample Input 1:**

```txt
10
Hello
```

**Sample Output 1:**

```txt
java.util.InputMismatchException
```

**Sample Input 2:**

```txt
10
0
```

**Sample Output 2:**

```txt
java.lang.ArithmeticException: / by zero
```

**Sample Input 3:**

```txt
23.323
0
```

**Sample Output 3:**

```txt
java.util.InputMismatchException
```

### Code

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        try {
            int x = sc.nextInt();
            int y = sc.nextInt();
            System.out.println(x/y);
        } catch (ArithmeticException e1) {
                System.out.println(e1.toString());
        } catch (InputMismatchException e){
            System.out.println(e.getClass().getName());
        }
        sc.close();
    }
}
```
