## LOGICAL OPERATORS

1. Logical AND
Performs a logical boolean AND-ing of the two operands returning 1 if both of the operands are non-zero. The logical AND operator is of type int.
```CPP
0 && 0 /* Returns 0. */
0 && 1 /* Returns 0. */
2 && 0 /* Returns 0. */
2 && 3 /* Returns 1. */
```

2. Logical OR
Performs a logical boolean OR-ing of the two operands returning 1 if any of the operands are non-zero. The logical
OR operator is of type int.
```CPP
0 || 0 /* Returns 0. */
0 || 1 /* Returns 1. */
2 || 0 /* Returns 1. */
2 || 3 /* Returns 1. */
```

3. Logical NOT
Performs a logical negation. The logical NOT operator is of type int. The NOT operator checks if at least one bit is
equal to 1, if so it returns 0. Else it returns 1;
```CPP
!1 /* Returns 0. */
!5 /* Returns 0. */
!0 /* Returns 1. */
```

## Relational Operators

1. Equals [ == ]
Checks whether the supplied operands are equal.
```CPP
1 == 0; /* evaluates to 0. */
1 == 1; /* evaluates to 1. */

int x = 5;
int y = 5;
int *xptr = &x, *yptr = &y;
xptr == yptr; /* evaluates to 0, the operands hold different location addresses. */
*xptr == *yptr; /* evaluates to 1, the operands point at locations that hold the same value. */
```

#### Attention: This operator should not be confused with the assignment operator (=)!

2. Not equals "!="
Checks whether the supplied operands are not equal.

```CPP
1 != 0; /* evaluates to 1. */
1 != 1; /* evaluates to 0. */
int x = 5;
int y = 5;
int *xptr = &x, *yptr = &y;
xptr != yptr; /* evaluates to 1, the operands hold different location addresses. */
*xptr != *yptr; /* evaluates to 0, the operands point at locations that hold the same value. */
```
This operator effectively returns the opposite result to that of the equals (==) operator.

3. Not "!"
Check whether an object is equal to 0.
```CPP
The ! can also be used directly with a variable as follows:
!someVal

This has the same effect 
assomeVal == 0
```
4. Greater than ">"
Checks whether the left hand operand has a greater value than the right hand operand
```CPP
5 > 4 /* evaluates to 1. */
4 > 5 /* evaluates to 0. */
4 > 4 /* evaluates to 0. */
```

5. Less than "<"
Checks whether the left hand operand has a smaller value than the right hand operand
```CPP
5 < 4 /* evaluates to 0. */
4 < 5 /* evaluates to 1. */
4 < 4 /* evaluates to 0. */
```

6. Greater than or equal ">="
Checks whether the left hand operand has a greater or equal value to the right operand.
```CPP
5 >= 4 /* evaluates to 1. */
4 >= 5 /* evaluates to 0. */
4 >= 4 /* evaluates to 1. */
```

7. Less than or equal "<="
Checks whether the left hand operand has a smaller or equal value to the right operand.
```CPP
5 <= 4 /* evaluates to 0. */
4 <= 5 /* evaluates to 1. */
4 <= 4 /* evaluates to 1. */
```

## CONDITIONAL OPERATORS

Evaluates its first operand, and, if the resulting value is not equal to zero, evaluates its second operand. Otherwise, it evaluates its third operand, as shown in the following example:
```CPP
a = b ? c : d;
```
is equivalent to:
```CPP
if (b)
 a = c;
else
 a = d;
```
This pseudo-code represents it : condition ? value_if_true : value_if_false. Each value can be the result of an evaluated expression.
```CPP
int x = 5;
int y = 42;
printf("%i, %i\n", 1 ? x : y, 0 ? x : y); /* Outputs "5, 42" */
```
The conditional operator can be nested. For example, the following code determines the bigger of three numbers:
```CPP
big= a > b ? (a > c ? a : c): (b > c ? b : c)
```
The conditional operator associates from right to left. Consider the following:
```CPP
exp1 ? exp2 : exp3 ? exp4 : exp5
```
As the association is from right to left, the above expression is evaluated as
```CPP
exp1 ? exp2 : ( exp3 ? exp4 : exp5 )
```

## BITWISE OPERATORS

Bitwise operators in a nutshell is equivalent to doing logical operations on every bit.

i.e. a = 4, b = 3 then;

bitwise operators do operations on 
binary(4) ==> 0000 0100  &
binary(3) ==> 0000 0011   

Note that binary() here is not a function. It is written such in order to understand.

```CPP
Symbol    Operator
&        bitwise AND
|        bitwise inclusive OR
^        bitwise exclusive OR (XOR)
~        bitwise not (one's complement)
<<       logical left shift
>>       logical right shift
```

Following program illustrates the use of all bitwise operators:

```CPP
include <stdio.h>
int main(void)
{
 unsigned int a = 29; /* 29 = 0001 1101 */ 
 unsigned int b = 48; /* 48 = 0011 0000 */
 int c = 0; 

 c = a & b; /* 32 = 0001 0000 */
 printf("%d & %d = %d\n", a, b, c );

 c = a | b; /* 61 = 0011 1101 */
 printf("%d | %d = %d\n", a, b, c );

 c = a ^ b; /* 45 = 0010 1101 */
 printf("%d ^ %d = %d\n", a, b, c );

 c = ~a; /* -30 = 1110 0010 */
 printf("~%d = %d\n", a, c );

 c = a << 2; /* 116 = 0111 0100 */  // shifts all bits to left and fills it with zero
 printf("%d << 2 = %d\n", a, c );

 c = a >> 2; /* 7 = 0000 0111 */ // shifts all bits to right and fills it with zero
 printf("%d >> 2 = %d\n", a, c ); 

 return 0;
}
```
## ARITHMETIC OPERATORS

1. Addition Operator
The addition operator (+) is used to add two operands together. Example:
```CPP
#include <stdio.h>
int main(void)
{
 int a = 5;
 int b = 7;
 int c = a + b; /* c now holds the value 12 */
 printf("%d + %d = %d",a,b,c); /* will output "5 + 7 = 12" */
 return 0;
}
```

2. Subtraction Operator
The subtraction operator (-) is used to subtract the second operand from the first. Example:
```CPP
#include <stdio.h>
int main(void)
{
 int a = 10;
 int b = 7;
 int c = a - b; /* c now holds the value 3 */
 printf("%d - %d = %d",a,b,c); /* will output "10 - 7 = 3" */
 return 0;
}
```

3. Multiplication Operator
The multiplication operator (*) is used to multiply both operands. Example:
```CPP
#include <stdio.h>
int main(void)
{ 
 int a = 5;
 int b = 7;
 int c = a * b; /* c now holds the value 35 */
 printf("%d * %d = %d",a,b,c); /* will output "5 * 7 = 35" */
 return 0;
}
```

4. Division Operator
The division operator (/) divides the first operand by the second. If both operands of the division are integers, it will return an integer value and discard the remainder (use the modulo operator % for calculating and acquiring the remainder). If one of the operands is a floating point value, the result is an approximation of the fraction.

Example:
```CPP
#include <stdio.h>
int main (void)
{
 int a = 19 / 2 ; /* a holds value 9 */
 int b = 18 / 2 ; /* b holds value 9 */
 int c = 255 / 2; /* c holds value 127 */
 int d = 44 / 4 ; /* d holds value 11 */
 double e = 19 / 2.0 ; /* e holds value 9.5 */
 double f = 18.0 / 2 ; /* f holds value 9.0 */
 double g = 255 / 2.0; /* g holds value 127.5 */
 double h = 45.0 / 4 ; /* h holds value 11.25 */
 printf("19 / 2 = %d\n", a); /* Will output "19 / 2 = 9" */
 printf("18 / 2 = %d\n", b); /* Will output "18 / 2 = 9" */
 printf("255 / 2 = %d\n", c); /* Will output "255 / 2 = 127" */
 printf("44 / 4 = %d\n", d); /* Will output "44 / 4 = 11" */
 printf("19 / 2.0 = %g\n", e); /* Will output "19 / 2.0 = 9.5" */
 printf("18.0 / 2 = %g\n", f); /* Will output "18.0 / 2 = 9" */
 printf("255 / 2.0 = %g\n", g); /* Will output "255 / 2.0 = 127.5" */
 printf("45.0 / 4 = %g\n", h); /* Will output "45.0 / 4 = 11.25" */
 return 0;
}
```

5. Modulo Operator
The modulo operator (%) receives integer operands only, and is used to calculate the remainder after the first operand is divided by the second. Example:
```CPP
#include <stdio.h>
int main (void) {
 int a = 25 % 2; /* a holds value 1 */
 int b = 24 % 2; /* b holds value 0 */
 int c = 155 % 5; /* c holds value 0 */
 int d = 49 % 25; /* d holds value 24 */
 printf("25 % 2 = %d\n", a); /* Will output "25 % 2 = 1" */
 printf("24 % 2 = %d\n", b); /* Will output "24 % 2 = 0" */
 printf("155 % 5 = %d\n", c); /* Will output "155 % 5 = 0" */
 printf("49 % 25 = %d\n", d); /* Will output "49 % 25 = 24" */
 return 0;
}
```

6. Increment / Decrement Operators
The increment (a++) and decrement (a--) operators are different in that they change the value of the variable you apply them to without an assignment operator. You can use increment and decrement operators either before or after the variable. The placement of the operator changes the timing of the incrementation/decrementation of the value to before or after assigning it to the variable. Example:

```CPP
#include <stdio.h>
int main(void)
{
 int a = 1;
 int b = 4;
 int c = 1;
 int d = 4;
 a++;
 printf("a = %d\n",a); /* Will output "a = 2" */
 b--;
 printf("b = %d\n",b); /* Will output "b = 3" */
 if (++c > 1) { /* c is incremented by 1 before being compared in the condition */
 printf("This will print\n"); /* This is printed */
 } else {
 printf("This will never print\n"); /* This is not printed */
 }
 if (d-- < 4) { /* d is decremented after being compared */
 printf("This will never print\n"); /* This is not printed */
 } else {
 printf("This will print\n"); /* This is printed */
 }
}
```

As the example for c and d shows, both operators have two forms, as prefix notation and postfix notation. Both have the same effect in incrementing (++) or decrementing (--) the variable, but differ by the value they return: prefix operations do the operation first and then return the value, whereas postfix operations first determine the value that is to be returned, and then do the operation.

## sizeof Operator
1. With a type as operand
Evaluates into the size in bytes, of type size_t, of objects of the given type. Requires parentheses around the type.
```CPP
printf("%zu\n", sizeof(int)); /* Valid, outputs the size of an int object, which is platform dependent. */
printf("%zu\n", sizeof int); /* Invalid, types as arguments need to be surrounded by parentheses! */
```
2. With an expression as operand
Evaluates into the size in bytes, of type size_t, of objects of the type of the given expression. The expression itself is not evaluated. Parentheses are not required; however, because the given expression must be unary, it's considered best practice to always use them.
```CPP
char ch = 'a';
printf("%zu\n", sizeof(ch)); /* Valid, will output the size of a char object, which is always 1 for all platforms. */
printf("%zu\n", sizeof ch); /* Valid, will output the size of a char object, which is always 1 forall platforms. */
```
