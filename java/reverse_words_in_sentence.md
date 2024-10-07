## Implement a function to reverse words in a sentence

**Question:** Write a function that reverses the words in a given sentence.

**Solution:**
```java
import java.util.Collections;
import java.util.List;
import java.util.Arrays;

public class ReverseWords {
    public static String reverseWords(String sentence) {
        // Split the sentence into words
        List<String> words = Arrays.asList(sentence.split(" "));
        
        // Reverse the list of words
        Collections.reverse(words);
        
        // Join the words back into a single string
        return String.join(" ", words);
    }

    public static void main(String[] args) {
        // Example usage
        System.out.println(reverseWords("Hello World")); // Output: "World Hello"
        System.out.println(reverseWords("The quick brown fox")); // Output: "fox brown quick The"
    }
}
