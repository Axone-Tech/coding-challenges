## Implement a function to count the frequency of words in a string

**Question:** Write a function that counts how many times each word appears in a given string.

**Solution:**
```typescript
function wordFrequency(sentence: string): { [key: string]: number } {
  const words = sentence.toLowerCase().split(/\W+/);
  const frequency: { [key: string]: number } = {};

  for (const word of words) {
    if (word) {
      frequency[word] = (frequency[word] || 0) + 1;
    }
  }
  return frequency;
}

// Example usage
console.log(wordFrequency("The quick brown fox jumps over the lazy dog")); 
// Output: { the: 2, quick: 1, brown: 1, fox: 1, jumps: 1, over: 1, lazy: 1, dog: 1 }

console.log(wordFrequency("Hello hello world!")); 
// Output: { hello: 2, world: 1 }
