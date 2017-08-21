# C++ Data Types

## Primitive Built-in Types

Following tables list down six basic C++ data types.

| Type                    | Keyword    |
|----------------------	  |----------  |
| Boolean               	| bool    	 |
| Character             	| char    	 |
| Integer               	| int     	 |
| Floating Point        	| float   	 |
| Double floating point 	| double  	 |
| Valueless             	| void    	 |

Several of the basic types can be modified using one or more of these type modifiers:

| Type               	| Typical Bit Width 	| Typical Range                                           	|
|--------------------	|-------------------	|---------------------------------------------------------	|
| char               	| 1 byte            	| -128 to 127 or 0 to 255                                 	|
| unsigned char      	| 1 byte            	| 0 to 255                                                	|
| signed char        	| 1 byte            	| -128 to 127                                             	|
| int                	| 4bytes            	| -2147483648 to 2147483647                               	|
| unsigned int       	| 4bytes            	| 0 to 4294967295                                         	|
| signed int         	| 4bytes            	| -2147483648 to 2147483647                               	|
| short int          	| 2bytes            	| -32768 to 32767                                         	|
| unsigned short int 	| 2 bytes           	| 0 to 65,535                                             	|
| signed short int   	| 2 bytes           	| -32768 to 32767                                         	|
| long int           	| 8 bytes           	| -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 	|
| unsigned long int  	| 8 bytes           	| 0 to 18,446,744,073,709,551,615                         	|
| signed long int    	| 8 bytes           	| -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 	|
| float              	| 4 bytes           	| +/- 3.4e +/- 38 (~7 digits)                             	|
| double             	| 8 bytes           	| +/- 1.7e +/- 308 (~15 digits)                           	|
| long double        	| 8 bytes           	| +/- 1.7e +/- 308 (~15 digits)                           	|

> The sizes of variables might be different from those shown in the above table, depending on the compiler and the computer you are using.

Following is the example, which will produce correct size of various data types on your computer.
```C++
  #include <iostream>
  using namespace std;

  int main() {
    cout << "Size of char : " << sizeof(char) << endl;
    cout << "Size of int : " << sizeof(int) << endl;
    cout << "Size of short int : " << sizeof(short int) << endl;
    cout << "Size of long int : " << sizeof(long int) << endl;
    cout << "Size of float : " << sizeof(float) << endl;
    cout << "Size of double : " << sizeof(double) << endl;
    return 0;
  }
```

## *typedef* Declarations

You can create a new name for an existing type using typedef. Following is the simple syntax to define a new type using typedef:

```C++ 
typedef type newname; 
```

For example, the following tells the compiler that feet is another name for int:

```C++
  typedef int feet;
```

## Enumerated Types

An enumeration is a user-defined data type that consists of integral constants. To define an enumeration, keyword **enum** is used.

```C++
  enum week { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday };
```

Here, the name of enumeration is `week`.<br/>
And  `Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday` are values of type `week`.

By default, Sunday is 0, Monday is 1 and Saturday is 6. You can change the default value of an enum element during declaration (if necessary).

```C++
  enum week {
    Sunday = 1,
    Monday = 2,
    Tuesday = 3,
    Wednesday = 4,
    Thursday = 5,
    Friday = 6,
    Saturday = 7
  };
```

Example of enum.

```C++
  #include <iostream>
  using namespace std;

  enum week { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday };

  int main()
  {
      week today;
      today = Wednesday;
      cout << "Day " << today+1;
      return 0;
  }
```

`Output: 4`
