# Java Static Initializer Block

* [Java Static Initializer Block](https://www.hackerrank.com/challenges/java-static-initializer-block/problem) `easy`

Static initialization blocks are executed when the class is loaded, and you can initialize static variables in those blocks.

It's time to test your knowledge of Static initialization blocks.

You are given a class `Solution` with a `main` method. Complete the given code so that it outputs the area of a parallelogram with breadth `B` and height `H`. You should read the variables from the standard input.

If `B ≤ 0` or `H ≤ 0`, the output should be "java.lang.Exception: Breadth and height must be positive" without quotes.

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {}

    static {
        try {
            Scanner sc = new Scanner(System.in);
            int b = sc.nextInt();
            int h = sc.nextInt();
            
            if (b <= 0 || h <= 0) {
                throw new Exception("Breadth and height must be positive");
            } else {
                System.out.println(b * h);
            }
            sc.close();
        } catch (Exception e) {
            System.out.println(e.getClass().getName() + ": " + e.getMessage());
        }
    }
}
```
