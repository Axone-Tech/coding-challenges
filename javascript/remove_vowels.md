## Implement a function to remove vowels from a string

**Question:** Write a function that removes all vowels from a given string.

**Solution:**
```javascript
function removeVowels(str) {
  return str.replace(/[aeiou]/gi, '');
}

// Example usage
console.log(removeVowels("Hello World")); // Output: "Hll Wrld"
console.log(removeVowels("JavaScript"));  // Output: "JvScrpt"
