## Remove duplicates from an array

**Question:** Write a function to remove duplicates from an array.

**Solution:**

```javascript
function removeDuplicates(arr) {
  // Use a Set to store unique values, then convert back to an array
  return [...new Set(arr)];
}

// Example usage
console.log(removeDuplicates([1, 2, 2, 3, 4, 4, 5])); // Output: [1, 2, 3, 4, 5]