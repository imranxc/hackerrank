# Java Loops I

* [Java Loops I](https://www.hackerrank.com/challenges/java-loops-i/problem) `easy`

In this challenge, we're going to use loops to help us do some simple math.

Given an integer `N`. print its first 10 multiples. Each multiple `N x i` (where `1 ≤ i ≤ 10`) should be printed on a new line in the form: `N x i = result`.

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

public class Solution {
  public static void main(String[] args) throws IOException {
    BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
    int N = Integer.parseInt(bufferedReader.readLine().trim());
    bufferedReader.close();

    for (int i = 1; i <= 10; i++) {
      System.out.println(N + " x " + i + " = " + N * i);
    }
  }
}
```
