#### Editing the program
Simple text editors include <a href="http://www.vim.org/"> vim</a> or <a href="">gedit</a> on Linux, or <a href="">Notepad</a> on Windows. Cross-platform editors also include
<a href="">Visual Studio Code</a> or <a href="">Sublime Text</a>. This are what we mean IDE i.e Integrated Development Environment.

Layman Terms : A software that where you can write, edit, modify and execute(run) your code

Note: The editor must create plain text files, not RTF or other any other format.

###`Compiling and running the program`

Consider the earlier example of "Hello World"

Open a notepad and paste that code into the file and save it as hello.c (here ".c" is the extension for the file so that the editor and the Operating System (windows, linux) can understand that it is a code in C language.)

To run the program, this source file (hello.c) first needs to be compiled into an executable file (e.g. hello on Unix/Linux system or hello.exe on Windows). This is done using a compiler for the C language.

So, in layman terms compiling can be considered as the process of converting a human-readable and understandable code into a form that a computer can understand.

FYI: Computer understands and works on machine language. A language consisting of "1" and "0" also referred as binary language so every character in the hello.c will be converted to zeroes and ones after compilation and the component that does this conversion is "COMPILER"

There are multiple compilers that can do this task. Following are some;

`Compile using GCC`

GCC (GNU Compiler Collection) is a widely used C compiler. To use it, open a terminal, use the command line to
navigate to the source file's location and then run:
```CPP
gcc hello.c -o hello
```
If no errors are found in the the source code (hello.c), the compiler will create a binary file, the name of which is given by the argument to the -o command line option (hello). This is the final executable file.

--- Extra info. Not mandatory to study---

We can also use the warning options -Wall -Wextra -Werror, that help to identify problems that can cause the program to fail or produce unexpected results. They are not necessary for this simple program but this is way of adding them:
```
gcc -Wall -Wextra -Werror -o hello hello.c
```

###One liner : COMPILER ==> checks code for errors + converts & saves the .c files into a executable file and reuses the same for future executions.

### Executing the program

Once compiled, the binary file/executable file may then be executed by typing ./hello in the terminal. Upon execution, the compiled program will print Hello, World, followed by a newline, to the command prompt.

So, if you want to see it in reality just try compiling the .c file and you would see a new file with .exe extension created automatically if in windows with the same name as your code file. For linux it would just create a file with execute permission again with same.


### PROCESS
###`1. Editing, modifying`
.c file : File with human readable code


###`2. Compiling`
.c file --conversion--> .exe file
How ? => for gcc compiler use, `gcc -o output_file_name source_file_name.c`

###`3. Error checking`
if the file has errors, the compiler will return an error with the line number.
Modifying it according to the generic syntax is error checking.

###`4. Execution`
running the .exe file
How ? => double click the file or on command line enter ./<path_to_file>/filename.exe 
[replace path_to_file with directory path of the file]

<details>
  <summary>Want to try a Lab, Click here</summary>
##follow this
<img src="./img/compiling.png">
</details>
