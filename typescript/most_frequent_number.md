## Find Most Frequent Element

**Question:** Write a function that finds the most frequent element in an array.

**Solution:**
```typescript
function mostFrequentElement(arr: number[]): number | undefined {
  const frequencyMap: { [key: number]: number } = {};
  let maxFrequency = 0;
  let mostFrequent: number | undefined;

  for (const item of arr) {
    frequencyMap[item] = (frequencyMap[item] || 0) + 1;
    if (frequencyMap[item] > maxFrequency) {
      maxFrequency = frequencyMap[item];
      mostFrequent = item;
    }
  }

  return mostFrequent;
}

// Example usage
const numbers = [1, 2, 3, 2, 4, 2, 5, 1, 2];
console.log(mostFrequentElement(numbers)); // Output: 2
