# Ex5 Count Inversions in an Array
## DATE:21/11/25
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Start the program.
2.Declare an array arr[] and a variable count = 0 to store the number of inversions.
3.Read the array elements from the user.
4.For each pair of elements (arr[i], arr[j]), check if arr[i] > arr[j] and i < j.
5.If the above condition is true, increment the inversion count.
6.Continue until all pairs are checked.
7.Display the total number of inversions found in the array and stop the program.


## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: MADHULEHA K
RegisterNumber:  212224060140
*/
import java.util.Scanner;

public class CountInversions {
    public static int mergeSortAndCount(int[] arr, int left, int right) {
        int count = 0;
        if (left < right) {
            int mid = (left + right) / 2;
            count += mergeSortAndCount(arr, left, mid);
            count += mergeSortAndCount(arr, mid + 1, right);
            count += mergeAndCount(arr, left, mid, right);
        }
        return count;
    }

    private static int mergeAndCount(int[] arr, int left, int mid, int right) {
        int[] leftArr = new int[mid - left + 1];
        int[] rightArr = new int[right - mid];

        for (int i = 0; i < leftArr.length; i++) leftArr[i] = arr[left + i];
        for (int i = 0; i < rightArr.length; i++) rightArr[i] = arr[mid + 1 + i];

        int i = 0, j = 0, k = left, swaps = 0;

        while (i < leftArr.length && j < rightArr.length) {
            if (leftArr[i] <= rightArr[j]) {
                arr[k++] = leftArr[i++];
            } else {
                arr[k++] = rightArr[j++];
                swaps += (leftArr.length - i); // Count inversions
                
            }
       
        }

        while (i < leftArr.length) arr[k++] = leftArr[i++];
        while (j < rightArr.length) arr[k++] = rightArr[j++];

        return swaps;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) arr[i] = sc.nextInt();
        System.out.println(mergeSortAndCount(arr, 0, n - 1));
    }
}
```

## Output:
<img width="357" height="240" alt="image" src="https://github.com/user-attachments/assets/3a8756cc-1a53-4f35-9e81-9691484719d2" />



## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
