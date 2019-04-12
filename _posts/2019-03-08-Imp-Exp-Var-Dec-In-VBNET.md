---
layout: post
title: Variable Declaration in VB.NET!!
author: Ashish
categories: [ Tutorials ]
image: assets/images/4.jpg
---
# How To Declare Variable in VB.NET

Most of the programming languages force the programmer to declare all the variables before they can be referenced in the program otherwise it will generate a compile time error.
However VB.NET does not forces the programmer to declare variables. It means there is no need to declare the variables before using it in the program.
Variables can be declared in visual basic using two methods.
(1) Implicit Declaration
(2) Explicit Declaration
By default VB.NET supports explicit variable declaration. However if you wish you can change default behavior by following steps given below:
**Steps**
Step 1: Select Properties option from Project Menu. 
Step 2: Select Compile Option.
Step 3: Select OFF in the Option Explicit Combo Box. 

You can also write Option Explicit OFF at starting of code window to turn OFF explicit variable declaration. 
Implicit Variable Declaration

In VB.NET it is not compulsory to declare all the variables in advance before it can be referenced in the program.
You can use the variable directly when it is required. When the compiler finds a variable that is not declared, it will automatically create a new variable of type object. This type of technique is known as implicit declaration of variable. 
The data type of variables declared using implicit declaration is object by default. You can store any type of value in this type of variable, the compiler will automatically determines the type of the variable depending upon the type of the value that is stored in the variable. 
Disadvantage of Implicit Declaration:
(1) It will decrease the speed and efficiency of the program because the compiler does not know in advance which variables are being used in the program and what are the data types of those variables. The compiler has to allocate memory to every variable when it finds a new variable. 
(2) Typing errors can not be caught using this type of technique because if you make a typing mistake while writing the name of the variable instead of generating a compile time error the compiler will create a new variable. 
(3) By default the data type of the variables declared using this technique is object which occupies more memory as compared to specific data type.
Explicit Variable Declaration

By default in VB.NET it is compulsory to declare all the variables in advance before it can be referenced in the program.
You can also declare the variable explicitly before it is referenced in the program. This type of technique is known as explicit declaration of variable. 
Advantage of Explicit Declaration:
(1) It will increase the speed and efficiency of the program because the compiler know in advance which variables are being used in the program and what are the data types of those variables.
(2) Typing errors can be easily caught using this type of technique because if you make a typing mistake while writing the name of the variable the compiler will generate a compile time error indicating "variable is not defined".
(3) Type Mismatch error can be easily caught using this technique. For example if you declared a variable of type integer and assign a string value to that variable will generate run time error indicating "Type Mismatch".
(4) You can declare typed variable using this technique so the memory is allocated depending upon the type of the variable. Thus there is no wastage of memory space while declaring variables explicitly.
How To Declare Variable Explicitly?

Variables can be declared explicitly using the Dim statement.
The general syntax for declaring the variable is given below:
Syntax:
Dim variable-name as DataType
Example:
Dim Name as String 
When you declare the variable the compiler allocates space for that variable depending upon the Type of the variable and assigns one name for that reserved memory space. So later in the program you can refer to that memory space using the name of the variable.
We can also declare more then one variables of the same type in the same line as shown below:
Dim a as integer, b as integer, c as integer
We can also declare more then one variable of different type in the same line as shown below:
Dim a as Integer, b as String, c as Double
