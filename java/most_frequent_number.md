## Find Most Frequent Element

**Question:** Write a function that finds the most frequent element in an array.

**Solution:**
```java
import java.util.HashMap;

public class MostFrequentElement {
    public static int mostFrequentElement(int[] arr) {
        HashMap<Integer, Integer> frequencyMap = new HashMap<>();
        int maxFrequency = 0;
        int mostFrequent = arr[0]; // Initialize with the first element

        for (int item : arr) {
            frequencyMap.put(item, frequencyMap.getOrDefault(item, 0) + 1);
            if (frequencyMap.get(item) > maxFrequency) {
                maxFrequency = frequencyMap.get(item);
                mostFrequent = item;
            }
        }

        return mostFrequent;
    }

    public static void main(String[] args) {
        // Example usage
        int[] numbers = {1, 2, 3, 2, 4, 2, 5, 1, 2};
        System.out.println(mostFrequentElement(numbers)); // Output: 2
    }
}
