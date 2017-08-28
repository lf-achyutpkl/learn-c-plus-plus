# C++ Loops

1. [while Loop](#whileLoop)
2. [do...while Loop](#doWhileLoop)
3. [for Loop](#forLoop)
4. [Nested Loop](#nestedLoop)
5. [break Statement](#break)
6. [continue Statement](#continue)

## <a name="whileLoop"></a>while Loop
A while loop statement repeatedly executes a target statement as long as a given condition is true.

```C++
  while(condition) {
   statement(s);
  }
```
Here, statement(s) may be a single statement or a block of statements. The condition may be any expression, and true is any non-zero value. The loop iterates while the condition is true.
When the condition becomes false, program control passes to the line immediately following the loop.

```C++
  #include <iostream>
  using namespace std;
  
  int main () {
    // Local variable declaration:
    int a = 10;

    // while loop execution
    while( a < 20 ) {
        cout << "value of a: " << a << endl;
        a++;
    }
  }
```

```
Output
  value of a: 10
  value of a: 11
  value of a: 12
  value of a: 13
  value of a: 14
  value of a: 15
  value of a: 16
  value of a: 17
  value of a: 18
  value of a: 19
```

## <a name="doWhileLoop"></a>do...while Loop
A do...while loop is similar to a while loop, except that a do...while loop is guaranteed to execute at least one time.

> do..while loop executes at least once even when condition is false.

```C++
  do {
    statement(s);
  } 
  while( condition );
```
Notice that the conditional expression appears at the end of the loop, so the statement(s) in the loop execute once before the condition is tested.

If the condition is true, the flow of control jumps back up to do, and the statement(s) in the loop execute again. This process repeats until the given condition becomes false.

Example

```C++
  #include <iostream>
  using namespace std;
  
  int main () {
    // Local variable declaration:
    int a = 10;

    // do loop execution
    do {
        cout << "value of a: " << a << endl;
        a = a + 1;
    } while( a < 20 );
  }
```

```
Output:
  value of a: 10
  value of a: 11
  value of a: 12
  value of a: 13
  value of a: 14
  value of a: 15
  value of a: 16
  value of a: 17
  value of a: 18
  value of a: 19
```

## <a name="forLoop"></a>for Loop

A for loop is a repetition control structure that allows you to efficiently write a loop that needs to execute a specific number of times.

```C++
  for ( init; condition; increment ) {
    statement(s);
  }
```

Here is the flow of control in a for loop −

* The init step is executed first, and only once. This step allows you to declare and initialize any loop control variables. You are not required to put a statement here, as long as a semicolon appears.

* Next, the condition is evaluated. If it is true, the body of the loop is executed. If it is false, the body of the loop does not execute and flow of control jumps to the next statement just after the for loop.

* After the body of the for loop executes, the flow of control jumps back up to the increment statement. This statement can be left blank, as long as a semicolon appears after the condition.

* The condition is now evaluated again. If it is true, the loop executes and the process repeats itself (body of loop, then increment step, and then again condition). After the condition becomes false, the for loop terminates.

```C++
  #include <iostream>
  using namespace std;
  
  int main () {
    // for loop execution
    for( int a = 10; a < 20; a = a + 1 ) {
        cout << "value of a: " << a << endl;
    }
  }
```

```
Output:
  value of a: 10
  value of a: 11
  value of a: 12
  value of a: 13
  value of a: 14
  value of a: 15
  value of a: 16
  value of a: 17
  value of a: 18
  value of a: 19
```

## <a name="nestedLoop"></a>Nested Loop

A loop can be nested inside of another loop. C++ allows at least 256 levels of nesting.

The syntax for a nested **for loop** statement in C++ is as follows:

```C++
  for ( init; condition; increment ) {
    for ( init; condition; increment ) {
        statement(s);
    }
    statement(s); // you can put more statements.
  }
```

The syntax for a nested **while loop** statement in C++ is as follows:

```C++
  while(condition) {
    while(condition) {
        statement(s);
    }
    statement(s); // you can put more statements.
  }
```

The syntax for a nested **do...while** loop statement in C++ is as follows:
```C++
  do {
    statement(s); // you can put more statements.
    do {
        statement(s);
    }while( condition );

  }while( condition );
```

The following program uses a nested for loop to find the prime numbers from 2 to 100:

```C++
  #include <iostream>
  using namespace std;
  
  int main () {
    int i, j;
    
    for(i = 2; i<100; i++) {
        for(j = 2; j <= (i/j); j++)
          if(!(i%j)) break; // if factor found, not prime
          if(j > (i/j)) cout << i << " is prime\n";
    }
  }
```
This would produce the following result:

```
  2 is prime
  3 is prime
  5 is prime
  7 is prime
  11 is prime
  13 is prime
  17 is prime
  19 is prime
  23 is prime
  29 is prime
  31 is prime
  37 is prime
  41 is prime
  43 is prime
  47 is prime
  53 is prime
  59 is prime
  61 is prime
  67 is prime
  71 is prime
  73 is prime
  79 is prime
  83 is prime
  89 is prime
  97 is prime
```

## <a name="break"></a> break statement

It is sometimes desirable to skip some statements inside the loop or terminate the loop immediately without checking the test expression.

The break statement terminates the loop (for, while and do...while loop) immediately when it is encountered.

Syntax for `break` statement
```C++
  break;
```

Example of break statement.

```C++
  // Program to calculate the sum of maximum of 10 numbers
  // Calculates sum until user enters positive number

  #include <iostream>
  using namespace std;
  int main()
  {
      int i;
      double number, sum = 0.0;
      
      for(i=1; i <= 10; ++i)
      {
          cout << "Enter a n" << i << ": ";
          cin >> number ;
          
          // If user enters negative number, loop is terminated
          if(number < 0.0)
          {
              break;
          }
          
          sum += number; // sum = sum + number;
      }
      
      cout << "Sum = " << sum;
      
      return 0;
  }
```

Output:
```
Enter a n1: 2.4
Enter a n2: 4.5
Enter a n3: 3.4
Enter a n4: -3
Sum = 10.30
```


## <a name="continue"></a> continue statement

The continue statement skips some statements inside the loop.

Syntax for `continue` statement
```C++
  continue;
```

Example of continue statement.

```C++
  // Program to calculate sum of maximum of 10 numbers
  // Negative numbers are skipped from calculation

  # include <iostream>
  using namespace std;

  int main()
  {
      int i;
      double number, sum = 0.0;
      
      for(i=1; i <= 10; ++i)
      {
          cout << "Enter a n" << i << ": ";
          cin >> number;
          
          // If user enters negative number, loop is terminated
          if(number < 0.0)
          {
              continue;
          }
          
          sum += number; // sum = sum + number;
      }
      
      cout << "Sum = " << sum;
      
      return 0;
  }
```

Output

```
Enter a n1: 1.1
Enter a n2: 2.2
Enter a n3: 5.5
Enter a n4: 4.4
Enter a n5: -3.4
Enter a n6: -45.5
Enter a n7: 34.5
Enter a n8: -4.2
Enter a n9: -1000
Enter a n10: 12
Sum = 59.70
```
