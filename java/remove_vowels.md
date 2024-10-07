## Implement a function to remove vowels from a string

**Question:** Write a function that removes all vowels from a given string.

**Solution:**
```java
public class RemoveVowels {
    public static String removeVowels(String str) {
        // Use a regular expression to remove vowels (both uppercase and lowercase)
        return str.replaceAll("[aeiouAEIOU]", "");
    }

    public static void main(String[] args) {
        // Example usage
        System.out.println(removeVowels("Hello World")); // Output: "Hll Wrld"
        System.out.println(removeVowels("JavaScript"));  // Output: "JvScrpt"
    }
}
