### Variables

Variable are name to the storage location for the data in the computer's memory where a value can be stored and later accessed by its name.

For example,

```
int a = 4;

Ressembles that the data stored in the program memory is referenced/tagged by name "a"

                   - - - - - - - memory address = 1000
                    |          |
                   - - - - - - - memory address = 1004 [added by 4 as integer size = 4]
int a ----------->  |    4     |
                   - - - - - - -
```

To create a variable in C, you must first specify its data type (e.g., int, float, char, etc.) and then give it a name. The name must follow the rules of C identifiers, such as beginning with a letter or underscore and consisting of letters, digits, and underscores.

Here is an example of creating a variable in C:
```CPP
int myVariable; // declaring a variable of type int with the name "myVariable"
```
This creates a variable of type int called myVariable in the computer's memory. The value of myVariable is initially undefined, meaning it may contain any value that happens to be in that memory location at the time of its creation.

To assign a value to a variable, you can use the assignment operator =. For example:
```
myVariable = 42; // assigning the value 42 to myVariable
```
This sets the value of myVariable to 42.

You can also initialize a variable with a value at the time of its creation by using the assignment operator after the variable's declaration. For example:
```
int myVariable = 42; // declaring and initializing myVariable with the value 42
```
Once a variable has been created and assigned a value, you can use it in expressions, such as arithmetic or comparison operations, and in function calls.


It's important to note that variables in C are `strongly typed`, meaning that once a variable has been declared with a certain data type, it can only hold values of that type. Attempting to assign a value of a different type to a variable will result in a type error.

## NAMING CONVENTIONS [RULES]

In C, the rules for naming variables are as follows:

1. Variable names must `start with a letter (a to z or A to Z), or an underscore (_)`.
2. After the first character, variable names may `also contain digits` (0 to 9).
3. Variable names are `case-sensitive`. This means that myVar, myvar, and MYVAR are all different names.
4. Variable names must `not be the same as keywords` reserved by the C language (e.g. int, for, while, etc.).
5. Variable names should be descriptive and meaningful, and should `not exceed 31 characters`.
Here are some examples of valid variable names in C:

```CPP
int age;
float temperature;
char my_char;
double my_double;
int _my_variable;
```
And here are some examples of invalid variable names:

```CPP
int 123var; // variable name cannot start with a digit
float my_variable+2; // variable name cannot contain special characters
int int; // variable name cannot be a reserved keyword
long variable_with_a_name_that_is_way_too_long; // variable name is too long
```

## CONSTANTS

In C, a constant is a value that cannot be modified by the program once it has been defined. Constants can be of various types, including integer, floating-point, and character types. Constants are useful for defining values that should not be changed during the program's execution and can help make code more readable and maintainable.

There are two types of constants in C:

1. `Literal constants`: Literal constants are fixed values that are directly specified in the program's source code. For example:

    1. Integer constant: 42
    2. Floating-point constant: 3.14
    3. Character constant: 'A'

2. `Symbolic constants`: Symbolic constants are named values that represent a fixed value in the program. They are defined using the #define preprocessor directive and are typically written in uppercase letters to distinguish them from variables. For example:

```CPP
#include <stdio.h>
int main(void)
{
#define PI 3.14
#define MAX_LENGTH 100

int radius = 4;
float area_of_circle = PI*radius*radius;

printf("Area of the circle = %.2f", area_of_circle); // Outputs --> Area of the circle = 50.24 (upto 2 decimals because its .2f)
 return 0;
}
```



Constants in C can be used in various ways, such as assigning them to variables, using them in expressions, passing them as function arguments, and more. By convention, symbolic constants are preferred over literal constants because they make the code more readable and maintainable by providing descriptive names for values used throughout the program.


## STATEMENTS

It is a syntactic unit that expresses an action to be carried out by the program. Statements are the building blocks of a program (relate it to a organ system in human body) and are executed one at a time in the order in which they appear. 
A statement can be a simple assignment or a more complex expression, and it can also include control flow statements, such as loops and conditional statements.

Here are some examples of statements in C:

```CPP
x = 5; // Assignment statement
y = x + 3; // Assignment statement with expression
if (x > 0) { // Conditional statement
   printf("x is positive\n");
}
while (y > 0) { // Loop statement
   y--;
   printf("y is now %d\n", y);
}
```

In C, each statement is terminated with a semicolon (;), which tells the compiler that the statement has ended and the next statement can be processed.

Note that C does not have a separate statement for declaring variables. Variable declarations are not considered statements, but rather declarations that provide information about the variables to the compiler. 

Declarations must appear before any statements that use the variables, and they can be grouped together at the beginning of a function or block.


## BLOCK

In C, a block is a group of zero or more statements enclosed in braces ({ }). Blocks are used to group statements together and to limit the scope of variables and functions.

Here is an example of a block:

```CPP
{
    int x = 5;
    printf("x is %d\n", x);
}
```
In this example, the block contains two statements: a variable declaration and a printf() statement. The variable x is declared inside the block, and it is only accessible from within the block. Once the block is exited, the variable is no longer in scope and cannot be accessed.

Blocks are commonly used in C to limit the scope of variables and functions. For example, a block can be used to define a local variable inside a function that is only needed for a specific section of code:

```CPP
void myFunction() {
    // some code here...
    {
        int x = 5; // x is only needed for this section of code
        // some more code here...
    }
    // the variable x is not in scope here
}```
In addition to limiting variable scope, blocks can also be used to group related statements together and to make code more readable and maintainable.