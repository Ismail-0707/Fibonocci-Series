# Fibonacci Series Using Recursion

## Problem Statement

Given a number `n`, print the first `n` terms of the Fibonacci Series using recursion.

The Fibonacci Series is a sequence where each number is the sum of the two preceding numbers.

## Example

Input:
```text
7
```

Output:
```text
0 1 1 2 3 5 8
```

## Approach

1. Define a recursive function `fibonacci(n)`.
2. If `n` is `0` or `1`, return `n`.
3. Otherwise, return:
   ```text
   fibonacci(n - 1) + fibonacci(n - 2)
   ```
4. Use a loop to print the first `n` Fibonacci numbers.

## Java Solution

```java
import java.util.*;

class Main {

    static int fibonacci(int n) {
        if (n <= 1) {
            return n;
        }

        return fibonacci(n - 1) + fibonacci(n - 2);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        for (int i = 0; i < n; i++) {
            System.out.print(fibonacci(i) + " ");
        }
    }
}
```

## Recursion Trace

For:

```text
fibonacci(5)
```

```text
fibonacci(5)
= fibonacci(4) + fibonacci(3)

= (fibonacci(3) + fibonacci(2))
  + (fibonacci(2) + fibonacci(1))

= 3 + 2

= 5
```

## Base Cases

```java
if (n <= 1) {
    return n;
}
```

```text
fibonacci(0) = 0
fibonacci(1) = 1
```

These base cases stop the recursion.

## Complexity Analysis

- **Time Complexity:** O(2ⁿ)
- **Space Complexity:** O(n)

## Tags

`Recursion` `Fibonacci` `Math` `Dynamic Programming`
