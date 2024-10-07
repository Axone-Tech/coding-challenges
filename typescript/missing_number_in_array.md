## Implement a function to find the missing number in an array of 1 to N

**Question:** Given an array containing n distinct numbers taken from 0, 1, 2, ..., n, find the one that is missing from the array.

**Solution:**
```typescript
function findMissingNumber(nums: number[]): number {
  const n = nums.length;

  // Calculate the expected sum of numbers from 0 to n
  const expectedSum = (n * (n + 1)) / 2;

  // Calculate the actual sum of the array
  const actualSum = nums.reduce((sum, num) => sum + num, 0);

  // The difference is the missing number
  return expectedSum - actualSum;
}

// Example usage
console.log(findMissingNumber([3, 0, 1])); // Output: 2
console.log(findMissingNumber([9, 6, 4, 2, 3, 5, 7, 0, 1])); // Output: 8
