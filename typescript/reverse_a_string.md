## Reverse a string

**Question:** Write a function to reverse a string.

**Solution:**
```typescript
function reverseString(str: string): string {
  // Split the string into an array of characters
  // Reverse the array
  // Join the array back into a string
  return str.split('').reverse().join('');
}

// Example usage
console.log(reverseString("hello")); // Output: "olleh"
