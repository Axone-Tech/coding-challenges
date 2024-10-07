## Implement a function to find the missing number in an array of 1 to N

**Question:** Given an array containing n distinct numbers taken from 0, 1, 2, ..., n, find the one that is missing from the array.

**Solution:**
```java
public class MissingNumber {
    public static int findMissingNumber(int[] nums) {
        int n = nums.length;

        // Calculate the expected sum of numbers from 0 to n
        int expectedSum = (n * (n + 1)) / 2;

        // Calculate the actual sum of the array
        int actualSum = 0;
        for (int num : nums) {
            actualSum += num;
        }

        // The difference is the missing number
        return expectedSum - actualSum;
    }

    public static void main(String[] args) {
        // Example usage
        System.out.println(findMissingNumber(new int[]{3, 0, 1})); // Output: 2
        System.out.println(findMissingNumber(new int[]{9, 6, 4, 2, 3, 5, 7, 0, 1})); // Output: 8
    }
}
