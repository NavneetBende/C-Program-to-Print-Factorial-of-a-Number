# C-Program-to-Print-Factorial-of-a-Number

Write a C program to find the Factorial of a number
Factorial is a sequence of a number where we multiply by all previous numbers. 

factorial of n (n!) = 1 * 2 * 3 * 4....n


Note : 0! = 1 and 1! = 1

Example : 
5! = 1 * 2 * 3 * 4 * 5 = 120
factorial of number in c
Methods we will discuss
Iterative approach for factorial
Recursive approach for factorial
Method 1
For an input num

Initialize fact = 1
If num < 0 : Print Error as we can’t calculate factorial of a negative number
Else run a iterative loop in iteration of (i) between [1, num]
do fact = fact * i
print the value of fact
C program:-
Run
#include<stdio.h>
int main ()
{
    int num = 5, fact = 1;
    
    // Can't calculate factorial of a negative number
    if(num < 0)
        printf("Error");
    else
    {
        for(int i = 1; i <= num; i++)
            fact = fact * i;
    }
    
    printf("Fact %d: %d",num, fact);
}
// Time complexity: O(N)
// Space complexity: O(1)
Output:-
Fact 5: 120
Related Pages
Fibonacci Series upto nth term

Find the Nth Term of the Fibonacci Series

Factorial of a number

Power of a number

Factor of a number

Strong number

Method 2
This method uses the recursive approach, for input num

For an input num

Call function getFactorial(num)
Set base case when num== 0 return 1
Other cases return num * getFactorial(num-1);
C Program
Run
#include<stdio.h>
int getFactorial(int num)
{
    if(num == 0)
        return 1;
        
    return num * getFactorial(num-1);
}
int main ()
{
    int num = 7;
    
    int fact = getFactorial(num);
    
    printf("Fact %d: %d",num, fact);
}
// Time complexity: O(N)
// Space complexity: O(1)
// Auxiliary Space complexity (Function call stack): O(N)
Output
Fact 7: 5040
