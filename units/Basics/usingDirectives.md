# _using_ Directives

> Namespaces are used to organize code into logical groups and to prevent name collisions that can occur especially when your code base includes multiple libraries.

It is just like saving files with similar names into different folders, so that both files can be saved without affecting eachother.

In previous programs, we were using std::cout, std::cin, std::endl, ([:: is a scope resolution operator](https://www.ibm.com/support/knowledgecenter/en/SSLTBW_2.3.0/com.ibm.zos.v2r3.cbclx01/cplr175.htm)).
However, We can omit that bolierplate using _using_ directive. 

Let's rewrite previous program witout repeating namespace i.e std::.

```c++
  #include<iostream>
  using namespace std;

  int main(){
    int number1;
    int number2;
    int sum;

    cout << "Enter first integer: ";
    cin >> number1; // read first integer from user into number1
    cout << "Enter second integer: ";
    cin >> number2; // read second integer from user into number2

    sum = number1 + number2;

    cout << "Sum is " << sum << endl;
  }
```

`using` directives elimate the need to repeate the std:: prefix as we did in previous programs. This enables a program to use _all_ the names in any standard C++ header (such as < iostream > that a program might include).
