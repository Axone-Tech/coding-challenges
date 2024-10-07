## Implement a function to check if an array contains duplicates

**Question:** Write a function that checks whether an array contains any duplicate elements.

**Solution:**
```typescript
function containsDuplicates<T>(arr: T[]): boolean {
  const seen = new Set<T>();
  for (const item of arr) {
    if (seen.has(item)) return true;
    seen.add(item);
  }
  return false;
}

// Example usage
console.log(containsDuplicates([1, 2, 3, 4, 5])); // Output: false
console.log(containsDuplicates([1, 2, 3, 3, 4, 5])); // Output: true
console.log(containsDuplicates(['a', 'b', 'c', 'b'])); // Output: true
```
```

