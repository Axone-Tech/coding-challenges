## Find the first non-repeated character in a string

**Question:** Write a function to find the first non-repeated character in a string.

**Solution:**
```java
import java.util.HashMap;

public class FirstNonRepeatedCharFinder {
    public static Character firstNonRepeatedChar(String str) {
        // Create a map to store character frequencies
        HashMap<Character, Integer> charFrequency = new HashMap<>();

        // Count the frequency of each character
        for (char ch : str.toCharArray()) {
            charFrequency.put(ch, charFrequency.getOrDefault(ch, 0) + 1);
        }

        // Find the first character with a frequency of 1
        for (char ch : str.toCharArray()) {
            if (charFrequency.get(ch) == 1) {
                return ch;
            }
        }

        // If no non-repeated character is found
        return null;
    }

    // Example usage
    public static void main(String[] args) {
        System.out.println(firstNonRepeatedChar("aabcbd")); // Output: "c"
    }
}
