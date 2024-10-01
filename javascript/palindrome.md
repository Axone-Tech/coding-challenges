## Check for palindrome

**Question:** Write a function to check if a given string is a palindrome.

**Solution:**

```javascript
function isPalindrome(str) {
  // Remove non-alphanumeric characters and convert to lowercase
  str = str.replace(/[^a-zA-Z0-9]/g, '').toLowerCase();
  
  // Compare the string with its reverse
  return str === str.split('').reverse().join('');
}

// Example usage
console.log(isPalindrome("A man, a plan, a canal: Panama")); // Output: true