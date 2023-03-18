## TYPE CONVERSION

Type conversion, also known as `type casting`, is the process of converting one data type into another data type in C. Type conversion is often necessary when working with variables of different data types or when passing values between functions that expect different data types.

There are two types of type conversions in C:

1. Implicit Type Conversion: Implicit type conversion is performed automatically by the compiler when two variables of different data types are used in an expression. The data type with the lower precision is automatically promoted to the data type with the higher precision. For example, when adding an integer and a float, the integer is implicitly converted to a float before the addition is performed.

2. Explicit Type Conversion: Explicit type conversion is performed by the programmer using a type cast operator. The type cast operator is denoted by placing the desired data type in parentheses before the value to be converted. For example, to convert an integer to a float, the integer variable can be explicitly cast as a float using the following syntax:

```CPP
int num = 5;
float fnum = (float) num;

//In similar way Numeric data can be converted into inter-Numeric datatypes 
double d = (double) num;
int i = (int) d

```

It's important to note that explicit type conversion can result in loss of data or precision. For example, converting a float to an integer will truncate the decimal portion of the float, potentially resulting in a loss of precision. As such, explicit type conversion should be used with caution and only when necessary.


## PRECEDENCE AND ORDER OF EVALUATION

Precedence and order of evaluation are important concepts in C that determine how expressions are evaluated by the compiler.

`Precedence` refers to the order in which operators are evaluated in an expression. Operators with higher precedence are evaluated before operators with lower precedence. For example, in the expression 2 + 3 * 4, the multiplication operator has a higher precedence than the addition operator, so the multiplication is performed first and the result is added to 2.

The following table shows the operator precedence in C, from highest to lowest:

```CPP
Operator	                                       Description
()	                                           =>   Parentheses
[]	                                           =>   Array subscripting
->	                                           =>   Member selection via pointer
++, --	                                           =>   Postfix increment/decrement
++, --	                                           =>   Prefix increment/decrement
+, -	                                           =>   Unary plus/minus
!, ~	                                           =>   Logical NOT, bitwise complement
*, /, %	                                           =>   Multiplication, division, modulus
+, -	                                           =>   Addition, subtraction
<<, >>	                                           =>   Bitwise shift left/right
<, <=, >, >=	                                   =>   Relational operators
==, !=	                                           =>   Equality operators
&	                                           =>   Bitwise AND
^	                                           =>   Bitwise XOR
|	                                           =>   Bitwise OR
&&	                                           =>   Logical AND
||	                                           =>   Logical OR
?:	                                           =>   Ternary conditional
=, +=, -=, *=, /=, %=, <<=, >>=, &=, ^=, |=	   =>   Assignment operators
```
`Order of evaluation` refers to the order in which operands in an expression are evaluated. In C, the order of evaluation is `left-to-right`, with the `exception` of some operators, such as the `logical AND (&&) and logical OR (||) operators`, which use short-circuit evaluation. Short-circuit evaluation means that if the left-hand side of the operator is enough to determine the result, the right-hand side will not be evaluated at all. 

For example, in the expression (x != 0) && (y/x > 3), if x is equal to zero, the right-hand side of the operator will not be evaluated, as the result of the entire expression will be false.

It's important to understand operator precedence and order of evaluation in order to write correct and efficient C code. Parentheses can be used to override the default order of evaluation, and it's always a good practice to use them to make expressions more readable and to avoid potential bugs.


