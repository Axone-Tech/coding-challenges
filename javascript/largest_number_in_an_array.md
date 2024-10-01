## Find the largest number in an array

**Question:** Write a function to find the largest number in an array.

**Solution:**

```javascript
function findLargestNumber(arr) {
  // Use the spread operator with Math.max to find the largest number
  return Math.max(...arr);
}

// Example usage
console.log(findLargestNumber([1, 5, 2, 9, 3])); // Output: 9