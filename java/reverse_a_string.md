## Reverse a string

**Question:** Write a function to reverse a string.

**Solution:**
```java
public class ReverseString {
    public static String reverseString(String str) {
        // Create a StringBuilder to reverse the string
        return new StringBuilder(str).reverse().toString();
    }

    public static void main(String[] args) {
        // Example usage
        System.out.println(reverseString("hello")); // Output: "olleh"
    }
}
