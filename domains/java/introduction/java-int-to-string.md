# Java Int to String

* [Java Int to String](https://www.hackerrank.com/challenges/java-int-to-string/problem) `easy`

You are given an `integer` , you have to convert it into a `string`.

Please complete the partially completed code in the editor. If your code successfully converts  `n` into a string `s` the code will print "Good job". Otherwise it will print "Wrong answer".

```java
import java.util.*;
import java.security.*;

public class Solution {
  public static void main(String[] args) {

    DoNotTerminate.forbidExit();

    try {
      Scanner in = new Scanner(System.in);
      int n = in.nextInt();
      // String s=???; Complete this line below
      String s = Integer.toString(n);

      if (n == Integer.parseInt(s)) {
        System.out.println("Good job");
      } else {
        System.out.println("Wrong answer.");
      }
    } catch (DoNotTerminate.ExitTrappedException e) {
      System.out.println("Unsuccessful Termination!!");
    } finally {
        in.close();
    }
  }
}

// The following class will prevent you from terminating the code using exit(0)!
class DoNotTerminate {

  public static class ExitTrappedException extends SecurityException {
    private static final long serialVersionUID = 1;
  }

  public static void forbidExit() {
    final SecurityManager securityManager = new SecurityManager() {
      @Override
      public void checkPermission(Permission permission) {
        if (permission.getName().contains("exitVM")) {
          throw new ExitTrappedException();
        }
      }
    };
    System.setSecurityManager(securityManager);
  }
}
```
