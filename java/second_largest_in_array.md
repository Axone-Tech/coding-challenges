## Implement a function to find the second largest number in an array

**Question:** Write a function to find the second largest number in a given array of numbers.

**Solution:**
```java
public class SecondLargest {
    public static int secondLargest(int[] arr) {
        int largest = Integer.MIN_VALUE;
        int secondLargest = Integer.MIN_VALUE;
        
        for (int num : arr) {
            if (num > largest) {
                secondLargest = largest;
                largest = num;
            } else if (num > secondLargest && num != largest) {
                secondLargest = num;
            }
        }
        
        return secondLargest;
    }

    public static void main(String[] args) {
        // Example usage
        System.out.println(secondLargest(new int[]{10, 5, 8, 12, 7})); // Output: 10
        System.out.println(secondLargest(new int[]{1, 2, 3, 4, 5}));   // Output: 4
    }
}
