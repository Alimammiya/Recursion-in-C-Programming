In this tutorial, we will study  [what is recursion in c](https://usemynotes.com/what-is-recursion-in-c/)  programming, the structure of the recursion function, the advantages and disadvantages of recursion in c, the types of recursion, and the factorial of a number using recursion.

## Recursion in C Programming
Recursion is a process in which the function calls itself. Recursion is used to solve a problem by dividing it into small parts. Such functions which call themselves are called recursive functions.

## Structure of Recursive Function
```
return type myFunction(Parameters-list)
{
  statement 1;
  statement 2; 
  …
  statement N;
  myFunction(Arguments-list);
  …
  other statements;
}
```

## Advantages and Disadvantages of Recursion in c

### Advantages
- If we solve a problem through Recursion, then there is no need to call the function again and again. If we call the function 1 time, it keeps calling itself till the end result comes.
- The same problem is easily solved in recursion.

### Disadvantages
- Recursive programs are slower than normal programs.
- Requires consuming extra memory.

## Types of Recursion in C
### Direct Recursion
Direct recursion is a recursion in which a function calls itself.

```
return_type MyFunction(parameter-list)
{
  statements;
  MyFunction(argument-list);
  other statements;
}
```

### Indirect Recursion
In this, one function calls another function which in return calls it itself.

**First Function**
```
return_type FunctionOne(parameter-list)
{
statements;
FunctionTwo(argument-list);
other statements;
}
```
**Second Function**
```
return_type FunctionTwo(parameter-list)
{
statements;
FunctionOne(argument-list);
other statements;
}
```
## Factorial of a Number Using Recursion
```
#include <stdio.h>
#include <conio.h>
long int fact(int n);
int main()
{
  int n;
  printf("Enter a positive integer: ");
  scanf("%d", &n);
  printf("Factorial of %d = %ld", n, fact(n));
  return 0;
}
long int fact(int n)
{
  if (n >= 1)
  return n*fact(n-1);
  else
  return 1;
}
```
**Output**

```
Enter a positive integer: 4
Factorial of 4 = 24
```
Originally posted on [alimammiya.hashnode.dev](https://alimammiya.hashnode.dev/recursion-in-c-programming)
