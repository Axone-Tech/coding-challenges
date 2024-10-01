## FizzBuzz

**Question:** Write a function that prints the numbers from 1 to 100. For multiples of 3, print "Fizz" instead of the number. For multiples of 5, print "Buzz". For numbers which are multiples of both 3 and 5, print "FizzBuzz".

**Solution:**

```javascript
function fizzBuzz() {
  for (let i = 1; i <= 100; i++) {
    let output = '';
    
    // Check if number is divisible by 3
    if (i % 3 === 0) output += 'Fizz';
    
    // Check if number is divisible by 5
    if (i % 5 === 0) output += 'Buzz';
    
    // If output is empty, use the number itself
    console.log(output || i);
  }
}

// Run the function
fizzBuzz();