
# EX-01-Datatypes-Operators
## AIM:
Write a C program to read 3 characters one by one and print the characters in a reverse order.

## ALGORITHM:
1.	Declare three character variables to store the input characters.
2.	Use the scanf function to read the characters one by one from the user.
3.	Print the characters in reverse order using the printf function.
4.	End the program.

## PROGRAM:
```c
#include <stdio.h>

int main() {
    char ch1, ch2, ch3;

    // Read 3 characters one by one
    printf("Enter first character: ");
    scanf(" %c", &ch1);  // space before %c to skip any leftover newline

    printf("Enter second character: ");
    scanf(" %c", &ch2);

    printf("Enter third character: ");
    scanf(" %c", &ch3);

    // Print characters in reverse order
    printf("Characters in reverse order: %c %c %c\n", ch3, ch2, ch1);

    return 0;
}

```
## OUTPUT:
<img width="1270" height="556" alt="image" src="https://github.com/user-attachments/assets/9b47c934-ee4f-4cc6-8a58-bc8b1373d1c1" />


















## RESULT:
Thus the program to read 3 characters one by one and print the characters in a reverse order has been executed successfully.


# EX-02- Conditional-Statements
## AIM:
Write a C program to read A values and check whether A is positive number or not.

# ALGORITHM:
1.	Declare a variable to store the input value A.
2.	Use the scanf function to read the value of A from the user.
3.	Check if the value of A is greater than zero.
4.	If A is greater than zero, print a message indicating that it's a positive number. 
5.	Otherwise, print a message indicating that it's not a positive number.
6.End the program.

# PROGRAM:
```c
#include <stdio.h>

int main() {
    int A;

    // Read the number
    printf("Enter a number: ");
    scanf("%d", &A);

    // Check whether A is positive or not
    if (A > 0)
        printf("%d is a positive number.\n", A);
    else
        printf("%d is not a positive number.\n", A);

    return 0;
}

```

# OUTPUT:
<img width="1264" height="480" alt="image" src="https://github.com/user-attachments/assets/fce3b1c6-3c5b-41a5-baca-b84737610566" />












# RESULT:
Thus the program to read A values and check whether A is positive number or not has been executed successfully.
 
 
 


# EX-03- Operators-Expressions
## AIM:
Write a program to find minimum between two fraction numbers using conditional operator or ternary operator.

## ALGORITHM:
1.	Declare variables to store the two fraction numbers and the result.
2.	Use the printf function to prompt the user to enter the first fraction number (numerator and denominator separately).
3.	Use the scanf function to read the numerator and denominator of the first fraction.
4.	Repeat steps 2 and 3 to get the second fraction from the user.
5.	Calculate the decimal values of both fractions by dividing the numerators by the denominators.
6.	Use the conditional (ternary) operator to compare the decimal values and store the minimum value in the result variable.
7.	Print the minimum value.

## PROGRAM:
```c
#include <stdio.h>

int main() {
    float num1, num2, min;

    // Read two fractional numbers
    printf("Enter first number: ");
    scanf("%f", &num1);

    printf("Enter second number: ");
    scanf("%f", &num2);

    // Find minimum using ternary operator
    min = (num1 < num2) ? num1 : num2;

    // Display the result
    printf("Minimum number = %.2f\n", min);

    return 0;
}

```

## OUTPUT:
<img width="1252" height="489" alt="image" src="https://github.com/user-attachments/assets/d65f2d7a-2e16-4350-bd18-25bcb15a3898" />










## RESULT:
Thus the program to find minimum between two fraction numbers using conditional operator or ternary operator has been executed successfully.




# EX-04- Using Conditional Statements

## AIM:
Write a C program to check whether the input value is equal to 1 using simple if statement

## ALGORITHM:
1.	Declare a variable to store the input value.
2.	Use the scanf function to read the input value from the user.
3.	Use an if statement to check if the input value is equal to 1.
4.	If the condition in the if statement is true, print a message indicating that the input value is equal to 1.
5.	Otherwise, print a message indicating that it's not equal to 1.
6.	End the program.

## PROGRAM:
```c
#include <stdio.h>

int main() {
    int num;

    // Read a number from user
    printf("Enter a number: ");
    scanf("%d", &num);

    // Check whether the number is equal to 1
    if (num == 1)
        printf("The number is equal to 1.\n");

    return 0;
}

```

## OUTPUT:
<img width="1257" height="478" alt="image" src="https://github.com/user-attachments/assets/1c0b678d-88ac-41ee-b24b-67241bccc3cb" />










	

## RESULT:
Thus the program to check whether the input value is equal to 1 using simple if statement has been executed successfully



# EX-05- Calculating Total, Percentage, And Division Using Conditional Statements 
## AIM:
To write a C program that reads marks of three subjects, calculates the total and percentage, and then determines the division (First, Second, Pass, or Fail) based on the percentage and minimum marks criteria.
## ALGORITHM:
1.	Start
2.	Declare integer variables m1, m2, m3 for marks, and float variables tot, per.
3.	Input the marks for three subjects.
4.	Calculate total marks: tot = m1 + m2 + m3
5.	Calculate percentage: per = tot / 3
6.	Display total and percentage.
7.	Check if all marks are greater than or equal to 40:
8.	If yes:
a.	If percentage >= 60: Print “Division = First”
b.	Else if percentage >= 48: Print “Division = Second”
c.	Else if percentage >= 36: Print “Division = Pass”
9.	Else: Print “Division = Fail”
10.	End
## PROGRAM:
```c
#include <stdio.h>

int main() {
    float sub1, sub2, sub3, total, percentage;

    // Read marks of three subjects
    printf("Enter marks of three subjects: ");
    scanf("%f %f %f", &sub1, &sub2, &sub3);

    // Calculate total and percentage
    total = sub1 + sub2 + sub3;
    percentage = (total / 300) * 100;  // assuming each subject is out of 100

    // Check minimum marks criteria (e.g., pass mark = 35 per subject)
    if (sub1 < 35 || sub2 < 35 || sub3 < 35) {
        printf("Result: Fail (One or more subjects below 35)\n");
    } 
    else {
        // Determine division based on percentage
        if (percentage >= 60)
            printf("Division: First (%.2f%%)\n", percentage);
        else if (percentage >= 50)
            printf("Division: Second (%.2f%%)\n", percentage);
        else if (percentage >= 35)
            printf("Division: Pass (%.2f%%)\n", percentage);
        else
            printf("Result: Fail (%.2f%%)\n", percentage);
    }

    // Display total and percentage
    printf("Total Marks = %.2f\n", total);
    printf("Percentage = %.2f%%\n", percentage);

    return 0;
}
```

## OUTPUT:
<img width="1161" height="664" alt="image" src="https://github.com/user-attachments/assets/17e4cd29-9969-41e9-957e-767e38f0664e" />


## RESULT:
The program successfully takes three subject marks, calculates the total and percentage, and correctly determines the division based on predefined grading logic.

