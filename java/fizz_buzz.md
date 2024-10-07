## FizzBuzz

**Question:** Write a function that prints the numbers from 1 to 100. For multiples of 3, print "Fizz" instead of the number. For multiples of 5, print "Buzz". For numbers which are multiples of both 3 and 5, print "FizzBuzz".

**Solution:**
```java
public class FizzBuzz {
    public static void main(String[] args) {
        for (int i = 1; i <= 100; i++) {
            StringBuilder output = new StringBuilder();

            // Check if number is divisible by 3
            if (i % 3 == 0) output.append("Fizz");

            // Check if number is divisible by 5
            if (i % 5 == 0) output.append("Buzz");

            // If output is empty, use the number itself
            if (output.length() == 0) {
                System.out.println(i);
            } else {
                System.out.println(output);
            }
        }
    }
}
