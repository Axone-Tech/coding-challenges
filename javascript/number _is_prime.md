## Check if a number is prime

**Question:** Write a function to check if a given number is prime.

**Solution:**

```javascript
function isPrime(num) {
  // Numbers less than 2 are not prime
  if (num < 2) return false;
  
  // Check for divisibility up to the square root of the number
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) return false;
  }
  
  return true;
}

// Example usage
console.log(isPrime(17)); // Output: true
console.log(isPrime(15)); // Output: false