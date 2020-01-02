## Loops in python

1.While Loop: In python, while loop is used to execute a block of statements repeatedly until a given a condition is satisfied. And when the condition becomes false, the line immediately after the loop in program is executed.

2.For Loop: For loops are used for sequential traversal. For example: traversing a list or string or array etc. In Python, there is no C style for loop, i.e., for (i=0; i<n; i++). There is “for in” loop which is similar to for each loop in other languages.

3.Iterating by index of sequences: We can also use the index of elements in the sequence to iterate. The key idea is to first calculate the length of the list and in iterate over the sequence within the range of this length.

4.Using else statement with for loops: We can also combine else statement with for loop like in while loop. But as there is no condition in for loop based on which the execution will terminate so the else block will be executed immediately after for block finishes execution.

5.Nested Loops: Python programming language allows to use one loop inside another loop.

for iterator_var in sequence: for iterator_var in sequence: statements(s) statements(s)

## Loop Control Statements: 

Loop control statements change execution from its normal sequence. When execution leaves a scope, all automatic objects that were created in that scope are destroyed. Python supports the following control statements.

- Continue Statement: It returns the control to the beginning of the loop.

- Break Statement: It brings control out of the loop

- Pass Statement: We use pass statement to write empty loops. Pass is also used for empty control statement, function and classes.

![L1](L1.PNG)
![L1O](L1O.PNG)

![L2](L2.PNG)
![L2O](L2O.PNG)

## Break and Continue in Python

- Break():
The break statement in Python terminates the current loop and resumes execution at the next statement, just like the traditional break found in C.

The most common use for break is when some external condition is triggered requiring a hasty exit from a loop. The break statement can be used in both while and for loops.
![Continue](Continue.PNG)

- Continue():
The continue statement in Python returns the control to the beginning of the while loop. The continue statement rejects all the remaining statements in the current iteration of the loop and moves the control back to the top of the loop.

The continue statement can be used in both while and for loops.
![Break](Break.PNG)

## Conditions

Python supports to have an else statement associated with a loop statements.

- If the else statement is used with a for loop, the else statement is executed when the loop has exhausted iterating the list.

- If the else statement is used with a while loop, the else statement is executed when the condition becomes false.

![If](If.PNG)

- ELIF
>a = 10

>b = 32

>if b > a:

>  print("b is greater than a")

>elif a == b:

>  print("a and b are equal")


- ELIF with else
>a = 10

>b = 32

>if b > a:

>  print("b is greater than a")

>elif a == b:

>  print("a and b are equal")

>else:

>  print("a is greater than b")

- Modules in python:

What is a Module?
Consider a module to be the same as a code library.

A file containing a set of functions you want to include in your application.


![Mod](Mod.PNG)
![InMod](InMod.PNG)
!![InModO](InModO.PNG)

- Variables in module:

![Var](Var.PNG)
![VarO](VarO.PNG)



- The from...import Statement
  
  Python's from statement lets you import specific attributes from a module into the current namespace.

> from modname import name1[, name2[, ... nameN]]

For example, to import the function fibonacci from the module fib, use the following statement

> from fib import fibonacci

- The from...import * Statement
   
   It is also possible to import all names from a module into the current namespace by using the following import statement.
   
> from modname import *


> The module search path is stored in the system module sys as the sys.path variable. The sys.path variable contains the current directory, PYTHONPATH, and the installation-dependent default.

- The dir() function
The dir() built-in function returns a sorted list of strings containing the names defined by a module. The list contains the names of all the modules, variables and functions that are defined in a module.

> import platform

> x = dir(platform)

> print(x)

## Function and Function calls

In the most general sense, a function is a structuring element in programming languages to group a set of statements so they can be utilized more than once in a program. The only way to accomplish this without functions would be to reuse code by copying it and adapt it to its different context. Using functions usually enhances the comprehensibility and quality of the program. It also lowers the cost for development and maintenance of the software.

Functions are known under various names in programming languages, e.g. as subroutines, routines, procedures, methods, or subprograms.

> def function-name(Parameter list):
>    statements, i.e. the function body

Function bodies can contain one or more return statement. They can be situated anywhere in the function body. A return statement ends the execution of the function call and "returns" the result, i.e. the value of the expression following the return keyword, to the caller. If the return statement is without an expression, the special value None is returned. If there is no return statement in the function code, the function ends, when the control flow reaches the end of the function body and the value "None" will be returned.

![Func](Func.PNG)
![FuncO](FuncO.PNG)

- Return Values

![RV](RV.PNG)  
![RV2](RV2.PNG) 
![RV3](RV3.PNG) 


- Returning Multiple Values

![RMV](RMV.PNG) 

- Local and Global Values

![local](Local.PNG) 
