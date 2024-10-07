## Implement a function to check if an array contains duplicates

**Question:** Write a function that checks whether an array contains any duplicate elements.

**Solution:**
```java
import java.util.HashSet;

public class DuplicateChecker {
    public static boolean containsDuplicates(int[] arr) {
        HashSet<Integer> seen = new HashSet<>();
        for (int num : arr) {
            if (seen.contains(num)) {
                return true;
            }
            seen.add(num);
        }
        return false;
    }

    // Example usage
    public static void main(String[] args) {
        System.out.println(containsDuplicates(new int[]{1, 2, 3, 4, 5})); // Output: false
        System.out.println(containsDuplicates(new int[]{1, 2, 3, 3, 4, 5})); // Output: true
    }
}
