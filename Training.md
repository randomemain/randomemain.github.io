# **Date: 09-06-2022**
## **Session Objectives**
+ Continue Working with Conditional Constructs
+ Implementing nested if Construct
+ Understanding Menu Driven Prigramming
+ Implementing Menu Driven Programming using switch case
+ Tricky Code approach of switch case
## **Nested If**
## Syntax :
```
if(condition)
{
    if(another_condition)
        statement;
    else
        statement;
}
else
{
    if(yet_another_condition)
        statement;
    else
        statement;
}
```
## **Activity - 1**
### Write a program to evaluate the eligibility of a candidate for a position. The candidate should get an average of 80 in all the tests, the candidate gender should be male. The candidate should belongs to local region.
## Data Type : 
+ char - which stores only one character
+ float - to store the average
## Variables :
+ float avg;
+ char gender, region;
## Program Code :
```
#include <stdio.h>

int main()
{
    char gender, region;
    float avg;

    printf("Enter Gender [ M / F ]: ");
    scanf("%c", &gender);

    if (gender == 'm' || gender == 'M')
    {
        printf("Enter Avg. Marks: ");
        scanf("%f", &avg);
        getc(stdin);
        printf("Enter Region: ");
        scanf("%c", &region);
        if (region == 'l' || region == 'L' && avg >= 80)
            printf("Eligible\n");
        else
            printf("Not Eligible\n");
    }
    else
        printf("Not Eligible\n");
    
    return 0;
}
```
