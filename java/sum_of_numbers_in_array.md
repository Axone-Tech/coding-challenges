## Implement a function to find the sum of all numbers in an array

**Question:** Write a function that calculates the sum of all numbers in an array.

**Solution:**
```java
import java.util.Arrays;

public class SumArray {
    public static int sumArray(int[] arr) {
        return Arrays.stream(arr).sum();
    }

    // Example usage
    public static void main(String[] args) {
        System.out.println(sumArray(new int[]{1, 2, 3, 4, 5})); // Output: 15
        System.out.println(sumArray(new int[]{10, -2, 3, 7})); // Output: 18
    }
}
