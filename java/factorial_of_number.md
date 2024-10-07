## Implement a function to find the factorial of a number

**Question:** Write a function that calculates the factorial of a given number.

**Solution:**
```java
public class FactorialCalculator {
    public static long factorial(int n) {
        if (n == 0 || n == 1) return 1;
        return n * factorial(n - 1);
    }

    // Example usage
    public static void main(String[] args) {
        System.out.println(factorial(5)); // Output: 120
        System.out.println(factorial(0)); // Output: 1
    }
}
