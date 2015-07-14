# 极客学院 Wiki 项目外部翻译试译题（C语言）
---

## A Simple Example of C

Let’s take a look at a simple C program. This program, shown in Listing 2.1, serves to point out some of the basic features of programming in C. Before you read the upcoming line-by-line explanation of the program, read through Listing 2.1 to see whether you can figure out for yourself what it will do.


```C
#include <stdio.h>
int main(void)                /* a simple program             */
{
    int num;                  /* define a variable called num */
    num = 1;                  /* assign a value to num        */

    printf("I am a simple "); /* use the printf() function    */
    printf("computer.\n");
    printf("My favorite number is %d because it is first.\n",num);

    return 0;
}
```
Listing 2.1

If you think this program will print something on your screen, you’re right! Exactly what will be printed might not be apparent, so run the program and see the results. First, use your favorite editor (or your compiler’s favorite editor) to create a file containing the text from Listing 2.1. Give the file a name that ends in .c and that satisfies your local system’s name requirements. You can use first.c, for example. Now compile and run the program. If all went well, the output should look like the following:

```C
I am a simple computer.
My favorite number is 1 because it is first.
```

## The Example Explained

### #include Directives and Header Files
`#include <stdio.h>`

This is the line that begins the program. The effect of #include <stdio.h> is the same as if you had typed the entire contents of the stdio.h file into your file at the point where the #include line appears. In effect, it’s a cut-and-paste operation. include files provide a convenient way to share information that is common to many programs.   

The #include statement is an example of a C preprocessor directive. In general, C compilers perform some preparatory work on source code before compiling; this is termed preprocessing.   

The stdio.h file is supplied as part of all C compiler packages. It contains information about input and output functions, such as printf(), for the compiler to use. The name stands for standard input/output header. C people call a collection of information that goes at the top of a file a header, and C implementations typically come with several header files.

### The main() Function
`int main(void)`

This next line from the program proclaims a function by the name of main. True, main is a rather plain name, but it is the only choice available. A C program (with some exceptions we won’t worry about) always begins execution with the function called main(). You are free to choose names for other functions you use, but main() must be there to start things. What about the parentheses? They identify main() as a function. You will learn more about functions soon. For now, just remember that functions are the basic modules of a C program.

### Declarations
`int num;`

This line from the program is termed a declaration statement. The declaration statement is one of C’s most important features. This particular example declares two things. First, somewhere in the function, you have a variable called num. Second, the int proclaims num as an integer—that is, a number without a decimal point or fractional part. (int is an example of a data type.) The compiler uses this information to arrange for suitable storage space in memory for the num variable. The semicolon at the end of the line identifies the line as a C statement or instruction. The semicolon is part of the statement, not just a separator between statements as it is in Pascal.   

The word int is a C keyword identifying one of the basic C data types. Keywords are the words used to express a language, and you can’t use them for other purposes. For instance, you can’t use int as the name of a function or a variable. These keyword restrictions don’t apply outside the language, however, so it is okay to name a cat or favorite child int. (Local custom or law may void this option in some locales.)   

### Data Types

C deals with several kinds (or types) of data: integers, characters, and floating point, for example. Declaring a variable to be an integer or a character type makes it possible for the computer to store, fetch, and interpret the data properly. You’ll investigate the variety of available types in the next chapter.

### Four Good Reasons to Declare Variables

Some older languages, such as the original forms of FORTRAN and BASIC, allow you to use variables without declaring them. So why can’t you take this easy-going approach in C? Here are some reasons:   

- Putting all the variables in one place makes it easier for a reader to grasp what the program is about. This is particularly true if you give your variables meaningful names (such as taxrate instead of r). If the name doesn’t suffice, use comments to explain what the variables represent. Documenting a program in this manner is one of the basic techniques of good programming.   

- Thinking about which variables to declare encourages you to do some planning before plunging into writing a program. What information does the program need to get started? What exactly do I want the program to produce as output? What is the best way to represent the data?   

- Declaring variables helps prevent one of programming’s more subtle and hard-to-find bugs—that of the misspelled variable name. 

- Your C program will not compile if you don’t declare your variables. If the preceding reasons fail to move you, you should give this one serious thought.

---
(End of File)	Edited by Wiki@极客学院 Jun. 24th, 2015   
940 words 5594 characters						   