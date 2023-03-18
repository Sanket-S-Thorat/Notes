##Commenting
 Commenting is a way to write something in a code that you as a programmer dont want yor compiler to compile.

 Consider if you want to explain what the code does in the same file where you wrote your code but you don't want your compiler to read that we can do that as following.

 ```CPP
 int main(void)
{
//puts("Hi");                                          //Line 3
 printf("Hello, World");                               //Line 4
 
                                                       //line 6
/*                                                     //line 7
 puts("Again Hello, World");                           //line 8
 puts("last time, Hello, World");                      //line 9
*/                                                     //line 10
 printf("Bye!!!");                                     //line 11
/*This code prints Hello, World                        //line 12
only once to the console*/                             //line 13
return 0;                                              //line 14

printf("Doesnt runs as after return statement");       //line 16
```

#### Output
<img src="./img/output1.png">

So, commenting can be done in two ways:

1. By preceding "//" ==> This does a single line comment
    Notice that at line 3 there is a put statment with Hi but the console doesn't prints that. As the // ask the compiler to skip that line for compilation
    Also note that the line 4 is read by the compiler as we can see it in output so it is not commented. Hence, single line comment

2. By enclosing within "/* .... */ " ==> Multiline comment
    It visible that compiler doesn't compile the put function at line 8 and line 9 so compiler considered both line 8 and 9 as comments.

3. The very line after */ gets compiled hence we can see that  anything between /* */ is a comment

4. Line 12 and 13 is another example of multiline comment.
