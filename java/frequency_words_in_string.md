## Implement a function to count the frequency of words in a string

**Question:** Write a function that counts how many times each word appears in a given string.

**Solution:**
```java
import java.util.HashMap;
import java.util.Map;

public class WordFrequency {
    public static Map<String, Integer> wordFrequency(String sentence) {
        // Convert the sentence to lowercase and split it into words
        String[] words = sentence.toLowerCase().split("\\W+");
        Map<String, Integer> frequency = new HashMap<>();

        for (String word : words) {
            if (!word.isEmpty()) {
                frequency.put(word, frequency.getOrDefault(word, 0) + 1);
            }
        }
        return frequency;
    }

    public static void main(String[] args) {
        // Example usage
        System.out.println(wordFrequency("The quick brown fox jumps over the lazy dog"));
        // Output: {the=2, quick=1, brown=1, fox=1, jumps=1, over=1, lazy=1, dog=1}

        System.out.println(wordFrequency("Hello hello world!"));
        // Output: {hello=2, world=1}
    }
}
