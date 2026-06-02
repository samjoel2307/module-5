# EX-26-AREA-OF-RECTANGLE-USING- POINTER

## NAME: B.SAM JOEL JOSHUA

## REGISTER NO: 212225230242

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
#include<stdio.h>
int main()
{
    int num1,num2;
    scanf("%d %d",&num1,&num2);
    int *ptr1=&num1,*ptr2=&num2;
    printf("\n Area of Rectangle = %d units",*ptr1**ptr2);
    return 0;
}
```
## OUTPUT
		       	
<img width="902" height="232" alt="Screenshot 2026-03-26 144308" src="https://github.com/user-attachments/assets/f864d26e-2a2d-421b-ac1a-775efd3ee07a" />


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
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int main()
{
    char str[7]="WELCOME";
    char*ptr=malloc(strlen(str)*sizeof(char));
    for(int i=0;i<7;i++)
    {
        ptr[i]=str[i];
    }
    for(int i=0;i<7;i++)
    {
        printf("%c",ptr[i]);
    }
    free(ptr);
    return 0;
}
```
## OUTPUT

<img width="340" height="108" alt="Screenshot 2026-03-26 144352" src="https://github.com/user-attachments/assets/ce92648b-02bc-4916-a908-a8a4de88c2cb" />


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully.



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
#include<stdio.h>
struct student
{
    char name[30];
    int roll_no;
    int m1,m2,m3;
}obj[3];
int main()
{
    for(int i=0;i<3;i++)
    {
        scanf("%s",obj[i].name);
        scanf("%d",&obj[i].roll_no);
        scanf("%d %d %d",&obj[i].m1,&obj[i].m2,&obj[i].m3);
    }
    for(int i=0;i<3;i++)
    {
        printf("\nStudent Name: %s",obj[i].name);
        printf("\nStudent Roll_No: %d",obj[i].roll_no);
        printf("\nMarks:");
        printf("\nm1= %d\nm2= %d\nm3= %d\n",obj[i].m1,obj[i].m2,obj[i].m3);
    }
    return 0;
}
```
## OUTPUT

<img width="278" height="181" alt="Screenshot 2026-03-26 144600" src="https://github.com/user-attachments/assets/a946f4a3-f419-481c-b402-45806d1b530e" />
<img width="243" height="175" alt="Screenshot 2026-03-26 144556" src="https://github.com/user-attachments/assets/2faf2244-6496-4b6e-8787-81fe5827cf82" />
<img width="779" height="403" alt="Screenshot 2026-03-26 144549" src="https://github.com/user-attachments/assets/66a47d85-9374-4351-86ce-e9c70120c4e9" />


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
#include<stdio.h>
struct details
{
    int no;
    char name[30];
    float price;
}obj[3];
int main()
{
    for(int i=0;i<3;i++)
    {
    scanf("%d",&obj[i].no);
    scanf("%s",obj[i].name);
    scanf("%f",&obj[i].price);
    }
    printf("Details of the Employee:\n");
    for(int i=0;i<3;i++)
    {
        printf("%d    ",obj[i].no);
        printf("%s           ",obj[i].name);
        printf("%.0f    ",obj[i].price);
        printf("%.0f    ",obj[i].price*10/100);
        printf("%.0f    ",obj[i].price*30/100);
        printf("%.2f    ",obj[i].price+obj[i].price*10/100+obj[i].price*30/100);
        printf("\n");
    }
    return 0;
}
```
 ## OUTPUT

<img width="879" height="343" alt="Screenshot 2026-03-26 144921" src="https://github.com/user-attachments/assets/ec65591d-0dd9-48c4-8d0a-12c3b6416947" />


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
#include<stdio.h>
struct student
{
    char name[10];
    int roll_no;
    int mark[5];
    int total;
    float average;
}stu[2];
int main()
{
    int itr;
    for(itr=0;itr<2;itr++)
    {
        scanf("%s",stu[itr].name);
        scanf("%d",&stu[itr].roll_no);
        for(int j=0;j<5;j++)
        {
            scanf("%d",&stu[itr].mark[j]);
        }
    }
    for(itr=0;itr<2;itr++)
    {
        stu[itr].total=0;
        printf("\nStudent Name: %s",stu[itr].name);
        printf("\nStudent Roll No: %d",stu[itr].roll_no);
        printf("\nMarks:");
        for(int j=0;j<5;j++)
        {
            printf("%d ",stu[itr].mark[j]);
            stu[itr].total+=stu[itr].mark[j];
        }
        printf("\nTotal Marks: %d",stu[itr].total);
        stu[itr].average=stu[itr].total/5;
        printf("\nAverage: %.2f",stu[itr].average);
        printf("\n");
    }
    return 0;
}
```
## OUTPUT

<img width="832" height="455" alt="Screenshot 2026-03-26 192905" src="https://github.com/user-attachments/assets/a883dc04-5525-4480-8f18-b5bd63a70dc8" />


## RESULT
Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


