# Ex.No: 3 To check the number is prime or not and inspect for failures.
 
### DATE:10/04/2025                                                                            
### REGISTER NUMBER : 212222040147
### AIM: 
Write a python program to check the number is prime or not and inspect for failures.
 
### Algorithm:
1. Start the program.
2. Get the number to be checked from the user.
3. If the number is less than or equal to 1, return "Not Prime".
4. If the number is 2, return "Prime".
5. Start the iteration from 3, For each iteration:
6. If the number is divisible by the current iteration value, return "Not Prime".
7. If the number is not divisible by any value from 2 to the square root, return "Prime".
8. Stop the program.

### Program:
```
num = input("Enter a number: ")
flag = 0

if num.isnumeric():
    z = int(num)
    if z == 2:
        flag = 1
    elif z > 2:
        flag = 1
        for i in range(2, z // 2 + 1):  # Include z//2 in the range
            if z % i == 0:
                flag = 0
                break
    if flag == 1:
        print("Prime Number")
    else:
        print("Not a Prime Number")
else:
    print("Enter a Positive Number")

```
### Output:
```
Python 3.13.2 (tags/v3.13.2:4f8bb39, Feb  4 2025, 15:23:48) [MSC v.1942 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license()" for more information.

========================== RESTART: C:/python/ex 03.py =========================
Enter a number: 
========================== RESTART: C:/python/ex 03.py =========================
Enter a number: 10
Not a Prime Number

========================== RESTART: C:/python/ex 03.py =========================
Enter a number: 2
Prime Number

========================== RESTART: C:/python/ex 03.py =========================
Enter a number: string
Enter a Positive Number

========================== RESTART: C:/python/ex 03.py =========================
Enter a number: -5
Enter a Positive Number

========================== RESTART: C:/python/ex 03.py =========================
Enter a number: 
Enter a Positive Number

========================== RESTART: C:/python/ex 03.py =========================
Enter a number: A
Enter a Positive Number

========================== RESTART: C:/python/ex 03.py =========================
Enter a number: !@#
Enter a Positive Number

========================== RESTART: C:/python/ex 03.py =========================
Enter a number: 5
Prime Number

========================== RESTART: C:/python/ex 03.py =========================
Enter a number: 22/7
Enter a Positive Number

```
### Result:
Thus, the python program to check the number is prime or not is implemented and the output is verified successfully.
