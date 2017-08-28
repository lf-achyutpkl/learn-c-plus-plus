
# C++ Decision Statement

1. [if statement](#if)
2. [if...else](#ifElse)
3. [Nested if...else](#nestedIfElse)
4. [Ternary Operator](#ternary)
5. [Examples](#example)

## <a name="if"></a> if statement
The if statement evaluates the test expression inside parenthesis.
If test expression is evaluated to true, statements inside the body of if is executed.
If test expression is evaluated to false, statements inside the body of if is skipped.

Syntax
```C++
if (testExpression) 
{
  // statements
}
``` 

Example
```C++
// Program to print positive number entered by the user
// If user enters negative number, it is skipped
 
#include <iostream>
using namespace std;

int main() 
{
    int number;
    cout << "Enter an integer: ";
    cin >> number;

    // checks if the number is positive
    if ( number > 0) 
    {
        cout << "You entered a positive integer: " << number << endl;
    }

    cout << "This statement is always executed.";
    return 0;

}
```

Output 1
```
Enter an integer: 5
You entered a positive number: 5
This statement is always executed.
```

Output 2
```
Enter a number: -5
This statement is always executed.
```

## <a name="ifElse"></a> if...else statement
The if else executes the codes inside the body of if statement if the test expression is true and skips the codes inside the body of else.

If the test expression is false, it executes the codes inside the body of else statement and skips the codes inside the body of if.

Syntax
```C++
if (testExpression) {
  // statements
} else {
  // statement
}
```

Example

```C++
// Program to check whether an integer is positive or negative
// This program considers 0 as positive number

#include <iostream>
using namespace std;

int main() 
{
    int number;
    cout << "Enter an integer: ";
    cin >> number;

    if ( number >= 0)
    {
        cout << "You entered a positive integer: " << number << endl;
    }
    
    else
    {
        cout << "You entered a negative integer: " << number << endl;
    }

    cout << "This line is always printed.";
    return 0;
}
```

Output
```
Enter an integer: -4
You entered a negative integer: -4.
This line is always printed.
```

## <a name="nestedIfElse"></a> Nested if...else statement

The if...else statement executes two different codes depending upon whether the test expression is true or false. Sometimes, a choice has to be made from more than 2 possibilities.

The nested if...else statement allows you to check for multiple test expressions and execute different codes for more than two conditions.

Syntax
```C++
if (testExpression1) 
{
   // statements to be executed if testExpression1 is true
}
else if(testExpression2) 
{
   // statements to be executed if testExpression1 is false and testExpression2 is true
}
else if (testExpression 3) 
{
   // statements to be executed if testExpression1 and testExpression2 is false and testExpression3 is true
}
.
.
else 
{
   // statements to be executed if all test expressions are false
}
```

Example

```C++
// Program to check whether an integer is positive, negative or zero

#include <iostream>
using namespace std;

int main() 
{
    int number;
    cout << "Enter an integer: ";
    cin >> number;

    if ( number > 0)
    {
        cout << "You entered a positive integer: " << number << endl;
    }
    else if (number < 0)
    {
        cout<<"You entered a negative integer: " << number << endl;
    }
    else
    {
        cout << "You entered 0." << endl;
    }

    cout << "This line is always printed.";
    return 0;
}
```

Output
```
Enter an integer: 0
You entered 0.
This line is always printed.
```

## <a name="ternary"></a> Conditional/Ternary Operator ?:

A ternary operator operates on 3 operands which can be used instead of a if...else statement.

Consider this code:
```C++
if ( a < b ) {
   a = b;
}
else {
   a = -b;
}
```

You can replace the above code with:

```C++
a = (a < b) ? b : -b;
```

Ternary operator is just a shorthand for if else statement.
<p>

## <a name="example"></a> Decision Making Statement Examples

### Example 1:Find Largest Number Using if Statement

```C++
#include <iostream>
using namespace std;

int main()
{    
    float n1, n2, n3;

    cout << "Enter three numbers: ";
    cin >> n1 >> n2 >> n3;

    if(n1 >= n2 && n1 >= n3)
    {
        cout << "Largest number: " << n1;
    }

    if(n2 >= n1 && n2 >= n3)
    {
        cout << "Largest number: " << n2;
    }

    if(n3 >= n1 && n3 >= n2) {
        cout << "Largest number: " << n3;
    }

    return 0;
}
```

### Example 2: Find Largest Number Using if...else Statement

```C++
#include <iostream>
using namespace std;

int main()
{
    float n1, n2, n3;

    cout << "Enter three numbers: ";
    cin >> n1 >> n2 >> n3;

    if((n1 >= n2) && (n1 >= n3))
        cout << "Largest number: " << n1;
    else if ((n2 >= n1) && (n2 >= n3))
        cout << "Largest number: " << n2;
    else
        cout << "Largest number: " << n3;
    
    return 0;
}
```

### Example 3: Find Largest Number Using Nested if...else statement

```C++
#include <iostream>
using namespace std;

int main()
{
    float n1, n2, n3;

    cout << "Enter three numbers: ";
    cin >> n1 >> n2 >> n3;

    if (n1 >= n2)
    {
        if (n1 >= n3)
            cout << "Largest number: " << n1;
        else
            cout << "Largest number: " << n3;
    }
    else
    {
        if (n2 >= n3)
            cout << "Largest number: " << n2;
        else
            cout << "Largest number: " << n3;
    }

    return 0;
}
```
