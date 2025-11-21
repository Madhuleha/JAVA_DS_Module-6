# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE:21/11/25
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Start the program.
2.Declare two 2D arrays, A and B, of the same size.
3.Initialize Matrix A with all odd numbers and Matrix B with all even numbers.
4.Create another 2D array C to store the sum of corresponding elements of A and B.
5.For each element position (i, j): Compute C[i][j] = A[i][j] + B[i][j].

## Program:
```
/*
Program to ind the nature of resultant matrrix.
Developed by: MADHULEHA K
RegisterNumber:  212224060140
*/
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
    
        int a=sc.nextInt();
        int b=sc.nextInt();
        int[][] row=new int[a][b];
        int[][] col=new int[a][b];
        int[][] res=new int[a][b];
        for(int i=0;i<a;i++){
            for(int j=0;j<b;j++){
                row[i][j]=sc.nextInt();
            }
        }
    
        for(int i=0;i<a;i++){
            for(int j=0;j<b;j++){
                col[i][j]=sc.nextInt();
            }
        }
    
        for(int i=0;i<a;i++){
            for(int j=0;j<b;j++){
                res[i][j]=row[i][j]+col[i][j];
            }
        }
    
        for(int i=0;i<a;i++){
            for(int j=0;j<b;j++){
                System.out.print(res[i][j]);
                if(j<b-1){
                    System.out.print(" ");
                }
            
            }
            System.out.println();
        }
    }
}
```

## Output:

<img width="374" height="546" alt="image" src="https://github.com/user-attachments/assets/b1cedd6a-9b7c-4781-bafe-7074099b6cd0" />


## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
