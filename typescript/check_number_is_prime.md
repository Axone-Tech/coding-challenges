## Implement a function to check if a number is prime

**Question:** Write a function that checks if a given number is prime.

**Solution:**
```typescript
function isPrime(num: number): boolean {
  if (num <= 1) return false;
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) return false;
  }
  return true;
}

// Example usage
console.log(isPrime(7));  // Output: true
console.log(isPrime(10)); // Output: false
