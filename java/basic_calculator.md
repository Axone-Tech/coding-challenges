## Implement a basic calculator

**Question:** Implement a basic calculator that can perform addition, subtraction, multiplication, and division.

**Solution:**
```java
public class BasicCalculator {
    public static double calculator(double a, double b, char operation) {
        switch (operation) {
            case '+':
                return a + b;
            case '-':
                return a - b;
            case '*':
                return a * b;
            case '/':
                // Check for division by zero
                if (b == 0) throw new IllegalArgumentException("Cannot divide by zero");
                return a / b;
            default:
                throw new IllegalArgumentException("Invalid operation");
        }
    }

    // Example usage
    public static void main(String[] args) {
        System.out.println(calculator(5, 3, '+')); // Output: 8.0
        System.out.println(calculator(10, 2, '/')); // Output: 5.0
    }
}
