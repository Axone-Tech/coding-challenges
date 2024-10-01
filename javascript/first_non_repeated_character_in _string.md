## Find the first non-repeated character in a string

**Question:** Write a function to find the first non-repeated character in a string.

**Solution:**

```javascript
function firstNonRepeatedChar(str) {
  // Create an object to store character frequencies
  const charFrequency = {};
  
  // Count the frequency of each character
  for (let char of str) {
    charFrequency[char] = (charFrequency[char] || 0) + 1;
  }
  
  // Find the first character with a frequency of 1
  for (let char of str) {
    if (charFrequency[char] === 1) {
      return char;
    }
  }
  
  // If no non-repeated character is found
  return null;
}

// Example usage
console.log(firstNonRepeatedChar("aabcbd")); // Output: "c"