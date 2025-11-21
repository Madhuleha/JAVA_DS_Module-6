# EX3 Write a program to count the number of digits in an integer.
## DATE:21/11/25
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1. Start the program.
2. Declare an integer variable n and count = 0.
3. Read the integer number n from the user.
4. If n is 0, then the count of digits is 1.
5. Otherwise, Repeat the steps while n is not equal to 0. Divide n by 10. Increment count by 1.
6. Display the value of count.
7. Stop the program.
  

## Program:
```
/*
Program to to count the number of digits in an integer
Developed by: MADHULEHA K
RegisterNumber: 212224060140  
*/
import java.util.Scanner;

public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num, count = 0;

        System.out.print("Enter an integer: ");
        num = sc.nextInt();

        if (num == 0) {
            count = 1;
        } else {
            while (num != 0) {
                num = num / 10;
                count++;
            }
        }

        System.out.println("Number of digits: " + count);
        sc.close();
    }
}
```

## Output:

<img width="543" height="180" alt="image" src="https://github.com/user-attachments/assets/b8f08758-da73-401b-aada-3370e0cd393e" />


## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
