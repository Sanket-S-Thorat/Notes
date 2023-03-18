## Declaration

For exam : A declaration introduces an identifier and describes its type, be it a type, object, or function. A declaration is whatthe compiler needs to accept references to that identifier

For understanding:

Only providing a variable and its type is declaration.

For example;
```CPP
int bar;
signed int g;
float f(int, double);
double h1; 
long long h2; 
```

## DEFINITION

For exam : A  definition actually instantiates/implements this identifier. It's what the linker needs in order to link references to those entities

For understanding: Assigning a value to a variable is called definition irrespective of the way it's defined. Either in two statements or one.

```CPP
int bar = 4;

signed int g;  // variable declaration
g = 7;        // variable definition

float f = 1.24;
double h1 =2.3445, h2 = 4.289; // variable decalration & definition 
long long h2 = 988898798;
```