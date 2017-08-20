# First program in C++

__Let's write a program to print Hello World.__

```C++
  #include <iostream> //allows program to output data to the screen

  // function main begins program execution
  int main() {
    std::cout << "Hello World";
    
    return 0;   // indicated that program ended successfully
  } // end function main
```
## Program description

* __include Preprocessor Directive__ <br/>
`#include <iostream>`, this line notifies the proprocessor to include the content of the **input/output stream header `<iostream>`**  in it. <br/>

  This header must be included for any program that outputs data to the screen or inputs data from the keyboard using C++'s stream input/output.

* __The *main* Function__ <br/>
Main function is a part of every C++ program and it begins program execution.

* __An *Output* Statement__ <br/>
`std::cout << "Hello World";` <br/> 
instructs the computer to print the string of characters contained between the double quotation marks.

* __The _std_ namespace__<br/>
The _std::_ before _cout_ is required when we use names that we've brought into the program by the preprocessor directive **`include<iostream>`**. The notation _std::cout_ specifies that we are using a name, in this case cout, that belongs to **namespace** std.

* __The _return_ Statement__ <br/>
When the _return_ statement is used at the end of main, the value 0 indicates that the program has _terminated successfully_. 

  > According to the C++ standard, if program execution reaches the end of _main_ without encountering a **return** statement, it's assumed that the program terminated successfully -- exactly as when the last statement in main is a return statement with the value 0. **So we can omit return statement at the end of the _main_ function.**
