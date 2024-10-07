## Check for palindrome

**Question:** Write a function to check if a given string is a palindrome.

**Solution:**
```java
public class PalindromeChecker {
    public static boolean isPalindrome(String str) {
        // Remove non-alphanumeric characters and convert to lowercase
        str = str.replaceAll("[^a-zA-Z0-9]", "").toLowerCase();
        
        // Compare the string with its reverse
        String reversed = new StringBuilder(str).reverse().toString();
        return str.equals(reversed);
    }

    public static void main(String[] args) {
        // Example usage
        System.out.println(isPalindrome("A man, a plan, a canal: Panama")); // Output: true
    }
}
