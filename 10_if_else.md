## PRETEXT : CONDITIONS:

Consider a case where you want to run a set of statements or block only if it meets a specific condition or criteria.

Consider a layman case:
 If I want to get a driver's license I need to be eligible and possess the driving skillset needed to get the license.

 So, say Conditions here would be like;

 1. age should be greater than or equal to 18
 2. Clear the exam test drive
 3. Clear the MCQ exam.

 In coding terms it would be like;

 ```CPP
requirements:
 age >= 18;
 test_drive == true;
 mcq_exam == true;

to get license.
 ```

 Just to put a shorthand for above;

 ```CPP
 requirements = (age>=18 && test_drive && mcq_exam) 

 to get license.
 ```

 So in similar way we can make use of && (logical AND), || (logical OR) and ~ (logical NOT) for declaring complex conditions.

## if statements:

Lets directly go to a simple code and then understand how if statement works.

Say, you went to supermarket store and you want to buy a chocolates. You being stubborn need atleast 5 chocloates so you could write code for something like this as;

<details>
    <summary>
        If you are unaware of how to take input from console/user check this
    </summary>

    ```CPP
    #include <stdio.h>

        int main() {
            int a;
            printf("Enter a number: ");
            scanf("%d", str);
            printf("You entered: %d", str);
            return 0;
    }

    Here as it was an integer we used %d same is for boolean,
    for short int we use %hd, 
    for long int we use %ld, 
    for long long int we use %lld 

    for float we use %f,
    for double we use %lf,
    for long double we use %Lf, 

    for char we use %c, 

    for string we use %s,
    for pointer we use %p,
    ```
</details>

```CPP
#include <stdio.h>

int main(){
    int no_of_chocolates ; 

    printf("Enter the number of chocolates given: ");
    scanf("%d", &no_of_chocolates); 

    if (no_of_chocolates >= 5){
        printf("I will take that!!");
    }
    return 0;
}
```

Ok to explain in short, the code will take a number from user and will check the condition, in order to mention your decision.

So, if I provided 4, as my input the condition no_of_chocolates >= 5 would turn out to be false coz. 4 < 5 so, 4>=5 ==> false. 

Hence the if statement has following ressemblance: if(false) and if statements allows to compiler to compile the code under its block only if the condition is true. So, the block wont be executed and the code would be terminated with return statement without any output.

Now to extend the above example, say guardian now mentions that you won't be getting more than 7 chocolates so the condition will be bit changed as (no_of_chocolates >= 5 && no_of_chocolates <=7) or either way you can also write it as (no_of_chocolates >= 5 && no_of_chocolates <8)

I will leave the code upto you.

Also try with an additional condition that its ok with you if you could get one soft_drink and 3 chocolates.

How ? - add a new variable to get a boolean value for soft_drink and change condition 
as ((soft_drink && no_of_chocolates >= 3) || (no_of_chocolates >= 5 && no_of_chocolates <8))

## if() else()

Now our above code is bit unclear, we do agree on getting desired no of chocolates but what if we get less than what we want.

In such a case we can use the else() clause. Which by default get executed if the condition under if() statement is false

So, our improvised code to my previous code would be;

```CPP
#include <stdio.h>

int main(){
    int no_of_chocolates ;  

    printf("Enter the number of chocolates given: ");
    scanf("%d", &no_of_chocolates); 

    if (no_of_chocolates >= 5){
        printf("I will take that!!");
    }
    else{
        printf("No deal!!!")
    }
    return 0;
}
```
So, now we have something to respond when we are not interested in what we are getting.

## if() else if() else [if else ladder]

Now lets write the code including the condition of soft_drink but with the use of else if. Luckily, for this case we can code it this way as well.
`Conditions : either no_of_chocolates >=5 or no_of_chocolates >=3 with a soft drink and no_of_chocolates <= 7 `
```CPP
#include <stdio.h>
#include <stdbool.h>   //As mentioned in data types boolean is not in built we need to include the stdbool.h for using it.

int main() {
    int no_of_chocolates;
    bool soft_drink;

    printf("Am I getting a soft drink? (0 for false, 1 for true): ");
    scanf("%d", &soft_drink);
    
    printf("Enter the number of chocolates given: ");
    scanf("%d", &no_of_chocolates);

    if (no_of_chocolates >= 5 && no_of_chocolates <= 7) {
        printf("I will take that!!");
    }else if (soft_drink == true && (no_of_chocolates >= 3 && no_of_chocolates <= 7)) {
        printf("I will take that too!!");
    }else {
        printf("No deal!!!");
    }

    return 0;
}

// Make note of the formatting difference while writing if else this was intentional to let you know C ignores identation as long as the quotes used are as per syntax rules.
```

We can also nest the if statements i.e.

```CPP
if (condition){
    if(condition){
        ...somecode
    }
    else if(condition){
        ...somecode
    }else{
        ...somecode
    }
}
else{
    if(condition){
        ...somecode
    }
    else if(condition){
        ...somecode
    }else{

    }
}
```
