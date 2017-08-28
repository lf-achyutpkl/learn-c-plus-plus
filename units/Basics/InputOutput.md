# Input and Output in C++

__Write a program to take two integers from user add them and print the sum.__

```c++
  #include<iostream>

  int main(){
    int number1;
    int number2;
    int sum;

    std::cout << "Enter first integer: ";
    std::cin >> number1; // read first integer from user into number1
    std::cout << "Enter second integer: ";
    std::cin >> number2; // read second integer from user into number2

    sum = number1 + number2;

    std::cout << "Sum is " << sum << std::endl;
  }
```
## Program description

* __Obtaining _Value_ from the User__ <br/>
`std::cout << "Enter first integer: ";`
display _Enter first integer:_. This message is called a **prompt** because it directs the user to take a specific action. 

  `std::cin << number1` uses the _standard input stream object cin_ (of namespace std) and the stream extraction operator, >>, to obtain a value from the keyboard. 
  
* __Displaying the result__ <br/>
`std::cout << "Sum is " << sum << std::endl;` displays the character string _Sum is_ followed by the numerical value of variable _sum_ followed by endl --a so called __stream manipulator__. The name __endl__ is an abbreviation for "end line" and belongs to namespace _std_. <br/>
The _std::endl_ stream manipulator outputs a newline, then "flushes the output buffer".
