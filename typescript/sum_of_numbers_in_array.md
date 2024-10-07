## Implement a function to find the sum of all numbers in an array

**Question:** Write a function that calculates the sum of all numbers in an array.

**Solution:**
```typescript
function sumArray(arr: number[]): number {
  return arr.reduce((acc, num) => acc + num, 0);
}

// Example usage
console.log(sumArray([1, 2, 3, 4, 5])); // Output: 15
console.log(sumArray([10, -2, 3, 7])); // Output: 18
