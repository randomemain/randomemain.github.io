# **Date: 09-06-2022**
## **Session Objectives**

+ ### Continue Working with Conditional Constructs
+ ### Implementing nested if Construct
+ ### Understanding Menu Driven Prigramming
+ ### Implementing Menu Driven Programming using switch case
+ ### Tricky Code approach of switch case

## **Nested If**

### **Syntax :**

```c
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

## **Task - 1**

##### Write a program to evaluate the eligibility of a candidate for a position. The candidate should get an average of 80 in all the tests, the candidate gender should be male. The candidate should belongs to local region.

```c
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

## **Menu Driven Programming**

+ ### Menu is a list of options, can be selected by user in computer applications terminology.
+ ### In C we can develop menu driven applications, application allows the user to select an option from menu.
+ ### switch case is a construct to create menu driven applications
+ ### In GUI environment the Menu's are Drop Down, Pop-Up, or it can be of any other format.

## Syntax :

```c
switch(parameter)
{
    case 1:
        statemests;
        break;
    case 2:
        statements;
        break;
    :
    :
    :
    default:
        statements;
        break;
}
```

## **Task - 1**

#### A Basic Calculator using Menus

```c
#include <stdio.h>

int main()
{
    int opt, n1, n2;

    printf("Enter First Number: ");
    scanf("%d", &n1);
    printf("Enter Second Number: ");
    scanf("%d", &n2);

    printf("\n1. Add\n2. Subtract\n3. Multiply\n4. Divide\n: ");
    scanf("%d", &opt);

    printf("\nResult: ");

    switch (opt)
    {
    case 1:
        printf("%d\n", n1 + n2);
        break;
    case 2:
        printf("%d\n", n1 - n2);
        break;
    case 3:
        printf("%d\n", n1 * n2);
        break;
    case 4:
        printf("%d\n", n1 / n2);
        break;
    default:
        printf("[nil]\n");
        break;
    }

    return 0;
}
```

## **Task - 2**

#### Vowel or Consonant

```c
#include <stdio.h>

int main()
{
    char alphabet;
    printf("Enter an alphabet: ");
    scanf("%c", &alphabet);

    switch (alphabet)
    {
    case 'a':
        printf("Is a vowel\n");
        break;
    case 'e':
        printf("Is a vowel\n");
        break;
    case 'i':
        printf("Is a vowel\n");
        break;
    case 'o':
        printf("Is a vowel\n");
        break;
    case 'u':
        printf("Is a vowel\n");
        break;
    default:
        printf("Is a cosonent\n");
        break;
    }

    return 0;
}
```

# **Date: 10-06-2022**
## **Session Objectives**

+ ### Implementing Reptitive Process

### **Loop :**

+ ### A loop causes setion of a program to be repeated certain no. of times. The repetition continious as long as the loop condition holds true.
+ ### Loop Constructs are while, for, do while
+ ### Constructs based on type of Condition Ecaluations - entry loop (while loop and for loop), exit loop (do while)
+ ### Type of loop process - fixed no. of iterations, variable no. of iterations.

### **Unary Operator :**

+ ### Unary Increment  -  ```<variable_name>++ (or) ++<variable_name>```
+ ### Unary Decrement  -  ```<variable_name>-- (or) --<variable_name>```

## **Task - 1**

### Find the sum of even and odd numbers

```c
#include <stdio.h>

int main()
{
    int a[10], sum[2] = { 0 };

    printf("Enter numbers:\n");
    for (int i = 0; i < 10; i++)
    {
        printf("Element - %d: ", i + 1);
        scanf("%d", &a[i]);
    }
    
    for (int i = 0; i < 10; i++)
    {
        if (a[i] % 2) sum[0] += a[i];
        else sum[1] += a[i];
    }
    

    printf("Sum of odd numbers: %d\nSum of even numbers: %d\n", sum[0], sum[1]);

    return 0;
}
```