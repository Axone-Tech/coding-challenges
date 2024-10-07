## Implement a function to check if a number is prime

**Question:** Write a function that checks if a given number is prime.

**Solution:**
```java
public class PrimeChecker {
    public static boolean isPrime(int num) {
        if (num <= 1) return false;
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) return false;
        }
        return true;
    }

    // Example usage
    public static void main(String[] args) {
        System.out.println(isPrime(7));  // Output: true
        System.out.println(isPrime(10)); // Output: false
    }
}
