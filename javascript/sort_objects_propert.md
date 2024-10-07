## Sort Objects by Property

**Question:** Create a function that sorts an array of objects based on a specified property of the objects.

**Solution:**

```javascript
function sortByProperty(array, property) {
  return array.sort((a, b) => {
    if (a[property] < b[property]) return -1;
    if (a[property] > b[property]) return 1;
    return 0;
  });
}

// Example usage
const people = [
  { name: 'Alice', age: 30 },
  { name: 'Bob', age: 25 },
  { name: 'Charlie', age: 35 }
];
console.log(sortByProperty(people, 'age'));
// Output: [{ name: 'Bob', age: 25 }, { name: 'Alice', age: 30 }, { name: 'Charlie', age: 35 }]
```
```

