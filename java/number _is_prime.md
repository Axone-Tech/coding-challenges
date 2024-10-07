## Check if a number is prime

**Question:** Write a function to check if a given number is prime.

**Solution:**
```java
public class PrimeChecker {
    public static boolean isPrime(int num) {
        // Numbers less than 2 are not prime
        if (num < 2) return false;
        
        // Check for divisibility up to the square root of the number
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) return false;
        }
        
        return true;
    }

    public static void main(String[] args) {
        // Example usage
        System.out.println(isPrime(17)); // Output: true
        System.out.println(isPrime(15)); // Output: false
    }
}
