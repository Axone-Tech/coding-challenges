## Remove duplicates from an array

**Question:** Write a function to remove duplicates from an array.

**Solution:**
```java
import java.util.Arrays;
import java.util.LinkedHashSet;

public class RemoveDuplicates {
    public static Integer[] removeDuplicates(Integer[] arr) {
        // Use a LinkedHashSet to maintain insertion order and remove duplicates
        LinkedHashSet<Integer> set = new LinkedHashSet<>(Arrays.asList(arr));
        return set.toArray(new Integer[0]);
    }

    public static void main(String[] args) {
        // Example usage
        Integer[] result = removeDuplicates(new Integer[]{1, 2, 2, 3, 4, 4, 5});
        System.out.println(Arrays.toString(result)); // Output: [1, 2, 3, 4, 5]
    }
}
