## Implement a function to reverse words in a sentence

**Question:** Write a function that reverses the words in a given sentence.

**Solution:**
```javascript
function reverseWords(sentence) {
  // Split the sentence into words, reverse the array, and join back
  return sentence.split(' ').reverse().join(' ');
}

// Example usage
console.log(reverseWords("Hello World")); // Output: "World Hello"
console.log(reverseWords("The quick brown fox")); // Output: "fox brown quick The"