# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE:21/11/25
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Start the program.
Read the number of elements and store them in an array.
3.Define a recursive function findMin() that compares elements to find the minimum.
4.Base condition: If the array has one element, return that element.
5.Recursive step: Compare the last element with the minimum of the rest of the array and return the smaller one.
6.Display the minimum value.
7.Stop the program.
  

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: MADHULEHA K
RegisterNumber:  212224060140
*/
import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n) {
        if (i == n - 1) {
            return arr[i];
        }
        int minRest = getMin(arr, i + 1, n);
        return Math.min(arr[i], minRest);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}
```

## Output:

<img width="405" height="177" alt="image" src="https://github.com/user-attachments/assets/5036a7da-b9cc-469e-97a3-dadcaeb89def" />


## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
