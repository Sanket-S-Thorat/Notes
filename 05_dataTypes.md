## Basic data types:
1. `char`: used to store a single character value. 
`Size = 1 byte` 
`Range = -(2^7) to (2^7)-1 i.e. -128 to 127`
```CPP
char my_char = 'a'; // Make note that we have used single quotation and not double quotes
```

2. `int`: used to store integer values.
`Size = 4 bytes`
`Size = -(2^31) to (2^31)-1 i.e. -2,147,483,648 to 2,147,483,647`
```CPP
/* the following variables are initialized to the same value: */
int d = 42; /* decimal constant (base10) */
int o = 052; /* octal constant (base8) */
int x = 0xaf; /* hexadecimal constants (base16) */
int X = 0XAf; /* (letters 'a' through 'f' (case insensitive) represent 10 through 15) */
```
Use following formula to keep the ranges in mind:

`range = -(2^(number of bits-1)/2) to (2^(number of bits-1)/2)-1`
We negate one on positive side because of 1.

And we negate one from number of bits as the most significant bit is used as sign bit in a datatype.

i.e. for a 4byte integer | sign-bit | xxxx | xxxx | xxxx | xxxxx | xxxx | xxxx | xxxx | and each | xxxx | represents a binary representation for a number i.e. 0-9 for decimal and 0-15 for hexadecimal representation.

3. `float`: used to store floating-point values.
`Size = 4 bytes`
`Precision = upto 6 decimal places`
`Range = 1.2E-38 to 3.4E+38`
```CPP
float f = 0.314f; /* suffix f or F denotes type float */
```

4. `double`: used to store double-precision floating-point values.
`Size = 8 bytes`
`Precision = upto 15 decimal places`
`range = 2.2E-308 to 1.8E+308`
```CPP
double d = 0.314; /* no suffix denotes double */
long double ld = 0.314l; /* suffix l or L denotes long double */
```

<details>
    <summary>calculating range for  float and double can be a bit complex but if you want you can chech here</summary>

    Float/Decimal values representation  : Exponent ^ Mantissa

    range = (2 - 2^(-m)) * 2^(e-b)
    where,
        m = mantissa
        e = exponent
        b = bias
    Bias is a complex terminology just keep in mind that it is something that is added to store it as integer on backend. So we subtract that while getting the float datatype.
</details>

I advise if very new to C just read through the following types for now. We can get to this a bit later.

<details>
    <summary>Derived data types</summary>
## Derived data types:
1. `array`: used to store a collection of values of the same data type.
```CPP
int my_array[10];
```

2. `pointer`: used to store the memory address of another variable.
```CPP
int *my_pointer;
```

3. `function`: used to store a set of statements that perform a specific task.
```CPP
int my_function(int arg1, float arg2);
```
</details>

<details>
    <summary>User defined data types</summary>
## User-defined data types:
1. `struct`: used to define a new data type that contains a collection of variables of different data types.
```CPP
struct my_struct {
    int my_int;
    float my_float;
};
```

2. `union`: used to define a new data type that can store different types of data in the same memory location.
```CPP
union my_union {
    int my_int;
    float my_float;
};
```

3. `enum`: used to define a new data type that consists of a set of named constants.
```CPP
enum my_enum {
    VALUE1,
    VALUE2,
    VALUE3
};
```
</details>

C also has `modifiers` that can be used with the basic data types to modify the range or precision of the data type. The modifiers include:

As the name suggests, it modifies the data type behaves.

1. signed: used to indicate that a variable can store both positive and negative values.
2. unsigned: used to indicate that a variable can store only non-negative values.
3. short: used to indicate that a variable can store a smaller range of values than a regular variable of the same data type.
4. long: used to indicate that a variable can store a larger range of values than a regular variable of the same data type.

Just to represent the range according to modifiers,
```
Signed   ==> (-------------------------------) 0 (++++++++++++++++++++++++++++)  [eg. signed int ==> -2^31 to (2^31)-1]
Unsigned ==> 0 (+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++) [eg. unsigned int ==> 0 to (2^32)-1]
Short    ==> (-------------------------------)/2 0 (++++++++++++++++++++++++++++++++)/2 [eg. short int ==> -2^15 to (2^15)-1]
Long     ==> (-------------------------------)*2 0(+++++++++++++++++++++++++++++++++++++++++++++++)*2 [eg. long long int ==> -2^63 to (2^63)-1 and yes its long long, thats not a typo here] 

We can use, long int or long long int as per requirements to enlarge the range.

Where (+++...+++) represent range of positive integers [2^n-1]-1
and (---...---) represent range of negative integers [2^n-1]

```

Another data type would be `BOOLEAN` which has only two values --> true and false. But make note it is not a built-in data type. We need to include <stdbool.h> for using this data type.

One more data type is `VOID` void literally means no data type.