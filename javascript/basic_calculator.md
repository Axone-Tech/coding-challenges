## Implement a basic calculator

**Question:** Implement a basic calculator that can perform addition, subtraction, multiplication, and division.

**Solution:**
```javascript
function calculator(a, b, operation) {
  switch (operation) {
    case '+':
      return a + b;
    case '-':
      return a - b;
    case '*':
      return a * b;
    case '/':
      // Check for division by zero
      if (b === 0) throw new Error("Cannot divide by zero");
      return a / b;
    default:
      throw new Error("Invalid operation");
  }
}

// Example usage
console.log(calculator(5, 3, '+')); // Output: 8
console.log(calculator(10, 2, '/')); // Output: 5