# Java Inheritance I

* [Java Inheritance I](https://www.hackerrank.com/challenges/java-inheritance-1/problem) `easy`

Using inheritance, one class can acquire the properties of others. Consider the following Animal class:

```java
class Animal {
  void walk() {
    System.out.println("I am walking");
  }
}
```

This class has only one method, walk. Next, we want to create a Bird class that also has a fly method. We do this using extends keyword:

```java
class Bird extends Animal {
  void fly() {
    System.out.println("I am flying");
  }
}
```

Finally, we can create a Bird object that can both fly and walk.

```java
public class Solution {
  public static void main(String[] args) {

    Bird bird = new Bird();
    bird.walk();
    bird.fly();
  }
}
```

The above code will print:

```txt
I am walking
I am flying
```
This means that a Bird object has all the properties that an Animal object has, as well as some additional unique properties.

The code above is provided for you in your editor. You must add a sing method to the Bird class, then modify the main method accordingly so that the code prints the following lines:

```txt
I am walking
I am flying
I am singing
```

### Completed Code

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

class Animal {
  void walk() {
    System.out.println("I am walking");
  }
}

class Bird extends Animal {
  void fly() {
    System.out.println("I am flying");
  }

  void sing() {
    System.out.println("I am singing");
  }
}

public class Solution {

  public static void main(String args[]) {

    Bird bird = new Bird();
    bird.walk();
    bird.fly();
    bird.sing();
  }
}
```
