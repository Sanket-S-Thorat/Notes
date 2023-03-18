## HELLO WORLD

As the tradition goes lets look at a the code using C that can print "Hello World" to the console (For now make a understanding console is somewhere you get your output)

###`Important: Do not try to find as what this code does nor how it behaves for now just read it and look how the formatting is done.`

```CPP
#include <stdio.h>      //Line 1
int main(void)          //Line 2
{                       //Line 3
 printf("Hello, World");  //Line 4
 return 0;              //Line 5
}                       //Line 6
```


You can play with above code over <a href="http://coliru.stacked-crooked.com/a/263e35298419ef1d">here</a>

###`Line 1:`
This line tells the compiler(for now consider this as the software that will be running your code) to include the contents of the standard library header file stdio.h in the program.

In Layman terms : Take example, when you are going on a trip somewhere out of the country you would be needing some essential to do so. Say you need passport to onboard the plane. In similar way the compiler needs to understand what the following code is trying to tell him. 


-- Following just keep in mind. Dont try to overdo on the terminologies like macros, functions, etc.
Headers are usually files containing function declarations, macros and data types, and you must include the header file before you use them. This line includes stdio.h so it can call the function puts().

###`Line 2:`
This line starts the definition of a function (Function is a set of statements that does a specific work as whole). It states the name of the function (main), the type and number of arguments it expects (void, meaning none), and the type of value that this function returns (int). Program execution starts in the main() function

Important : Keep in mind that, irrespective of the placement of the functions a compiler would by default initiate the execution of the code by main() function. And every C program will have a void main() function.

###`Line 3 to Line 6:`
The curly braces are used in pairs to indicate where a block of code begins and ends. They can be used in a lot of ways, but in this case they indicate where the function begins and ends.
(Remember I mentioned something about set of statements, this curly braces ({}) would contain those.)

###`Line 4: Function CALL`
This line calls the puts() function to output text to standard output (the screen, by default), followed by a newline. The string (sentence enclosed in "") to be output is included within the parentheses. (here, Hello World)

Make note puts() function is function stored under the header (here, stdio.h)

"Hello, World" is the string that will be written to the screen. In C, every string literal value must be inside the double quotes "…"


Some miscellaneous information;

###`Line 5`
In C programs, every statement needs to be terminated by a semi-colon (i.e. ";").
```CPP
return 0;
```
When we defined main(), we declared it as a function returning an int [int main(){}--syntax--> returnType functionName(){}], meaning it needs to return an integer. In this example, we are returning the integer value 0, which is used to indicate that the program exited successfully.
After the return 0; statement, the execution process will terminate (end).

Above code can also be written as;

```CPP
#include <stdio.h>
main()
{
 puts("hello, world\n");

 return 0;
}
```

Try to play with the link provided above.
