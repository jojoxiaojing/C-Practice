# C-Practice
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
## Pointers
## Arrays and Strings
## Input and Output
## Structs
## Shell Scripting
## Debugging and Testing
## Misc C


