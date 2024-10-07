## Implement a function to find the longest word in a sentence

**Question:** Write a function that finds the longest word in a given sentence.

**Solution:**
```typescript
function findLongestWord(sentence: string): string {
  // Split the sentence into words
  const words = sentence.split(' ');

  // Use reduce to find the longest word
  return words.reduce((longest: string, current: string) => {
    // Remove any non-alphanumeric characters from the current word
    const cleanWord = current.replace(/[^\w]/g, '');
    // Return the longer word
    return cleanWord.length > longest.length ? cleanWord : longest;
  }, '');
}

// Example usage
console.log(findLongestWord("The quick brown fox jumped over the lazy dog")); // Output: "jumped"
