# Java Interface

* [Java Interface](https://www.hackerrank.com/challenges/java-interface/problem) `easy`

You are given an interface `AdvancedArithmetic` which contains a method signature `int divisor_sum(int n)`. You need to write a class called `MyCalculator` which implements the interface.

divisorSum function just takes an integer as input and return the sum of all its divisors. For example divisors of 6 are 1, 2, 3 and 6, so divisor_sum should return 12. The value of `n` will be at most 1000.

Read the partially completed code in the editor and complete it. You just need to write the `MyCalculator` class only. Your class shouldn't be public.

**Sample Input**

```txt
6
```

**Sample Output**

```txt
I implemented: AdvancedArithmetic
12
```

### General Approach

```java
import java.util.*;

interface AdvancedArithmetic {
  int divisor_sum(int n);
}

// O(n)
class MyCalculator implements AdvancedArithmetic {
    @Override
    public int divisor_sum(int n) {
        int i = 1;
        int sum = 0;
        
        while (i <= n) {
            int val = n % i;

            if (val == 0) {
                sum += i;
            }
            
            i += 1;
        }
        
        return sum;
    }
}

class Solution {
    public static void main(String []args){
        MyCalculator my_calculator = new MyCalculator();
        System.out.print("I implemented: ");
        ImplementedInterfaceNames(my_calculator);
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        System.out.print(my_calculator.divisor_sum(n) + "\n");
      	sc.close();
    }

    static void ImplementedInterfaceNames(Object o){
        Class[] theInterfaces = o.getClass().getInterfaces();
        for (int i = 0; i < theInterfaces.length; i++){
            String interfaceName = theInterfaces[i].getName();
            System.out.println(interfaceName);
        }
    }
}
```

### Optimized Approach

* If `i` is a divisor of `n`, then `n/i` is also a divisor.
* Rather than checking all numbers from `1` to `n`, you only need to check numbers from `1` to `√n`. 
  * For each divisor `i` you find, you can add both `i` and `n/i` to the sum.
* If `i == n/i`, then `i` should only be added once. 

```java
import java.util.*;

interface AdvancedArithmetic {
  int divisor_sum(int n);
}

// O(√n)
class MyCalculator implements AdvancedArithmetic {
    @Override
    public int divisor_sum(int n) {
        int i = 1;
        int sum = 0;
        
        // divisors come in pairs
        while (i*i <= n) {
            int val = n % i;

            if (val == 0) {
                sum += i;

                // If `i` [when i is square root of n] is not the same as `n/i` (36/6=6), add `n/i`
                if (i != n/i) {
                    sum += (n/i);
                }
            }

            i += 1;
        }
        
        return sum;
    }
}

class Solution {
    public static void main(String []args){
        MyCalculator my_calculator = new MyCalculator();
        System.out.print("I implemented: ");
        ImplementedInterfaceNames(my_calculator);
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        System.out.print(my_calculator.divisor_sum(n) + "\n");
      	sc.close();
    }

    static void ImplementedInterfaceNames(Object o){
        Class[] theInterfaces = o.getClass().getInterfaces();
        for (int i = 0; i < theInterfaces.length; i++){
            String interfaceName = theInterfaces[i].getName();
            System.out.println(interfaceName);
        }
    }
}
```
