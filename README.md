# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
int main() {
    float length, breadth, area;
    float *ptrLength, *ptrBreadth;
    ptrLength = &length;
    ptrBreadth = &breadth;
    scanf("%f", ptrLength);
    printf("Enter the length of the rectangle: %.f\n",length);
    scanf("%f", ptrBreadth);
    printf("Enter the breadth of the rectangle: %.f\n",breadth);
    area = (*ptrLength) * (*ptrBreadth);
    printf("Area of the rectangle = %.2f\n", area);
    return 0;
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/dd65e4f6-7fc6-45e4-a790-08f71723d0c2)
		       	
## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main() {
    char *str;
    str = (char *)malloc(8 * sizeof(char)); 
    if (str == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }
    strcpy(str, "WELCOME");
    printf("%s\n", str);
    free(str);
    return 0;
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/63081375-550f-418c-8ed0-e77a2aafb45e)

## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct Student {
    int rollNumber;
    char name[50];
    float marks;
};
int main() {
    struct Student s;
    scanf("%d", &s.rollNumber);
    scanf(" %[^\n]", s.name);
    scanf("%f", &s.marks);
    printf("Student Information\n");
    printf("Roll Number : %d\n", s.rollNumber);
    printf("Name : %s\n", s.name);
    printf("Marks : %.2f\n", s.marks);
    return 0;
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/fe4d6a8c-37e4-4572-92be-4b8eeb590dea)
											
## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct Employee {
    int empId;
    char name[50];
    float basicSalary;
    float hra;
    float da;
    float grossSalary;
};
int main() {
    struct Employee emp[3];
    for (int i = 0; i < 3; i++) {
        scanf("%d", &emp[i].empId);
        scanf(" %[^\n]", emp[i].name);
        scanf("%f", &emp[i].basicSalary);
        emp[i].hra = 0.20 * emp[i].basicSalary;
        emp[i].da = 0.80 * emp[i].basicSalary;
        emp[i].grossSalary = emp[i].basicSalary + emp[i].hra + emp[i].da;
    }
    printf("\nEmployee Salary Details\n");
    for (int i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("ID           : %d\n", emp[i].empId);
        printf("Name         : %s\n", emp[i].name);
        printf("Basic Salary : %.2f\n", emp[i].basicSalary);
        printf("HRA          : %.2f\n", emp[i].hra);
        printf("DA           : %.2f\n", emp[i].da);
        printf("Gross Salary : %.2f\n", emp[i].grossSalary);
    }
    return 0;
}
```

 ## OUTPUT
![image](https://github.com/user-attachments/assets/865046f9-b464-4665-ba5f-6c6de0213def)

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.

Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.

Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.

Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].

Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.

Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.

Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.

Step 8: End the program.

## PROGRAM
```
#include <stdio.h>
struct Student {
    int rollNumber;
    char name[50];
    float marks1, marks2, marks3;
    float total, average;
};
int main() {
    struct Student s;
    scanf("%d", &s.rollNumber);
    scanf(" %[^\n]", s.name); 
    scanf("%f", &s.marks1);
    scanf("%f", &s.marks2);
    scanf("%f", &s.marks3);
    s.total = s.marks1 + s.marks2 + s.marks3;
    s.average = s.total / 3;
    printf("Student Information\n");
    printf("Roll Number : %d\n", s.rollNumber);
    printf("Name        : %s\n", s.name);
    printf("Marks 1     : %.2f\n", s.marks1);
    printf("Marks 2     : %.2f\n", s.marks2);
    printf("Marks 3     : %.2f\n", s.marks3);
    printf("Total       : %.2f\n", s.total);
    printf("Average     : %.2f\n", s.average);
    return 0;
}

```
## OUTPUT

 ![image](https://github.com/user-attachments/assets/9691698b-a90c-479e-8cbf-26c9b3057a9b)

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	
# Name: A.Nabithra
# Register Number : 212224230172

