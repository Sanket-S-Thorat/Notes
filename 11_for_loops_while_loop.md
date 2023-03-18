## for loop

Consider the following code;

```CPP
#include <stdio.h>

int main(){
    printf("1\n");
    printf("2\n");
    printf("3\n");
    printf("4\n");
    printf("5\n");
    printf("6\n");
    printf("7\n");
    printf("8\n");
    printf("9\n");
    printf("10\n");

    return 0;
}
```
So, above code would print all numbers from 1 - 10 each on new line.

Note that the \n in each print statement moves the cursor to the next line of the console. It is called as new line character, such character are preceded by "\" character.
It is also called as escape character. to hit a tab we use \t inside the string literal.

Coming back to code.

It is visible that we are doing repetitive task of printing statements.

What if you could create a variable with value 1 which can go from value 1 to 10.
Such case can be handled using for loops.

When to use? => When we want to run a set of statements multiple times.

`Syntax : for( iterable_value; condition; increment/decrement){}`

We can write above example as;

```CPP
#include <stdio.h>

int main(){
    int a = 1;

    for( a = 1; a < 11; a++){
        printf("%d\n", a);
    }
    return 0;
}
```
So, our code got so small.

The line that prints to console get executed for values of "a" from 1-10. The above code can also be written by directly declaring the variable "a" in the for statement itself.

```CPP
#include <stdio.h>

int main(){

    for( int a = 1; a < 11; a++){
        printf("%d\n", a);
    }
    return 0;
}
```

Now to give a try for yourself. Try printing from 10 to 0.

<detail>
    <summary>
        Hint
    </summary>
    Use the decrement operator instead of a++
</detail>

You also nest the for loops in the same way as the if statement. Lets try a bit hard problem.

Lets try to print the sample space for rolling two fair dices.

<img src="./img/dice.png">

```CPP
#include <stdio.h>
int main(){

    for( int a = 1; a < 7; a++){        //line 1
        for( int b = 1; b < 7; b++){    //line 2
            printf("(%d,%d)", a, b);    //line 3
        }
        printf("\n");                  // line 4
    }
    return 0;
}
```

Lets go through the code flow

Line no | value of a | value of b
   1    |     1      |     0
   2    |     1      |     1   => print
   2    |     1      |     2   => print
   2    |     1      |     3   => print
   2    |     1      |     4   => print
   2    |     1      |     5   => print
   2    |     1      |     6   => print
   4    |     1      |     0   => new line [b turns back to zero coz variable b was created under local scope of 2nd for loop]
   1    |     2      |     0
   2    |     2      |     1   => print
   2    |     2      |     2   => print
   2    |     2      |     3   => print
   2    |     2      |     4   => print
   2    |     2      |     5   => print
   2    |     2      |     6   => print
   4    |     2      |     0   => new line

Same execution flow goes for all values of "a" = 3, 4, 5, 6.

In short the for every value of "a" from 1-6 the second for loop runs 6 times i.e. with value of b from 1-6 and;

whenever the second for loop runs 6 times consecutively it executes the new line print command.

## WHILE LOOP:

Similar loop but the increment/decrement/change of the iterator is done inside the loop itself.

Say for an example I want to print all even numbers till 20:

with for loop it can be done as;

```CPP
#include <stdio.h>
int main(){

    for( int a = 0; a <= 20; a++){ // made it <=20 coz we want our a to iterate from 0-20
        if(a%2 == 0){ //
            printf("(%d)", a);   
        }              
    }
    return 0;
}
```
Other way to write the same would be;
```CPP
#include <stdio.h>
int main(){

    for( int a = 0; a <= 20; a = a + 2){ // Here a is incremented by 2 so, a will iterate as 0,2,4,6,8,10,...20
            printf("(%d)", a);               
    }
    return 0;
}
```
Now just to look at `syntax` of `while loop`

```CPP
while (condition){
    do something...

    increment/decrement/value change;
}
```

So the above code using while loop can be written as;

```CPP
#include <stdio.h>
int main(){
    int a = 0;
    while( a <= 20){ // Here a is incremented by 2 so, a will iterate as 0,2,4,6,8,10,...20
            printf("(%d)", a);
            a += 2;  // This is a shorthand to a= a+2, in same way you can write for all arithmetic operators like a-=2 ==> a = a -2, a*=3 ==> a = a*3, etc               
    }
    return 0;
}
```

