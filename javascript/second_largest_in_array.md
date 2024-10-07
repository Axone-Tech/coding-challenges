## Implement a function to find the second largest number in an array

**Question:** Write a function to find the second largest number in a given array of numbers.

**Solution:**
```javascript
function secondLargest(arr) {
  let largest = -Infinity, secondLargest = -Infinity;
  
  for (let num of arr) {
    if (num > largest) {
      secondLargest = largest;
      largest = num;
    } else if (num > secondLargest && num !== largest) {
      secondLargest = num;
    }
  }
  return secondLargest;
}

// Example usage
console.log(secondLargest([10, 5, 8, 12, 7])); // Output: 10
console.log(secondLargest([1, 2, 3, 4, 5]));   // Output: 4
