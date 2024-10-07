## Implement a function to find the longest word in a sentence

**Question:** Write a function that finds the longest word in a given sentence.

**Solution:**
```java
public class LongestWordFinder {
    public static String findLongestWord(String sentence) {
        // Split the sentence into words
        String[] words = sentence.split(" ");
        String longest = "";

        for (String current : words) {
            // Remove any non-alphanumeric characters from the current word
            String cleanWord = current.replaceAll("[^\\w]", "");
            // Update the longest word if the current word is longer
            if (cleanWord.length() > longest.length()) {
                longest = cleanWord;
            }
        }
        return longest;
    }

    // Example usage
    public static void main(String[] args) {
        System.out.println(findLongestWord("The quick brown fox jumped over the lazy dog")); // Output: "jumped"
    }
}
