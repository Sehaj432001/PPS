# Name: Sehajpreet Kaur #
# Branch : CSE 'B' #
# Roll No: 1915072 #

# C Programs : #

## 1. Addition of Two Numbers 

>#include<stdio.h>
     
    int main()
    {
       int a, b, c;
       
       printf("Enter two numbers to add\n");
       scanf("%d%d", &a, &b);
       
       c = a + b;
       
       printf("Sum of the numbers = %d\n", c);
       
       return 0;
    }

## 2. Average of N numbers
```C#include<stdio.h>

int main()
{
    printf("\n\n\t\tStudytonight - Best place to learn\n\n\n");

    int n, i;
    float sum = 0, x;

    printf("Enter number of elements:  ");
    scanf("%d", &n);
    printf("\n\n\nEnter %d elements\n\n", n);
    for(i = 0; i < n; i++)
    {
        scanf("%f", &x);
        sum += x;
    }
    printf("\n\n\nAverage of the entered numbers is =  %f", (sum/n));
    printf("\n\n\n\n\t\t\tCoding is Fun !\n\n\n");
    return 0;
}```
 
## 3.WeekDays
```C#include <stdio.h>

int main()
{
    int week;
    
    /* Input week number from user */
    printf("Enter week number(1-7): ");
    scanf("%d", &week);
    
    switch(week)
    {
        case 1: 
            printf("Monday");
            break;
        case 2: 
            printf("Tuesday");
            break;
        case 3: 
            printf("Wednesday");
            break;
        case 4: 
            printf("Thursday");
            break;
        case 5: 
            printf("Friday");
            break;
        case 6: 
            printf("Saturday");
            break;
        case 7: 
            printf("Sunday");
            break;
        default: 
            printf("Invalid input! Please enter week number between 1-7.");
    }

    return 0;

    
}```
## 4.Even odd:
    ```C#include <stdio.h>
    int main()
    {
        int number;
        printf("Enter an integer: ");
        scanf("%d", &number);
        // True if the number is perfectly divisible by 2
        if(number % 2 == 0)
            printf("%d is even.", number);
        else
            printf("%d is odd.", number);
        return 0;
    }```
 
## 5. Table:
    ```C#include <stdio.h>
    int main()
    {
        int n, i;
        printf("Enter an integer: ");
        scanf("%d",&n);
        for(i=1; i<=10; ++i)
        {
            printf("%d * %d = %d \n", n, i, n*i);
        }
        
        return 0;
    }```
## 6. Armstrong Number
    ```C#include <stdio.h>
    int main()
    {
        int number, originalNumber, remainder, result = 0;
        printf("Enter a three digit integer: ");
        scanf("%d", &number);
        originalNumber = number;
        while (originalNumber != 0)
        {
            remainder = originalNumber%10;
            result += remainder*remainder*remainder;
            originalNumber /= 10;
        }
        if(result == number)
            printf("%d is an Armstrong number.",number);
        else
            printf("%d is not an Armstrong number.",number);
        return 0;
    }```
 ## 7.Calculator:
  ```C#include <stdio.h>
int main() {
    char operator;
    double firstNumber,secondNumber;
    printf("Enter an operator (+, -, *,): ");
    scanf("%c", &operator);
    printf("Enter two operands: ");
    scanf("%lf %lf",&firstNumber, &secondNumber);
    switch(operator)
    {
        case '+':
            printf("%.1lf + %.1lf = %.1lf",firstNumber, secondNumber, firstNumber + secondNumber);
            break;
        case '-':
            printf("%.1lf - %.1lf = %.1lf",firstNumber, secondNumber, firstNumber - secondNumber);
            break;
        case '*':
            printf("%.1lf * %.1lf = %.1lf",firstNumber, secondNumber, firstNumber * secondNumber);
            break;
        case '/':
            printf("%.1lf / %.1lf = %.1lf",firstNumber, secondNumber, firstNumber / secondNumber);
            break;
        // operator doesn't match any case constant (+, -, *, /)
        default:
            printf("Error! operator is not correct");
    }
    
    return 0;
}```

## 8. Bubble Sort:
     ```C
    #include <stdio.h>
     
    int main()
    {
      int array[100], n, c, d, swap;
     
      printf("Enter number of elements\n");
      scanf("%d", &n);
     
      printf("Enter %d integers\n", n);
     
      for (c = 0; c < n; c++)
        scanf("%d", &array[c]);
     
      for (c = 0 ; c < n - 1; c++)
      {
        for (d = 0 ; d < n - c - 1; d++)
        {
          if (array[d] > array[d+1]) /* For decreasing order use < */
          {
            swap       = array[d];
            array[d]   = array[d+1];
            array[d+1] = swap;
          }
        }
      }
     
      printf("Sorted list in ascending order:\n");
     
      for (c = 0; c < n; c++)
         printf("%d\n", array[c]);
     
      return 0;
    
}
```

## 9. Binary Search:
```C
    #include <stdio.h>
     
    int main()
    {
       int c, first, last, middle, n, search, array[100];
     
       printf("Enter number of elements\n");
       scanf("%d",&n);
     
       printf("Enter %d integers\n", n);
     
       for (c = 0; c < n; c++)
          scanf("%d",&array[c]);
     
       printf("Enter value to find\n");
       scanf("%d", &search);
     
       first = 0;
       last = n - 1;
       middle = (first+last)/2;
     
       while (first <= last) {
          if (array[middle] < search)
             first = middle + 1;    
          else if (array[middle] == search) {
             printf("%d found at location %d.\n", search, middle+1);
             break;
          }
          else
             last = middle - 1;
     
          middle = (first + last)/2;
       }
       if (first > last)
          printf("Not found! %d isn't present in the list.\n", search);
     
       return 0;  
    }```   
## 10.Factorial:
```C
    #include <stdio.h>
     
    int main()
    {
      int c, n, fact = 1;
     
      printf("Enter a number to calculate its factorial\n");
      scanf("%d", &n);
     
      for (c = 1; c <= n; c++)
        fact = fact * c;
     
      printf("Factorial of %d = %d\n", n, fact);
     
      return 0;
    }
    ```
## 11.FizzBuzz
```C
#include <stdio.h>

int main(void)
{
    int i;
    for(i=1; i<=100; i++)
    {
        if(((i%3)||(i%5))== 0)
            printf("number= %d FizzBuzz\n", i);
        else if((i%3)==0)
            printf("number= %d Fizz\n", i);
        else if((i%5)==0)
            printf("number= %d Buzz\n", i);
        else
            printf("number= %d\n",i);

    }

    return 0;
}
```
## 12.Sum of First 100 Numbers:
```C
#include <stdio.h>
int main()
{
    int n, i, sum = 0;
    
    printf("Enter a positive integer: ");
    scanf("%d",&n);
    for(i=1; i <= 100; ++i)
    {
        sum += i;   // sum = sum+i;
    }
    printf("Sum = %d",sum);
    return 0;
}
```
## 13.Greater of two Numbers:
```C
#include<stdio.h>
#include<conio.h>
int main()
{
    int a, b, big;
    printf("Enter any two number: ");
    scanf("%d%d", &a, &b);
    if(a>b)
        big=a;
    else
        big=b;
    printf("\nBiggest of the two number is: %d", big);
    getch();
    return 0;
}
```
## 14.Greater of three numbers:
```C
    #include <stdio.h>
    int main()
    {
        double n1, n2, n3;
        printf("Enter three different numbers: ");
        scanf("%lf %lf %lf", &n1, &n2, &n3);
        if( n1>=n2 && n1>=n3 )
            printf("%.2f is the largest number.", n1);
        if( n2>=n1 && n2>=n3 )
            printf("%.2f is the largest number.", n2);
        if( n3>=n1 && n3>=n2 )
            printf("%.2f is the largest number.", n3);
        return 0;
    }
    ```
## 15. GCD of two numbers:
```C
#include <stdio.h>
    int main()
    {
        int n1, n2, i, gcd;
        printf("Enter two integers: ");
        scanf("%d %d", &n1, &n2);
        for(i=1; i <= n1 && i <= n2; ++i)
        {
            // Checks if i is factor of both integers
            if(n1%i==0 && n2%i==0)
                gcd = i;
        }
        printf("G.C.D of %d and %d is %d", n1, n2, gcd);
        return 0;
    }
    ```
 ## 16.Leap Year
 ```C
      #include <stdio.h>
     
    int main()
    {
      int year;
     
      printf("Enter a year to check if it is a leap year\n");
      scanf("%d", &year);
     
      if (year%400 == 0) // Exactly divisible by 400 e.g. 1600, 2000
        printf("%d is a leap year.\n", year);
      else if (year%100 == 0) // Exactly divisible by 100 and not by 400 e.g. 1900, 2100
        printf("%d isn't a leap year.\n", year);
      else if (year%4 == 0) // Exactly divisible by 4 and neither by 100 nor 400 e.g. 2020
        printf("%d is a leap year.\n", year);
      else // Not divisible by 4 or 100 or 400 e.g. 2017, 2018, 2019
        printf("%d isn't a leap year.\n", year);  
       
      return 0;
    }
    ```
## 17. Linear Search:
```C
      #include <stdio.h>
     
    int main()
    {
      int array[100], search, c, n;
     
      printf("Enter number of elements in array\n");
      scanf("%d", &n);
     
      printf("Enter %d integer(s)\n", n);
     
      for (c = 0; c < n; c++)
        scanf("%d", &array[c]);
     
      printf("Enter a number to search\n");
      scanf("%d", &search);
     
      for (c = 0; c < n; c++)
      {
        if (array[c] == search)    /* If required element is found */
        {
          printf("%d is present at location %d.\n", search, c+1);
          break;
        }
      }
      if (c == n)
        printf("%d isn't present in the array.\n", search);
     
      return 0;
    }
    ```
## 18. Matrix Addition:
```C
    #include <stdio.h>
     
    int main()
    {
       int m, n, c, d, first[10][10], second[10][10], sum[10][10];
     
       printf("Enter the number of rows and columns of matrix\n");
       scanf("%d%d", &m, &n);
       printf("Enter the elements of first matrix\n");
     
       for (c = 0; c < m; c++)
          for (d = 0; d < n; d++)
             scanf("%d", &first[c][d]);
     
       printf("Enter the elements of second matrix\n");
     
       for (c = 0; c < m; c++)
          for (d = 0 ; d < n; d++)
             scanf("%d", &second[c][d]);
       
       printf("Sum of entered matrices:-\n");
       
       for (c = 0; c < m; c++) {
          for (d = 0 ; d < n; d++) {
             sum[c][d] = first[c][d] + second[c][d];
             printf("%d\t", sum[c][d]);
          }
          printf("\n");
       }
     
       return 0;
    }
    ```
## 19.Transpose of a Matrix:
```C
    #include <stdio.h>
    int main()
    {
        int a[10][10], transpose[10][10], r, c, i, j;
        printf("Enter rows and columns of matrix: ");
        scanf("%d %d", &r, &c);
        // Storing elements of the matrix
        printf("\nEnter elements of matrix:\n");
        for(i=0; i<r; ++i)
            for(j=0; j<c; ++j)
            {
                printf("Enter element a%d%d: ",i+1, j+1);
                scanf("%d", &a[i][j]);
            }
        // Displaying the matrix a[][] */
        printf("\nEntered Matrix: \n");
        for(i=0; i<r; ++i)
            for(j=0; j<c; ++j)
            {
                printf("%d  ", a[i][j]);
                if (j == c-1)
                    printf("\n\n");
            }
        // Finding the transpose of matrix a
        for(i=0; i<r; ++i)
            for(j=0; j<c; ++j)
            {
                transpose[j][i] = a[i][j];
            }
        // Displaying the transpose of matrix a
        printf("\nTranspose of Matrix:\n");
        for(i=0; i<c; ++i)
            for(j=0; j<r; ++j)
            {
                printf("%d  ",transpose[i][j]);
                if(j==r-1)
                    printf("\n\n");
            }
        return 0;
    }
    ```
## 20.Sum of Digit of Number:
```C
    #include <stdio.h>
     
    int main()
    {
       int n, t, sum = 0, remainder;
     
       printf("Enter an integer\n");
       scanf("%d", &n);
     
       t = n;
     
       while (t != 0)
       {
          remainder = t % 10;
          sum       = sum + remainder;
          t         = t / 10;
       }
     
       printf("Sum of digits of %d = %d\n", n, sum);
     
       return 0;
    }
    ```
## 21.Pallindrome Numbers:
```C
    #include <stdio.h>
    int main()
    {
        int n, reversedInteger = 0, remainder, originalInteger;
        printf("Enter an integer: ");
        scanf("%d", &n);
        originalInteger = n;
        // reversed integer is stored in variable 
        while( n!=0 )
        {
            remainder = n%10;
            reversedInteger = reversedInteger*10 + remainder;
            n /= 10;
        }
        // palindrome if orignalInteger and reversedInteger are equal
        if (originalInteger == reversedInteger)
            printf("%d is a palindrome.", originalInteger);
        else
            printf("%d is not a palindrome.", originalInteger);
        
        return 0;
    }
    ```
 ## 22.Swapping Call by value:
 ```C
 #include <stdio.h>
 
void swap(int, int);
 
int main()
{
   int x, y;
 
   printf("Enter the value of x and y\n");
   scanf("%d%d",&x,&y);
 
   printf("Before Swapping\nx = %d\ny = %d\n", x, y);
 
   swap(x, y); 
 
   printf("After Swapping\nx = %d\ny = %d\n", x, y);
 
   return 0;
}
 
void swap(int a, int b)
{
   int temp;
 
   temp = b;
   b = a;
   a = temp;
    printf("Values of a and b is %d  %d\n",a,b);
}
```
 
## 23.Swapping call By refernce:
```C
    #include <stdio.h>
     
    void swap(int*, int*);
     
    int main()
    {
       int x, y;
     
       printf("Enter the value of x and y\n");
       scanf("%d%d",&x,&y);
     
       printf("Before Swapping\nx = %d\ny = %d\n", x, y);
     
       swap(&x, &y); 
     
       printf("After Swapping\nx = %d\ny = %d\n", x, y);
     
       return 0;
    }
     
    void swap(int *a, int *b)
    {
       int temp;
     
       temp = *b;
       *b = *a;
       *a = temp;   
    }
    ```
## 24.Details of Emloyee using Structures
```C

#include <stdio.h>
 
/*structure declaration*/
struct employee{
    char    name[30];
    int     empId;
    float   salary;
};
 
int main()
{
    /*declare structure variable*/
    struct employee emp;
     
    /*read employee details*/
    printf("\nEnter details :\n");
    printf("Name ?:");          gets(emp.name);
    printf("ID ?:");            scanf("%d",&emp.empId);
    printf("Salary ?:");        scanf("%f",&emp.salary);
     
    /*print employee details*/
    printf("\nEntered detail is:");
    printf("Name: %s"   ,emp.name);
    printf("Id: %d"     ,emp.empId);
    printf("Salary: %f\n",emp.salary);
    return 0;
}```
## 25.Fraction of numbers Using Structure:
```C
#include<stdio.h>
#include<conio.h>
typedef struct
     {
        int num;
        int deno;
     
      }Fract;
 
   Fract sum(Fract,Fract);
 
   int main()
    {
     int num1,deno1,num2,deno2;
     printf("Enter fraction 1: numerator denominator:");
     scanf("%d%d",&num1,&deno1);
     printf("Enter fraction 2:numerator denominator:");
     scanf("%d%d",&num2,&deno2);
    
     Fract f1={num1, deno1}; // fraction 1
     Fract f2 ={num2, deno2};//fraction 2
     Fract result = sum(f1, f2);//sum the fractions
     printf("Result=%d/%d",result.num,result.deno);  //display the result
 
     getch();
     return 0;
    }
   Fract sum(Fract f1, Fract f2)
    {
     Fract result={(f1.num * f2.deno) + (f2.num * f1.deno), f1.deno * f2.deno};
     return result;
   }
  ```
