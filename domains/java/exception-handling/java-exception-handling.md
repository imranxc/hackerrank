# Java Exception Handling

* [Java Exception Handling](https://www.hackerrank.com/challenges/java-exception-handling/problem) `easy`

You are required to compute the power of a number by implementing a calculator. Create a class `MyCalculator` which consists of a single method `long power (int, int)`. This method takes two integers, `n` and `p`. as parameters and finds np. If either `n` or `p` is negative, then the method must throw an exception which says "n or p should not be negative". Also. if both `n` and `p` are zero, then the method must throw an exception which says "n and p should not be zero."

For example, -4 and -5 would result in

`java.lang.Exception: n or p should not be negative.`

Complete the function power in class `MyCalculator` and return the appropriate result after the power operation or an appropriate exception as detailed above.

```java
import java.util.Scanner;

class MyClass {
  public long power(int n, int p) throws Exception {
    if (n < 0 || p < 0) {
      throw new Exception("n or p should not be negative.");
    } else if (n == 0 && p == 0) {
      throw new Exception("n and p should not be zero.");
    } else {
      return (long) Math.pow(n, p);
    }
  }
}

public class Solution {
  public static final MyClass my_calculator = new MyClass();
  public static final Scanner in = new Scanner(System.in);

  public static void main(String[] args) {
    while (in.hasNextInt()) {
      int n = in.nextInt();
      int p = in.nextInt();

      try {
        System.out.println(my_calculator.power(n, p));
      } catch (Exception e) {
        System.out.println(e);
      }
    }
  }
}
```
