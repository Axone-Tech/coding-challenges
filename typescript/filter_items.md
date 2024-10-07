## Filter Items by Prefix

**Question:** Write a function that filters an array of strings, returning only the items that start with a specific prefix.

**Solution:**
```typescript
function filterByPrefix(items: string[], prefix: string): string[] {
  return items.filter(item => item.startsWith(prefix));
}

// Example usage
const fruits = ['apple', 'banana', 'apricot', 'cherry', 'avocado'];
console.log(filterByPrefix(fruits, 'a')); // Output: ['apple', 'apricot', 'avocado']
