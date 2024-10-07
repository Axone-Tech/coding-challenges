## Remove duplicates from an array

**Question:** Write a function to remove duplicates from an array.

**Solution:**

```typescript
function removeDuplicates<T>(arr: T[]): T[] {
  // Use a Set to store unique values, then convert back to an array
  return [...new Set(arr)];
}

// Example usage
console.log(removeDuplicates<number>([1, 2, 2, 3, 4, 4, 5])); // Output: [1, 2, 3, 4, 5]
```
```

</rewritten_file>
