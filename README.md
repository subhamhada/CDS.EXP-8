# EXPERIMENT-8
## AIM
To study and implement C++ 2D array matrices

## THEORY
Matrices in C++ are represented as 2D arrays. They are used to store and manipulate data in a structured, tabular form.

### 1.Introduction to Matrices :
A matrix is a collection of elements arranged in rows and columns.<br>
In C++, matrices are typically implemented using 2D arrays.

### 2.Declaration :
Matrix Declaration Using 2D Arrays (Static Allocation).<br>This is useful when the size of the matrix is known at compile time.
```
// Declaration of a 3x3 matrix
int matrix[3][3];
```

### 3Initialization of Matrix :
Matrix can be initialized using a 2D array either by assigning values explicitly during declaration or by using loops to assign values later.
```
    // Initializing a 3x3 matrix
    int matrix[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };
```
### 4.Accessing Elements of a Matrix :
In C++, you can access elements of a matrix (2D array) using row and column indices.
```
int value = matrix[1][2];
```

### 5.Addition of Matrix :
To perform matrix addition using 2D arrays in C++:

1. *Matrix Dimensions*: Both matrices must have the same dimensions (same number of rows and columns).
2. *Create Two Matrices*: Define two 2D arrays representing the matrices to be added.
3. *Result Matrix*: Create a third 2D array to store the result of the addition.
4. *Addition Process*: Use nested loops to iterate over each element of both matrices, adding corresponding elements together.
5. *Store Result*: Store the sum of corresponding elements from the two matrices in the result matrix.

The result matrix will contain the sum of the two input matrices, element by element.

### 6.Subtraction of Matrix :
Matrix subtraction in C++ using 2D arrays follows a similar process to matrix addition.<br>
To subtract two matrices, you subtract corresponding elements of each matrix.<br> Both matrices must have the same dimensions.

1. *Same Dimensions*: Ensure both matrices have the same number of rows and columns.
2. *Two Matrices*: Define two 2D arrays to represent the matrices.
3. *Result Matrix*: Create a 2D array to store the result of the subtraction.
4. *Subtraction Process*: Use nested loops to iterate through both matrices, subtract corresponding elements.
5. *Store the Difference*: Store the difference in the result matrix.

The resulting matrix will store the difference of the two input matrices, element by element.

### 7.Multiplication of Matrix :
1. *Check Dimensions*: Ensure the number of columns in the first matrix equals the number of rows in the second matrix.

2. *Initialize Result Matrix*: Create a matrix with dimensions of rows from the first matrix and columns from the second matrix.

3. *Perform Multiplication*:
   - Iterate through rows of the first matrix.
   - Iterate through columns of the second matrix.
   - Compute the dot product of the current row and column.
   - Store the result in the corresponding position in the result matrix.

### 8.Transpose of Matrix :
1. *Create a New Matrix*: Initialize a matrix with dimensions swapped (rows become columns and vice versa).

2. *Assign Values*:
   - Iterate through the original matrix’s columns.
   - For each column, iterate through its rows.
   - Assign values to the new matrix based on the current column and row indices.
  
## Codes -
### 1.*Entering elements of matrix -*
```
//subham
//entc B2
//23070123132
//experiment 8
#include<iostream>
using namespace std;
int main()
{
    int temp[3][3],i,j,k,l;
    for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            cout<<"enter element- ("<<i<<j<<"): ";
            cin>>temp[i][j];
        }
    }
    for(k=0;k<3;k++)
    {
        for(l=0;l<3;l++)
        {
            cout<<temp[k][l];
            cout<<" ";
        }
    }    
    return 0;
}
```

### 2.*Addition of two matrices -*
```
//subham
//entc B2
//23070123132
//experiment 8
#include <iostream>
using namespace std;
int main() 
{
    // Define matrix dimensions
    int r1 = 3, c1 = 3;
    int r2 = 3, c2 = 3;

    int m1[r1][c1], m2[r2][c2], sum[r1][c1];

    cout << "Enter elements of the first matrix:" << endl;
    for (int i = 0; i < r1; ++i) 
    {
        for (int j = 0; j < c1; ++j) 
        {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m1[i][j];
        }
    }
    cout << "Enter elements of the second matrix:" << endl;
    for (int i = 0; i < r2; ++i) 
    {
        for (int j = 0; j < c2; ++j) 
        {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m2[i][j];
        }
    }

    for (int i = 0; i < r1; ++i) 
    {
        for (int j = 0; j < c1; ++j) 
        {
            sum[i][j] = m1[i][j] + m2[i][j];
        }
    }
 

    cout << endl << "Sum of matrices:" << endl;
    for (int i = 0; i < r1; ++i) 
    {
        for (int j = 0; j < c1; ++j) 
        {
            cout << sum[i][j] << "/t";
        }
        cout << endl;
    }

    return 0;
}
```

### 3.*Subtraction of two matrices -*
```
//subham
//entc B2
//23070123132
//experiment 8
#include <iostream>
using namespace std;
int main() 
{
    // Define matrix dimensions
    int r1 = 3, c1 = 3;
    int r2 = 3, c2 = 3;

    int m1[r1][c1], m2[r2][c2], sum[r1][c1];

    cout << "Enter elements of the first matrix:" << endl;
    for (int i = 0; i < r1; ++i) 
    {
        for (int j = 0; j < c1; ++j) 
        {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m1[i][j];
        }
    }
    cout << "Enter elements of the second matrix:" << endl;
    for (int i = 0; i < r2; ++i) 
    {
        for (int j = 0; j < c2; ++j) 
        {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m2[i][j];
        }
    }

    for (int i = 0; i < r1; ++i) 
    {
        for (int j = 0; j < c1; ++j) 
        {
            sum[i][j] = m1[i][j] - m2[i][j];
        }
    }
 

    cout << endl << "difference of matrices:" << endl;
    for (int i = 0; i < r1; ++i) 
    {
        for (int j = 0; j < c1; ++j) 
        {
            cout << sum[i][j] << "/t";
        }
        cout << endl;
    }

    return 0;
}
```

### 4.*Multiplication of two matrices -*
```
//subham
//entc B2
//23070123132
//experiment 8
// Matrix multiplication 
#include <iostream>
using namespace std;

int main() {
    int r1, c1, r2, c2;
    
    // Input dimensions of the first matrix
    cout << "Enter rows and columns for the first matrix: ";
    cin >> r1 >> c1;

    // Input dimensions of the second matrix
    cout << "Enter rows and columns for the second matrix: ";
    cin >> r2 >> c2;

    // Check if matrix multiplication is possible
    if (c1 != r2) {
        cout << "Matrix multiplication not possible!" << endl;
        return 0;
    }

    // Define the matrices
    int m1[r1][c1], m2[r2][c2], result[r1][c2];

    // Input elements of the first and second matrix
    cout << "Enter elements of the first matrix:" << endl;
    for (int i = 0; i < r1; ++i) {
        for (int j = 0; j < c1; ++j) {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m1[i][j];
        }
    }
    cout << "Enter elements of the second matrix:" << endl;
    for (int i = 0; i < r2; ++i) {
        for (int j = 0; j < c2; ++j) {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m2[i][j];
        }
    } 
    // Initialize the result matrix with zeros
    for (int i = 0; i < r1; i++) {
        for (int j = 0; j < c2; j++) {
            result[i][j] = 0;
        }
    }

    // Matrix multiplication
    for (int i = 0; i < r1; i++) {
        for (int j = 0; j < c2; j++) {
            for (int k = 0; k < c1; k++) {
                result[i][j] += m1[i][k] * m2[k][j];
            }
        }
    }

    // Display the result
    cout << "Resultant matrix:\n";
    for (int i = 0; i < r1; i++) {
        for (int j = 0; j < c2; j++) {
            cout << result[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```

### 5.*Transpose of a matrix -*
```
//subham
//entc B2
//23070123132
//experiment 8
//TRANSPOSE OF MATRIX 
#include <iostream>
using namespace std;

int main() {
    int r, c ;

    // Getting the size of the matrix
    cout << "Enter the number of rows and columns of the matrix: ";
    cin >> r  >> c ;

    int m[r][c], transpose[c][r];

    // Getting elements of the matrix
    cout << "Enter elements of the first matrix:" << endl;
    for (int i = 0; i < r; ++i) {
        for (int j = 0; j < c; ++j) {
            cout << "Enter element at position (" << i << ", " << j << "): ";
            cin >> m[i][j];
        }
    }

    // Transposing the matrix
    for(int i = 0; i < r; ++i) {
        for(int j = 0; j < c; ++j) {
            transpose[j][i] = m[i][j];
        }
    }

    // Displaying the transpose of the matrix
    cout << "\nTranspose of the matrix:" << endl;
    for(int i = 0; i < c; ++i) {
        for(int j = 0; j < r; ++j) {
            cout << transpose[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```

### 6. *Diagnol addition of a matrix -*
```
//subham
//entc B2
//23070123132
//experiment 8
//DIAGONAL ADDITION 
#include <iostream>
using namespace std;


const int MAX = 100;

void printDiagonalSums(int mat[][MAX], int n) 
{ 
    int principal = 0;
    
    for (int i = 0; i < n; i++)  
    { 
        // Condition for principal diagonal 
        principal += mat[i][i]; 
    } 
  
    cout << "Sum of the diagonal elements is: " << principal << endl; 
} 

int main() 
{ 
    int a[][MAX] = {{1, 2, 3, 4},  
                    {5, 6, 7, 8},  
                    {1, 2, 3, 4},  
                    {5, 6, 7, 8}}; 
    printDiagonalSums(a, 4); 
return 0;
}
```

## Output -
### 1.*Entering elements of matrix -*
![Screenshot 2024-08-21 011748](https://github.com/user-attachments/assets/9f4a6edc-39e5-4c7e-b6a3-22779db2d19b)

### 2.*Addition of two matrices -*
![Screenshot 2024-08-21 011910](https://github.com/user-attachments/assets/bf7c36d7-f6d8-4d2f-b8c0-83ffaea3a160)

### 3.*Subtraction of two matrices -*
![Screenshot 2024-08-21 012036](https://github.com/user-attachments/assets/3cc80b95-9060-43db-8463-5bd7dd6603f8)

### 4.*Multiplication of two matrices -*
![Screenshot 2024-08-21 012201](https://github.com/user-attachments/assets/a1f5e716-f137-4a54-ba1e-43f480442fc8)

### 5.*Transpose of a matrix -*
![Screenshot 2024-08-21 012244](https://github.com/user-attachments/assets/3926da44-3a25-44b9-9e18-3ee3feeffe28)

### 6. *Diagnol addition of a matrix -*
![Screenshot 2024-08-21 012317](https://github.com/user-attachments/assets/b1f51561-c508-4186-910f-290b32492355)

## Conclusion -
This experiment provides valuable insight into fundamental concepts in programming, particularly in handling data structures that require multi-dimensional organization. Through this process, we gain a deeper understanding of how to: <br>

* Efficiently Store and Manipulate Data: Using 2D arrays, we can efficiently store data in a tabular format, making it easier to perform operations like addition, subtraction, and multiplication of matrices.

* Develop Problem-Solving Skills: Implementing matrix operations enhances logical thinking and problem-solving skills, as it requires careful consideration of indices, loops, and data handling.

* Understand Memory Management: Working with 2D arrays in C++ also provides an understanding of how memory is allocated and accessed in programming, especially in managing rows and columns of data.
