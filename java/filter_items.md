## Filter Items by Prefix

**Question:** Write a function that filters an array of strings, returning only the items that start with a specific prefix.

**Solution:**
```java
import java.util.List;
import java.util.ArrayList;

public class FilterByPrefix {
    public static List<String> filterByPrefix(List<String> items, String prefix) {
        List<String> filteredItems = new ArrayList<>();
        for (String item : items) {
            if (item.startsWith(prefix)) {
                filteredItems.add(item);
            }
        }
        return filteredItems;
    }

    // Example usage
    public static void main(String[] args) {
        List<String> fruits = List.of("apple", "banana", "apricot", "cherry", "avocado");
        System.out.println(filterByPrefix(fruits, "a")); // Output: [apple, apricot, avocado]
    }
}
