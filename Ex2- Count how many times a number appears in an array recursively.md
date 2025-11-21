# Ex2 Count how many times a number appears in an array recursively.
## DATE:21/11/25
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1. Start the program.
2.Read the number of elements and store them in an array.
3.Get the number to be counted from the user.
4.Define a recursive function countOccurrences() that returns how many times the number appears.
5.Use base and recursive conditions to count occurrences.
6.Display the result.
7.Stop the program.


## Program:
```
/*
Program Count how many times a number appears in an array recursively.
Developed by: MADHULEHA K
RegisterNumber:  212224060140
*/
import java.util.Scanner;

public class CountOccurrencesRecursive {
    static int countOccurrences(int arr[], int n, int key) {
        if (n == 0)
            return 0;
        return (arr[n - 1] == key ? 1 : 0) + countOccurrences(arr, n - 1, key);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();
        int arr[] = new int[n];
        System.out.println("Enter the elements:");
        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();
        System.out.print("Enter number to count: ");
        int key = sc.nextInt();
        System.out.println("The number " + key + " appears " + countOccurrences(arr, n, key) + " times.");
        sc.close();
    }
}
```

## Output:
<img width="985" height="540" alt="image" src="https://github.com/user-attachments/assets/3dc69374-711e-4628-958f-683c646f9b59" />



## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
