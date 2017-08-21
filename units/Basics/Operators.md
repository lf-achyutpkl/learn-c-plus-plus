# C++ Operators

An operator is a symbol that tells the compiler to perform specific mathematical or logical manipulations.

C++ provides following types of operators:
1. Arithmetic Operators
2. Relational Operators
3. Logical Operators
4. Bitwise Operators
5. Assignment Operators

## Arithmetic Operators

Example Code

```C++
  #include <iostream>
  using namespace std;
  
  main() {
    int a = 21;
    int b = 10;
    int c ;
  
    c = a + b;
    cout << "Line 1 - Value of c is :" << c << endl ;
    c = a - b;
    cout << "Line 2 - Value of c is  :" << c << endl ;
    c = a * b;
    cout << "Line 3 - Value of c is :" << c << endl ;
    c = a / b;
    cout << "Line 4 - Value of c is  :" << c << endl ;
    c = a % b;
    cout << "Line 5 - Value of c is  :" << c << endl ;
    c = a++; 
    cout << "Line 6 - Value of c is :" << c << endl ;
    c = a--; 
    cout << "Line 7 - Value of c is  :" << c << endl ;
    return 0;
  }
```
```
Output:

  Line 1 - Value of c is :31
  Line 2 - Value of c is  :11
  Line 3 - Value of c is :210
  Line 4 - Value of c is  :2
  Line 5 - Value of c is  :1
  Line 6 - Value of c is :21
  Line 7 - Value of c is  :22
 ```

## Relational Operators

Example code

```C++
  #include <iostream>
  using namespace std;

  main() {
    int a = 21;
    int b = 10;
    int c ;

    if( a == b ) {
        cout << "Line 1 - a is equal to b" << endl ;
    } else {
        cout << "Line 1 - a is not equal to b" << endl ;
    }
    
    if ( a < b ) {
        cout << "Line 2 - a is less than b" << endl ;
    } else {
        cout << "Line 2 - a is not less than b" << endl ;
    }
    
    if ( a > b ) {
        cout << "Line 3 - a is greater than b" << endl ;
    } else {
        cout << "Line 3 - a is not greater than b" << endl ;
    }
    
    /* Let's change the values of a and b */
    a = 5;
    b = 20;
    
    if ( a <= b ) {
        cout << "Line 4 - a is either less than \
          or euqal to  b" << endl ;
    }
    
    if ( b >= a ) {
        cout << "Line 5 - b is either greater than \
          or equal to b" << endl ;
    }
    
    return 0;
  }
```

```
Output:
  Line 1 - a is not equal to b
  Line 2 - a is not less than b
  Line 3 - a is greater than b
  Line 4 - a is either less than or euqal to  b
  Line 5 - b is either greater than or equal to b
```

## Logical Operators

Example code

```C++
  #include <iostream>
  using namespace std;

  main() {
    int a = 5;
    int b = 20;
    int c ;

    if ( a && b ) {
        cout << "Line 1 - Condition is true"<< endl ;
    }
    
    if ( a || b ) {
        cout << "Line 2 - Condition is true"<< endl ;
    }
    
    /* Let's change the values of  a and b */
    a = 0;
    b = 10;
    
    if ( a && b ) {
        cout << "Line 3 - Condition is true"<< endl ;
    } else {
        cout << "Line 4 - Condition is not true"<< endl ;
    }
    
    if ( !(a && b) ) {
        cout << "Line 5 - Condition is true"<< endl ;
    }
    
    return 0;
  }
```

```
Output:
  Line 1 - Condition is true
  Line 2 - Condition is true
  Line 4 - Condition is not true
  Line 5 - Condition is true
```

## Bitwise Operators

Example code

```C++
  #include <iostream>
  using namespace std;

  main() {
    unsigned int a = 60;	  // 60 = 0011 1100  
    unsigned int b = 13;	  // 13 = 0000 1101
    int c = 0;           

    c = a & b;             // 12 = 0000 1100
    cout << "Line 1 - Value of c is : " << c << endl ;

    c = a | b;             // 61 = 0011 1101
    cout << "Line 2 - Value of c is: " << c << endl ;

    c = a ^ b;             // 49 = 0011 0001
    cout << "Line 3 - Value of c is: " << c << endl ;

    c = ~a;                // -61 = 1100 0011
    cout << "Line 4 - Value of c is: " << c << endl ;

    c = a << 2;            // 240 = 1111 0000
    cout << "Line 5 - Value of c is: " << c << endl ;

    c = a >> 2;            // 15 = 0000 1111
    cout << "Line 6 - Value of c is: " << c << endl ;

    return 0;
  }
```
```
Output:
  Line 1 - Value of c is : 12
  Line 2 - Value of c is: 61
  Line 3 - Value of c is: 49
  Line 4 - Value of c is: -61
  Line 5 - Value of c is: 240
  Line 6 - Value of c is: 15
```
## Assignment Operators

Example code

```C++
  #include <iostream>
  using namespace std;

  main() {
    int a = 21;
    int c ;

    c =  a;
    cout << "Line 1 - =  Operator, Value of c = : " <<c<< endl ;

    c +=  a;
    cout << "Line 2 - += Operator, Value of c = : " <<c<< endl ;

    c -=  a;
    cout << "Line 3 - -= Operator, Value of c = : " <<c<< endl ;

    c *=  a;
    cout << "Line 4 - *= Operator, Value of c = : " <<c<< endl ;

    c /=  a;
    cout << "Line 5 - /= Operator, Value of c = : " <<c<< endl ;

    c  = 200;
    c %=  a;
    cout << "Line 6 - %= Operator, Value of c = : " <<c<< endl ;

    c <<=  2;
    cout << "Line 7 - <<= Operator, Value of c = : " <<c<< endl ;

    c >>=  2;
    cout << "Line 8 - >>= Operator, Value of c = : " <<c<< endl ;

    c &=  2;
    cout << "Line 9 - &= Operator, Value of c = : " <<c<< endl ;

    c ^=  2;
    cout << "Line 10 - ^= Operator, Value of c = : " <<c<< endl ;

    c |=  2;
    cout << "Line 11 - |= Operator, Value of c = : " <<c<< endl ;

    return 0;
  }
```

```
Output:
  Line 1 - =  Operator, Value of c = : 21
  Line 2 - += Operator, Value of c = : 42
  Line 3 - -= Operator, Value of c = : 21
  Line 4 - *= Operator, Value of c = : 441
  Line 5 - /= Operator, Value of c = : 21
  Line 6 - %= Operator, Value of c = : 11
  Line 7 - <<= Operator, Value of c = : 44
  Line 8 - >>= Operator, Value of c = : 11
  Line 9 - &= Operator, Value of c = : 2
  Line 10 - ^= Operator, Value of c = : 0
  Line 11 - |= Operator, Value of c = : 2
```

