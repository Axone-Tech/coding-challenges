## Implement a function to remove vowels from a string

**Question:** Write a function that removes all vowels from a given string.

**Solution:**
```typescript
function removeVowels(str: string): string {
  return str.replace(/[aeiou]/gi, '');
}

// Example usage
console.log(removeVowels("Hello World")); // Output: "Hll Wrld"
console.log(removeVowels("JavaScript"));  // Output: "JvScrpt"
