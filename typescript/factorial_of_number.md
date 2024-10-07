## Implement a function to find the factorial of a number

**Question:** Write a function that calculates the factorial of a given number.

**Solution:**
```typescript
function factorial(n: number): number {
  if (n === 0 || n === 1) return 1;
  return n * factorial(n - 1);
}

// Example usage
console.log(factorial(5)); // Output: 120
console.log(factorial(0)); // Output: 1
