# Ex.No: 2   Matrix Multiplication 

### DATE: 27/03/2025                                                                           
### REGISTER NUMBER : 212222040147

### AIM: 
Write a python program for matrix multiplication and inspect for failures.
 
### Algorithm:

Algorithm:
1. Start the program.
2. Create empty list formatrix1, matrix2 and result.
3. Get the rows and columns count from the user.
4. Get the values of two matrix.
5. Perform matrix multiplication and store the answer in result.
6. Stop the program.
### Program:
```
r1, c1 = input("Enter row and column count in matrix 1: ").split()
r2, c2 = input("Enter row and column count in matrix 2: ").split()

if r1.isnumeric() and c1.isnumeric() and r2.isnumeric() and c2.isnumeric():
    r1 = int(r1)
    c1 = int(c1)
    r2 = int(r2)
    c2 = int(c2)
    if c1 != r2:
        print("Matrix multiplication not possible: column of matrix 1 must equal row of matrix 2")
    elif max(r1, c1, r2, c2) > 20 or min(r1, c1, r2, c2) == 0:
        print("Matrix multiplication not possible: dimensions must be between 1 and 20")
    else:
        matrix1 = []
        matrix2 = []
        result = []

        print("Enter elements for Matrix 1:")
        for i in range(r1):
            a = []
            for j in range(c1):
                a.append(int(input(f"Matrix1[{i}][{j}]: ")))
            matrix1.append(a)

        print("Enter elements for Matrix 2:")
        for i in range(r2):
            a = []
            for j in range(c2):
                a.append(int(input(f"Matrix2[{i}][{j}]: ")))
            matrix2.append(a)
        for i in range(r1):
            inter = []
            for j in range(c2):
                total = 0
                for k in range(c1):  
                    total += matrix1[i][k] * matrix2[k][j]
                inter.append(total)
            result.append(inter)

        print("Result of matrix multiplication:")
        for row in result:
            print(" ".join(map(str, row)))
else:
    print("Enter valid numeric values for rows and columns.")

```












### Output:

```
=================== RESTART: C:/Users/DELL/Downloads/ex 02.py ==================
Enter row and column count in matrix 1: 2 3
Enter row and column count in matrix 2: 2 3
Matrix multiplication not possible: column of matrix 1 must equal row of matrix 2

=================== RESTART: C:/Users/DELL/Downloads/ex 02.py ==================
Enter row and column count in matrix 1: p q 
Enter row and column count in matrix 2: q s
Enter valid numeric values for rows and columns.

=================== RESTART: C:/Users/DELL/Downloads/ex 02.py ==================
Enter row and column count in matrix 1: 1.5 2
Enter row and column count in matrix 2: 2 3
Enter valid numeric values for rows and columns.

=================== RESTART: C:/Users/DELL/Downloads/ex 02.py ==================
Enter row and column count in matrix 1: 350 480
Enter row and column count in matrix 2: 480 620
Matrix multiplication not possible: dimensions must be between 1 and 20
```




### Result:
Thus, the python program for matrix multiplication is implemented and the causes for its failure is introspected successfully.

