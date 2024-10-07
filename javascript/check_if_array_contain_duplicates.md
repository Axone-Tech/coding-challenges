## Implement a function to check if an array contains duplicates

**Question:** Write a function that checks whether an array contains any duplicate elements.

**Solution:**
```javascript
function containsDuplicates(arr) {
  let seen = new Set();
  for (let num of arr) {
    if (seen.has(num)) return true;
    seen.add(num);
  }
  return false;
}

// Example usage
console.log(containsDuplicates([1, 2, 3, 4, 5])); // Output: false
console.log(containsDuplicates([1, 2, 3, 3, 4, 5])); // Output: true
