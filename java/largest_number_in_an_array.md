## Find the largest number in an array

**Question:** Write a function to find the largest number in an array.

**Solution:**
```java
public class LargestNumber {
    public static int findLargestNumber(int[] arr) {
        int largest = Integer.MIN_VALUE;
        
        for (int num : arr) {
            if (num > largest) {
                largest = num;
            }
        }
        return largest;
    }

    public static void main(String[] args) {
        // Example usage
        System.out.println(findLargestNumber(new int[]{1, 5, 2, 9, 3})); // Output: 9
    }
}
