# C-Practice

* [C-Practice](#c-practice)
      * [Basics](#basics)
      * [Pointers](#pointers)
      * [Arrays and Strings](#arrays-and-strings)
      * [Input and Output](#input-and-output)
      * [Structs](#structs)
      * [Shell Scripting](#shell-scripting)
      * [Debugging and Testing](#debugging-and-testing)
      * [Misc C](#misc-c)


## Basics
1. Data types
    * Signed integers: int, short, long.
    * Unsigned integers: unsigned int, unsigned short, unsigned long (cannot be negative)    * Reals: float, double, long double
    * Characters: char (letter, digit, symbol, etc.) – technically a kind of integer.
2. Variable declarations:

    * A declaration consists of a datatype and a name:
    
    ```
    float number;        /* Declaration */    number = 5.0 * 2.5; /* Assignment  */
    ```
    
    * Declarations can also initialize variables:
    
    ```
    float number = 5.0 * 2.5;
    ```
    
    * Multiple variables can be declared at once, if they have the same data type:
    
    ```
    int alpha = 3, beta, gamma, delta = 6;
    ```

3. For loop: 

    ```
    for(int i = 0; i < 100; i++) { 
        ... 
    }
    ```

4. Comments

    * Block comments
    
    ```
    /* Speed of light    (metres per second) */
    ```
    
    * Single-line comments start with “//”
    
    ```
    int speed = 299792458; // Speed of light (m/s)
    ```
5. Switch and break
    
    ```
    switch(...) {        case 1:            ...            break;        case 2:            ...            break; 
        ...    }
    ```
    
6.  While loop -- break and continue:

    * Break a while loop
    
    ```
    while(...) {        ...        if(...) {            break;        }        ... 
    }
    ```
    
    * Continue a while loop: Jumps back to the top of the loop, and continues with the next iteration, if any.
    
    ```
    while(...) {        ...        if(...) {            continue;        }        ... 
    }
    ```
7. Function

    ```
    int someFunction(int x, float y)    {        ... 
        return result;
    }
    ```

8. Void: Can show that a function does not return a value; Can show that a function has no parameters.

    ```
    void hello(void) {        printf("Hello world.\n");    }
    ```
    
9. Printf() function
    
    ```
    printf("Hello world.\n");
    printf("Coordinates: (%d, %d)\n", x, y);
    ```
    
10. scanf() function

    ```
    int value;    printf("Enter value: ");    scanf("%d", &value);
    ```
    
11. Forward declarations: In C, the order of declaration is important (unlike Java).

    ```
    /*a prototype of function printNumber: A prototype consists of the name, parameters and return type of a function*/
    void printNumber(int number); 
        void printSum(int x, int y) {    printNumber(x + y);}
        void printNumber(int number) {    printf("%d\n", number);}
    ```

12. C program structure

    ```
    #include <stdio.h>
        void bananas(int n);    double mangos(void);
        int main(void) {    ...    return 0; }
        void bananas(int n) { ... }    double mangos(void) { ... }    ...
    
    ```

13. Compiling and running your C programs    ```
    gcc prog.c -o prog
    ./prog
    ```

## Environments
1. Header files

    In a multi-file C program:
        * Each .c file has a corresponding .h (header) file.
    * A header file declares the functions in its .c file.
    * To call those functions from a different .c file, that .c file must #include the right header file.
    * Each .c file also #includes its own header file. e.g. calc.c would also have “#include "calc.h"”.
    
    calc.c
    
    ```
    #include "calc.h" /* Include header file */
    
    double square(double n) { return n * n; }    double cube(double n)   { return n * n * n; }
    ```
    
    calc.h (header file)
    
    ```
    double square(double n); /* Declarations */double cube(double n);
    ```
    
    main.c
    
    ```
    #include "calc.h" /* Include header file */
        ...    result = square(5) + cube(5);
    ```

2. The Compilation Process
            
            C code
             |
             |  Preprocessing
            \|/
        Preprocessed C code
             |
             |  Compilation
            \|/
        Assembler code
             |
             |  Assembly
            \|/
         Object file
             |
             |  Linking
            \|/
         Executable file
         
3. Preprocessor and Directives
    * The #include Directive:
        * Use <...> for standard header files (in pre-defined directories).  
        
        ```
        #include <stdio.h>        ``` 
        * Use "..." for your own header files,in the current directory.
    
        ```        #include "myfunctions.h"
        ```    * The #define Directive
        * Assigns a name to a constant value.        * Everywhere that name occurs, the preprocessor replaces it with the given value.
        
        ```
        #define PI 3.141592654
        #define OUTPUT_STRING "Hello World!"
        ```
        
    * The #define — Macros
        * Small snippets of code with parameters (but not functions).        * Works by substitution.
        * Place brackets around macro parameters.        * Place brackets around the entire macro definition.
        
        ```
        #define SQUARE(x)  ((x) * (x))
                int squareSum(int a, int b) {            return SQUARE(a + b);        }
        ```
    
    * The #ifdef and #endif directives
        * A segment of code is only compiled if a given name has been        * \#defined (“conditional compilation”). 
        
        ```
        #define DEBUG 1
                ...        int i, sum = 0;        for(i = 0; i < 100; i++) {          sum += i;          #ifdef DEBUG          printf("%d ", sum);          #endif        }
        ```
        
4. Object Files
    * The last output is an object (.o) file for each .c file.
    * .o files contain compiled code, but they are not executable.    * They contain functions and function calls that have not yet been “linked” to each other.

5. Linking

    * Takes one or multiple .o files and produces a single executable.

    ```
    gcc -c main.c                           //compile    gcc -c other1.c                         //compile    gcc -c other2.c                         //compile    gcc main.o other1.o other2.o -o prog    //link
    ```
    
## Pointers
## Arrays and Strings
## Input and Output
## Structs
## Shell Scripting
## Debugging and Testing
## Misc C


