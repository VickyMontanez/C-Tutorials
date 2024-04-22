# C# A Comprehensive Developer's Guide
<img src="./img/csharp.png">

- [C# A Comprehensive Developer's Guide](#c-a-comprehensive-developers-guide)
  - [1. C# Basics Fundamentals](#1-c-basics-fundamentals)
    - [Syntax](#syntax)
    - [Primitive Types](#primitive-types)
      - [Integer Numeric Types](#integer-numeric-types)
      - [Floating-Point Numeric Types](#floating-point-numeric-types)
      - [Other Primitive Types](#other-primitive-types)
    - [Variables and Constants](#variables-and-constants)
      - [Declaring and Initializing Variables](#declaring-and-initializing-variables)
      - [Declaring and Initializing Constants](#declaring-and-initializing-constants)
    - [Operators in C#](#operators-in-c)
        - [Arithmetic Operators](#arithmetic-operators)
      - [Comparison Operators](#comparison-operators)
      - [Assignment Operators](#assignment-operators)
      - [Boolean logical Operators](#boolean-logical-operators)
      - [Increment and Decrement Operators](#increment-and-decrement-operators)
      - [Bitwise and shift Operators](#bitwise-and-shift-operators)
        - [Why use Bitwise Operators?](#why-use-bitwise-operators)
        - [Why use a Byte?](#why-use-a-byte)
        - [Why use the Binary System?](#why-use-the-binary-system)
          - [Binary Representation](#binary-representation)
          - [Bitwise Operations Example](#bitwise-operations-example)
    - [Non-Primitive Types](#non-primitive-types)
      - [Arrays](#arrays)
      - [Strings](#strings)
      - [Enumerations](#enumerations)
      - [Structs](#structs)
    - [Control Flow and Conditional Structures](#control-flow-and-conditional-structures)
      - [If-else](#if-else)
      - [Switch-case](#switch-case)
      - [Ternary operator](#ternary-operator)
    - [Loops](#loops)
      - [For Loop](#for-loop)
      - [While Loop](#while-loop)
      - [Do-While Loop](#do-while-loop)
    - [Type Conversions](#type-conversions)
      - [Implicit Conversion](#implicit-conversion)
      - [Explicit Conversion (Casting)](#explicit-conversion-casting)
    - [Boxing And Unboxing](#boxing-and-unboxing)
      - [Boxing](#boxing)
      - [Unboxing](#unboxing)
  - [2. Object-Oriented Programming in C#](#2-object-oriented-programming-in-c)
    - [Classes And Objects](#classes-and-objects)
      - [Class Structure](#class-structure)
      - [Class Coupling](#class-coupling)
      - [Objects](#objects)
    - [Inheritance](#inheritance)
    - [Composition](#composition)
    - [Polymorphism](#polymorphism)
    - [Interfaces](#interfaces)
      - [Interfaces vs Testability](#interfaces-vs-testability)
      - [Interfaces vs Extensibility](#interfaces-vs-extensibility)
    - [Abstraction](#abstraction)
    - [Encapsulation](#encapsulation)
    - [Methods](#methods)
    - [Access Modifiers](#access-modifiers)
      - [Public Modifier](#public-modifier)
      - [Private Modifier](#private-modifier)
      - [Protected Modifier](#protected-modifier)
      - [Internal Modifier](#internal-modifier)
      - [Internal Protected Modifier](#internal-protected-modifier)
      - [Readonly Modifier](#readonly-modifier)
    - [Upcasting and Downcasting](#upcasting-and-downcasting)
      - [Upcasting](#upcasting)
      - [Downcasting](#downcasting)
  - [3. System.IO in C#](#3-systemio-in-c)
    - [File Operations](#file-operations)
    - [Directory Operations](#directory-operations)
    - [Path Operations](#path-operations)
    - [Stream-based Operations](#stream-based-operations)
  - [Other Functionalities](#other-functionalities)
    - [DateTime and TimeSpan](#datetime-and-timespan)
    - [StringBuilder](#stringbuilder)
    - [StopWatch](#stopwatch)
  - [Summary and conclusions](#summary-and-conclusions)



------

## 1. C# Basics Fundamentals

C# is a powerful Object Orientated language. This documentation serves as an entry point into the world of C# programming.

### Syntax

C# is a powerful, modern programming language developed by Microsoft. Understanding its syntax is fundamental to writing efficient and effective C# code.

```csharp
using System;

namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      Console.WriteLine("Hello World!");    
    }
  }
}
```

- ***Basic Structure :***
  
  A C# program typically starts with the **using directive** to import namespaces, followed by the **namespace declaration**, which organizes code into logical groups. Inside a namespace, you define classes, methods, variables, and other elements.

- ***Main Method:***
  
  Every C# application has a Main method, which serves as the entry point for the program. It has a specific signature: **static void Main(string[] args)**. Code execution begins from here.

- ***Variables and Data Types:***
  
  C# supports various data types, including **integers (int, long)**, **floating-point numbers (float, double)**, **characters (char)**, **strings (string)**, bo**olean (bool)**, and more. Variables must be declared with a specific type before they can be used.

- ***Control Structures:***
  
  C# offers familiar control structures like **if**, **else**, **switch**, **for**, **while**, and **do-while**, which are used to control the flow of execution based on conditions and loops.

- ***Classes and Objects:***
  
  **Object-oriented programming (OOP)**  is a core concept in C#. You define classes to represent real-world entities or abstract concepts. Objects are instances of classes, encapsulating data and behavior. Classes can have fields, properties, methods, constructors, and events.

- ***Exception Handling:***
  
  C# provides mechanisms for handling runtime errors and exceptions using try, catch, finally, and throw blocks.

- ***Generics:***
  
  Generics allow you to create reusable, type-safe code by defining classes, interfaces, and methods with placeholder types.

- ***Lambda Expressions:***
  
  Lambda expressions provide a concise way to define anonymous methods, which are often used in LINQ queries and event handling.

### Primitive Types
Primitive types in C# are the basic building blocks for constructing more complex data structures. They include:

#### Integer Numeric Types

In C#, integer numeric types represent whole numbers without any fractional component. These types are used to store integer values such as counts, indices, or identifiers. 

- **int**: Represents Signed 32-bit Integers. It can store values in the range of -2,147,483,648 to 2,147,483,647. This is the most commonly used integer type in C#.
  ```c#
  int number = 10;
  ```
  
- **long**: Represents Signed 64-bit Integers. It can store values in the range of -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.
  ```c#
  long bigNumber = 10000000000L;
  ```

- **short**: Represents Signed 16-bit Integers. It can store values in the range of -32,768 to 32,767.
    ```c#
    short smallNumber = 100;
    ```
  
- **byte**: Represents Unsigned 8-bit Integers. It can store values in the range of 0 to 255.
    ```c#
    byte smallPositiveNumber = 200;
    ```

- **sbyte**: Represents Signed 8-bit Integers. It can store values in the range of -128 to 127.
    ```c#
    sbyte smallNumber = -100;
    ```

- **uint**: Represents Unsigned 32-bit integers. It can store values in the range of 0 to 4,294,967,295.
    ```c#
    uint positiveNumber = 2000U;
    ```

- **ulong**: Represents Unsigned 64-bit Integers. It can store values in the range of 0 to 18,446,744,073,709,551,615.
    ```c#
    ulong bigPositiveNumber = 10000000000UL;
    ```

- **ushort**: Represents Unsigned 16-bit Integers. It can store values in the range of 0 to 65,535.
    ```c#
    ushort smallPositiveNumber = 30000;
    ```

#### Floating-Point Numeric Types
Floating-point numeric types in C# are used to represent numbers with fractional components. These types are suitable for representing real numbers such as measurements, scientific values, and financial data. 

- **float**: Represents Single-precision floating-point numbers. It can store values with approximately 7 significant digits and has a range of approximately ±1.5 × 10^-45 to ±3.4 × 10^38.
    ```c#
    float floatValue = 3.14f;
    ```
- **double**: Represents Double-precision floating-point numbers. It can store values with approximately 15-16 significant digits and has a range of approximately ±5.0 × 10^-324 to ±1.7 × 10^308. This is the most commonly used floating-point type in C#.
    ```c#
    double doubleValue = 3.141592653589793;
    ```
- **decimal**: Represents Decimal floating-point numbers of high precision. It is primarily used for financial and monetary calculations where precision and rounding are crucial. It can store values with approximately 28-29 significant digits and has a range of approximately ±1.0 × 10^-28 to ±7.9 × 10^28.
    ```c#
    decimal decimalValue = 123.456m;
    ```

#### Other Primitive Types
- **char**: The char type represents a single Unicode character. It occupies 2 bytes of memory and can store any Unicode character, including letters, digits, symbols, and whitespace.
    ```c#
    char character = 'A';
    ```
- **bool**: The bool type represents a Boolean value, which can be either true or false. It is commonly used for logical operations, conditional statements, and boolean algebra.
  
    ```c#
     bool isTrue = true;
     bool isFalse = false;
    ```

### Variables and Constants

Variables and constants are similar; they are named storage locations that hold data. However, the values of variables can change during the execution of a program, whereas the values of constants cannot be changed after they are initialized. Both variables and constants must be declared with a specific type before they can be used.

#### Declaring and Initializing Variables

In C#, declaring a variable is all about specifying the name of the variable you want to create. The basic syntax for declaring a variable is as follows:

```csharp
// dataType variableName = value;
```

Where:

- **Datatype**: This is the data type of the variable.
- **VariableName**: This is the name of the variable you want to initialize.
- **Value**: This is the value you want to assign to the variable.

For example, if you want to declare and initialize an age variable of type int with the value 25, you can do it as follows:

```c#
int age; // Declaration of an integer variable
age = 25; // Assignment of a value to the variable
```

#### Declaring and Initializing Constants

In C#, constants are different from variables in that they are declared using the keyword `const`. The basic syntax for declaring a constant is as follows:

```c#
// const  dataType variableName = value;
```

Where:

- **const**: This is the key word for declaring a constant.
- **Datatype**: This is the data type of the variable.
- **VariableName**: This is the name of the variable you want to initialize.
- **Value**: This is the value you want to assign to the variable.

Unlike variables, ***the values of constants cannot be changed after they are initialized.*** Both variables and constants must be declared with a specific type before they can be used.

For example, if you want to declare and initialize a PI constant of type double with the value of pi (approximately 3.14159), you can do so as follows:

```c#
const double PI = 3.14159;
```

### Operators in C#
C# provides a variety of operators, many of which are supported by the built-in types, enabling you to perform fundamental operations with values of those types. Those operators include the following groups:

- **Arithmetic operators** that perform arithmetic operations with numeric operands.
- **Comparison operators** that compare numeric operands.
- **Assignament operators** assign values to variables.
- **Boolean logical operators** that perform logical operations with bool operands.
- **Increment and Decrement operators** modify the value of a variable by one.
- **Bitwise and shift operators** that perform bitwise or shift operations with operands of the integral types.

  
##### Arithmetic Operators
These operators are used to perform basic mathematical operations, such as addition, subtraction, multiplication, division, and modulus.

<img src="./img/AritOp.png" />

```c#
int a = 10;
int b = 5;
int add = a + b;		   //add = 15
int subtract = a - b;      //subtract = 5
int multiply = a * b;      //multiply = 50
int divide = a / b;        //divide = 2
int remainder = a % b;     //remainder = 0
```

#### Comparison Operators
These operators are used to compare values and return a Boolean value (true or false).

<img src="./img/ComOp.png" />

```c#
int a = 10;
int b = 5;
bool equal = (a == b);        //equal = false
bool notEqual = (a != b);     //notEqual = true
bool greaterThan = (a > b);   //greaterThan = true
bool lessThan = (a < b);      //lessThan = false
```

#### Assignment Operators
These operators are used to assign values to variables.

<img src="./img/AssigOp.png" />

```c#
int x = 10;
x += 5;   // x is now 15 (equivalent to x = x + 5)
x -= 3;   // x is now 12 (equivalent to x = x - 3)
x *= 2;   // x is now 24 (equivalent to x = x * 2)
x /= 4;   // x is now 6  (equivalent to x = x / 4)
x %= 5;   // x is now 1  (equivalent to x = x % 5)
```

#### Boolean logical Operators
These operators are used to combine logical expressions and return a Boolean value.

<img src="./img/LoOp.png" />

```c#
bool c1 = true;
bool c2 = false;
bool resultAnd = c1 && c2;   // resultAnd = false
bool resultOr = c1 || c2;    // resultOr = true
bool resultNot = !c1;        // resultNot = false
```

#### Increment and Decrement Operators
These operators are used to increase or decrease the value of a variable by one unit.

<img src="./img/InDeOp.png" />

```c#
int x = 10;
x++;  // Increment: x is now 11
x--;  // Decrement: x is now 10 again
```

#### Bitwise and shift Operators
These operators are used to perform operations at ***the bit level*** on ***binary representations*** of data.

##### Why use Bitwise Operators?
Bitwise operations were more prevalent in the past when computers had limited memory compared to contemporary systems.

If you're working on embedded devices with memory limitations, bitwise operations remain highly relevant and valuable. It's essential to have a good understanding of them in such contexts.

##### Why use a Byte?
The smallest unit of addressable space that a CPU can reference is typically one byte. This means that the smallest amount of space a variable can occupy in memory is one byte.
<img src="./img/byte.png"/>

##### Why use the Binary System?
"Binary" is a numeral system that uses a base of 2. In the binary system, each digit or bit can have one of two possible values: 0 or 1. This contrasts with the decimal system (base-10), which we commonly use, where each digit can have one of ten possible values (0 through 9).

<img src="./img/image.png"/>

In computing, binary is fundamental because computers use binary digits (bits) to represent and manipulate data internally. Everything in a computer is ultimately represented using binary, including numbers, text, images, and instructions. 

***Understanding binary is essential for understanding how computers store and process information at the lowest level.***

###### Binary Representation
Binary representation is used to represent numbers in base-2 format using only 0s and 1s. When we talk about a byte, we're referring to a group of 8 bits. Each bit in a byte can be either 0 or 1, which aligns perfectly with binary representation. 

***numeral system with a base of 2.***
<img src="./img/notation.png"/>

For example, let's convert the decimal number 13 into binary:

To do this, we can repeatedly divide 13 by 2, keeping track of the remainders. Here's the process:
```c#
13 ÷ 2 = 6    //remainder 1
6 ÷ 2 = 3     //remainder 0
3 ÷ 2 = 1     //remainder 1
1 ÷ 2 = 0     //remainder 1
```
Reading the remainders from bottom to top, **we get 1101**. So, the binary representation of the decimal number 13 is 1101 in base-2.

Now backwards, let's convert the binary 1101 into a decimal number:

To convert binary to decimal, we multiply each bit by 2 raised to its respective power and sum the results. 

<img src="./img/not.png" />
<img src="./img/example.png" />

```c#
1 * 2^0 = 1
0 * 2^1 = 0
1 * 2^2 = 4
1 * 2^3 = 8
```
Adding these together:
<img src="./img/result.png" />
So, the binary number 1101 is equal to the decimal number 13.

###### Bitwise Operations Example
<img src="./img/BitOp.png" />

```c#
int a = 5;     // binary representation: 00000101
int b = 3;     // binary representation: 00000011

//AND: Compares bits from two numbers. If both bits at the same position are 1, the resulting bit is 1.
int resultAnd = a & b;    // Bitwise AND: 00000001 (1)

//OR: Compares bits from two numbers. If at least one bit at the same position is 1, the resulting bit is 1.
int resultOr = a | b;     // Bitwise OR: 00000111 (7)

//XOR: Compares bits from two numbers. If the bits at the same position are different, the resulting bit is 1.
int resultXor = a ^ b;    // Bitwise XOR: 00000110 (6)

//NOT: Inverts each bit in a number. 0s become 1s and 1s become 0s.
int resultNot = ~a;       // Bitwise NOT: 11111010 (-6)

//LEFT SHIFT: Shifts all bits of a number to the left, introducing zeros on the right side.
int resultShiftLeft = a << 1;  // Left Shift: 00001010 (10)

//RIGHT SHIFT: Shifts all bits of a number to the right, introducing zeros on the left side.
int resultShiftRight = a >> 1; // Right Shift: 00000010 (2)

```

### Non-Primitive Types
Non-primitive types in C# are data types that are composed of primitive types or other non-primitive types. They include:
- Arrays
- Strings
- Enumerations
- Structs

#### Arrays
Arrays are data structures that store a fixed-size sequential collection of elements of the same type.

```c#
int[] numbers = new int[5]; // Declaration and instantiation of an integer array
numbers[0] = 1;
numbers[1] = 2;
// Accessing elements of the array
Console.WriteLine(numbers[0]); // Output: 1
Console.WriteLine(numbers[1]); // Output: 2

int[] numbers = new int[5] {1,2,3,4,5} //Declaration and initiation of the array
```
Some methods that are frequently used to manipulate arrays in C# offer functionality such as copying, searching, sorting, and modifying array elements.

1. **Length Property:**
   - **Description:** Gets the total number of elements in the array.
   - **Example:**
     ```csharp
     int[] numbers = { 1, 2, 3, 4, 5 };
     int length = numbers.Length; // length will be 5
     ```

2. **Copy Method:**
   - **Description:** Copies a range of elements from an array starting at the specified source index and pastes them to another array starting at the specified destination index.
   - **Example:**
     ```csharp
     int[] sourceArray = { 1, 2, 3 };
     int[] destinationArray = new int[3];
     Array.Copy(sourceArray, destinationArray, 3); // Copies all elements from sourceArray to destinationArray
     ```

3. **Clear Method:**
   - **Description:** Sets a range of elements in the array to zero, false, or null, depending on the element type.
   - **Example:**
     ```csharp
     int[] numbers = { 1, 2, 3, 4, 5 };
     Array.Clear(numbers, 0, numbers.Length); // Clears all elements in the numbers array
     ```

4. **IndexOf Method:**
   - **Description:** Searches for the specified object and returns the index of its first occurrence within the entire array.
   - **Example:**
     ```csharp
     int[] numbers = { 1, 2, 3, 4, 5 };
     int index = Array.IndexOf(numbers, 3); // index will be 2
     ```

5. **Reverse Method:**
   - **Description:** Reverses the sequence of elements in the entire array.
   - **Example:**
     ```csharp
     int[] numbers = { 1, 2, 3, 4, 5 };
     Array.Reverse(numbers); // numbers will be { 5, 4, 3, 2, 1 }
     ```

6. **Sort Method:**
   - **Description:** Sorts the elements in an entire array using the IComparable implementation of each element of the array.
   - **Example:**
     ```csharp
     int[] numbers = { 5, 3, 1, 4, 2 };
     Array.Sort(numbers); // numbers will be { 1, 2, 3, 4, 5 }
     ```

7. **Resize Method:**
   - **Description:** Changes the size of the array to a specified new size.
   - **Example:**
     ```csharp
     int[] numbers = { 1, 2, 3 };
     Array.Resize(ref numbers, 5); // Resizes the numbers array to have a length of 5
     ```

#### Strings
Strings are sequences of characters used to represent text. In C#, strings are immutable, meaning their values cannot be changed after they are created.

```c#
string greeting = "Hello, world!"; // Declaration and initialization of a string
Console.WriteLine(greeting); // Output: Hello, world!
```
Some methods that are frequently used to manipulate strings in C# offer functionality such as extracting substrings, changing casing, searching for substrings, splitting strings into substrings, and replacing substrings.

1. **Length Property:**
   - **Description:** Gets the number of characters in the current string.
   - **Example:**
     ```csharp
     string str = "Hello, world!";
     int length = str.Length; // length will be 13
     ```

2. **Substring Method:**
   - **Description:** Retrieves a substring from this instance. The substring starts at a specified character position and has a specified length.
   - **Example:**
     ```csharp
     string str = "Hello, world!";
     string subStr = str.Substring(7, 5); // subStr will be "world"
     ```

3. **ToUpper Method:**
   - **Description:** Returns a copy of this string converted to uppercase.
   - **Example:**
     ```csharp
     string str = "hello";
     string upperStr = str.ToUpper(); // upperStr will be "HELLO"
     ```

4. **ToLower Method:**
   - **Description:** Returns a copy of this string converted to lowercase.
   - **Example:**
     ```csharp
     string str = "HELLO";
     string lowerStr = str.ToLower(); // lowerStr will be "hello"
     ```

5. **Contains Method:**
   - **Description:** Returns a value indicating whether a specified substring occurs within this string.
   - **Example:**
     ```csharp
     string str = "Hello, world!";
     bool contains = str.Contains("world"); // contains will be true
     ```

6. **Split Method:**
   - **Description:** Splits a string into substrings based on the characters in an array and returns an array of substrings.
   - **Example:**
     ```csharp
     string str = "apple,banana,orange";
     string[] fruits = str.Split(','); // fruits will be ["apple", "banana", "orange"]
     ```

7. **IndexOf Method:**
   - **Description:** Reports the zero-based index of the first occurrence of a specified string within this instance.
   - **Example:**
     ```csharp
     string str = "Hello, world!";
     int index = str.IndexOf("world"); // index will be 7
     ```

8. **Replace Method:**
   - **Description:** Returns a new string in which all occurrences of a specified substring in the current string are replaced with another specified substring.
   - **Example:**
     ```csharp
     string str = "Hello, world!";
     string newStr = str.Replace("world", "universe"); // newStr will be "Hello, universe!"
     ```

#### Enumerations
Enumerations, or enums, are special value types that allow you to define named constants with a specific underlying type. Enumerations provide a way to create sets of related named constants, making code more readable and maintainable.

```c#
enum DaysOfWeek
{
    Sunday,
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday,
    Saturday
}

DaysOfWeek today = DaysOfWeek.Monday;
Console.WriteLine(today); // Output: Monday
```
Some methods of enums are frequently used to retrieve the name of a constant based on its value or to check if a given value or name exists in the enum.

1. **GetName Method:**
   - **Description:** Retrieves the name of the constant in the specified enumeration that has the specified value.
   - **Example:**
     ```csharp
     enum DaysOfWeek
     {
         Sunday,
         Monday,
         Tuesday,
         Wednesday,
         Thursday,
         Friday,
         Saturday
     }
     
     string day = Enum.GetName(typeof(DaysOfWeek), 1); // Returns "Monday"
     ```

2. **IsDefined Method:**
   - **Description:** Returns a Boolean indicating whether a given integral value, or its name as a string, exists in the specified enumeration.
   - **Example:**
     ```csharp
     enum DaysOfWeek
     {
         Sunday,
         Monday,
         Tuesday,
         Wednesday,
         Thursday,
         Friday,
         Saturday
     }
     
     bool isDefined = Enum.IsDefined(typeof(DaysOfWeek), "Monday"); // Returns true
     ```

#### Structs
Structs are similar to classes but are value types rather than reference types. They are typically used for small, lightweight objects that have a short lifetime and do not require inheritance or polymorphism.

```c#
struct Point
{
    public int X;
    public int Y;

    public Point(int x, int y)
    {
        X = x;
        Y = y;
    }
}

Point p1 = new Point(1, 2);
Console.WriteLine($"X: {p1.X}, Y: {p1.Y}"); // Output: X: 1, Y: 2
```
Structs can contain methods like: constructors, equality comparison methods, hash code generation methods, and custom methods as required by your application.

1. **Constructor:**
   - **Description:** Initializes an instance of the struct.
   - **Example:**
     ```csharp
     public struct Point
     {
         public int X { get; }
         public int Y { get; }
     
         // Constructor
         public Point(int x, int y)
         {
             X = x;
             Y = y;
         }
     }
     
     Point p = new Point(3, 4);
     ```

2. **Equals Method:**
   - **Description:** Determines whether the current object is equal to another object of the same type.
   - **Example:**
  
     ```csharp
     public struct Point
     {
         public int X { get; }
         public int Y { get; }
     
         public override bool Equals(object obj)
         {
             if (!(obj is Point))
                 return false;
     
             Point otherPoint = (Point)obj;
             return X == otherPoint.X && Y == otherPoint.Y;
         }
     }
     
     Point p1 = new Point(3, 4);
     Point p2 = new Point(3, 4);
     bool isEqual = p1.Equals(p2); // Returns true
     ```

3. **GetHashCode Method:**
   - **Description:** Serves as the default hash function.
   - **Example:**
     ```csharp
     public struct Point
     {
         public int X { get; }
         public int Y { get; }
     
         public override int GetHashCode()
         {
             return X.GetHashCode() ^ Y.GetHashCode();
         }
     }
     
     Point p = new Point(3, 4);
     int hashCode = p.GetHashCode(); // Returns a unique hash code
     ```

4. **ToString Method:**
   - **Description:** Returns a string that represents the current object.
   - **Example:**
     ```csharp
     public struct Point
     {
         public int X { get; }
         public int Y { get; }
     
         public override string ToString()
         {
             return $"({X}, {Y})";
         }
     }
     
     Point p = new Point(3, 4);
     string pointStr = p.ToString(); // Returns "(3, 4)"
     ```

5. **Custom Methods:**
   - **Description:** Methods defined by the programmer to perform specific actions or calculations.
   - **Example:**
     ```csharp
     public struct Rectangle
     {
         public int Width { get; }
         public int Height { get; }
     
         public Rectangle(int width, int height)
         {
             Width = width;
             Height = height;
         }
     
         public int CalculateArea()
         {
             return Width * Height;
         }
     }
     
     Rectangle rect = new Rectangle(5, 3);
     int area = rect.CalculateArea(); // area will be 15
     ```

### Control Flow and Conditional Structures

Control flow refers to the order in which the individual statements, instructions, or function calls of a program are executed. Conditional structures are programming constructs that allow decisions to be made within the code based on certain conditions. These conditions determine which block of code will be executed next.

**Conditional Structures:**

#### If-else 
   The if-else statement is used to execute a block of code if a specified condition is true, and another block of code if the condition is false.

   ```c#
   int age = 18;
   if (age >= 18)
   {
       Console.WriteLine("You are an adult.");
   }
   else
   {
       Console.WriteLine("You are a minor.");
   }
   ```

#### Switch-case
   The switch-case statement provides a way to execute different blocks of code based on the value of an expression or variable.

   ```c#
   char operation = '*';
   double num1 = 10;
   double num2 = 5;
   double result = 0;
   
   switch (operation)
   {
       case '+':
           result = num1 + num2;
           break;
       case '-':
           result = num1 - num2;
           break;
       case '*':
           result = num1 * num2;
           break;
       case '/':
           result = num1 / num2;
           break;
       default:
           Console.WriteLine("Invalid operation.");
           break;
   }
   
   Console.WriteLine("The result is: " + result);
   ```
#### Ternary operator
   The ternary operator is a shorthand version of an if-else statement and is used to assign a value to a variable based on a condition.

   ```c#
   int number = 10;
   string message = (number % 2 == 0) ? "It's even" : "It's odd";
   Console.WriteLine(message);
   ```

These conditional structures are essential for creating flexible and dynamic programs that can adapt their behavior based on different inputs or circumstances. They are fundamental tools for controlling the flow of execution in a program and implementing various decision-making logic.

### Loops
In C#, loops are used to repeat a block of code multiple times, enabling efficient handling of repetitive tasks and processing of data collections. They allow for precise control over program flow and are essential for implementing algorithms and automating tasks efficiently.

#### For Loop
The for loop is used to execute a block of code a specified number of times.
   - **Structure**: 
     ```csharp
     for (initialization; condition; iteration)
     {
         // code to be executed
     }
     ```
   - **Functionality**: 
     - Initialization: Executes once at the beginning of the loop.
     - Condition: Checked before each iteration. If true, the loop continues; otherwise, it exits.
     - Iteration: Executes after each iteration of the loop.
   - **Example**:
     ```csharp
     for (int i = 0; i < 5; i++)
     {
         Console.WriteLine(i);
     }
     ```
   - **Common Use**: *Iterating over arrays, collections, or a range of values.*

#### While Loop
The while loop executes a block of code as long as a specified condition is true.
   - **Structure**: 
     ```csharp
     while (condition)
     {
         // code to be executed
     }
     ```
   - **Functionality**: 
     - The condition is checked before each iteration. If true, the loop continues; otherwise, it exits.
   - **Example**:
     ```csharp
     int num = 0;
     while (num < 5)
     {
         Console.WriteLine(num);
         num++;
     }
     ```
   - **Common Use**: *Executing code based on a condition that may change during execution.*

#### Do-While Loop
  The do-while loop is similar to a while loop, but it guarantees that the code inside the loop is executed at least once before the condition is checked.
  - **Structure**: 
     ```csharp
     do
     {
         // code to be executed
     } while (condition);
     ```
   - **Functionality**: 

    The code inside the loop is executed once before checking the condition. If true, the loop continues; otherwise, it exits.
    **Example**:
    
     ```c#
     int num = 0;
     do
     {
         Console.WriteLine(num);
         num++;
     } while (num < 5);
     ```
   - **Common Use**: *Ensuring a block of code is executed at least once, regardless of the condition.*

### Type Conversions
Type conversions in C# refer to the process of converting a value from one data type to another. There are two main types of conversions: implicit conversions and explicit conversions (casting).

#### Implicit Conversion
Implicit conversion occurs automatically when there is no risk of data loss during the conversion. It's performed by the compiler without requiring any additional syntax. This type of conversion is typically used when converting smaller data types to larger ones.

```c#
int numInt = 10;
double numDouble = numInt; // Implicit conversion from int to double
```

**Use Case:**
Implicit conversions are commonly used when assigning a value of a smaller data type to a larger data type, such as converting an integer to a floating-point number.

#### Explicit Conversion (Casting)
Explicit conversion, also known as casting, is a manual conversion process where the programmer explicitly specifies the desired target data type. This type of conversion is necessary when there's a risk of data loss or when converting from a larger data type to a smaller one.

```c#
double numDouble = 10.5;
int numInt = (int)numDouble; // Explicit conversion (casting) from double to int
```
**Use Case:**
Explicit conversions are used when converting from a larger data type to a smaller one, such as converting a floating-point number to an integer. It's also used when converting between data types that aren't implicitly convertible, such as converting between numerical and non-numerical types.

### Boxing And Unboxing

Boxing and unboxing are operations used to convert value types to reference types and vice versa. They involve performance overhead and should be used judiciously.

#### Boxing
Boxing is the process of converting a value type (such as an integer, float, or struct) to a reference type (such as object).
When you box a value type, a new object is created on the heap, and the value of the value type is copied into that object.

```csharp
int i = 42; // value type
object obj = i; // Boxing: i is boxed into obj
```

#### Unboxing
Unboxing is the process of converting a reference type (typically an object) back to a value type. When you unbox an object, the runtime checks if the object is of the expected type, and if so, it retrieves the value of the boxed value type. Unboxing is an explicit conversion, meaning you need to explicitly cast the reference type back to the value type.

```csharp
int i = 42;
object obj = i; // Boxing: i is boxed into obj
int j = (int)obj; // Unboxing: obj is unboxed back to int
```

## 2. Object-Oriented Programming in C#

<img src="./img/OOP.jpeg">

### Classes And Objects
Classes are reference types that serve as blueprints for creating objects. They encapsulate data for the object and define methods for manipulating that data. Classes support inheritance, encapsulation, and polymorphism, allowing for the creation of complex data structures and behavior.

<img src="./img/clsob.png">

```c#
class Person
{
    public string Name { get; set; }
    public int Age { get; set; }

    public void PrintInfo()
    {
        Console.WriteLine($"Name: {Name}, Age: {Age}");
    }
}

Person person1 = new Person();
person1.Name = "John";
person1.Age = 30;
person1.PrintInfo(); // Output: Name: John, Age: 30
```
#### Class Structure

1. **Fields:**
   - **Description:** Fields are variables declared within a class to store data. They represent the state of an object.
   - **Example:**
     ```csharp
     class Person
     {
         public string Name; // Field
         public int Age;     // Field
     }
     ```

2. **Properties:**
   - **Description:** Properties provide a way to encapsulate fields, allowing controlled access to the data stored in a class.
   - **Example:**
     ```csharp
     class Person
     {
         private string name; // Field
         public string Name   // Property
         {
             get { return name; }
             set { name = value; }
         }
     }
     ```

3. **Access Modifiers:**
   - **Description:** Access modifiers control the accessibility of classes, methods, and other members within a program.
   - **Example:**
     ```csharp
     public class MyClass    // Public class
     {
         private int myField; // Private field
         public void MyMethod() { } // Public method
     }
     ```

4. **Static Members:**
   - **Description:** Static members belong to the class itself rather than to instances of the class. They are shared among all instances of the class.
   - **Example:**
     ```csharp
     class Circle
     {
         public static double Pi = 3.14;
     }
     double area = Circle.Pi * radius * radius;
     ```

5. **Constructor:**
   - **Description:** Initializes an instance of the class.
   - **Example:**
     ```csharp
     public class Person
     {
         public string Name { get; set; }
         public int Age { get; set; }
     
         // Constructor
         public Person(string name, int age)
         {
             Name = name;
             Age = age;
         }
     }
     
     Person person1 = new Person("John", 30);
     ```

#### Class Coupling
Class coupling refers to the degree of interdependence between classes in object-oriented programming. High coupling indicates tight connections between classes, making them highly dependent on each other. Conversely, low coupling implies classes are more independent, which promotes flexibility and maintainability.

There are various types of class coupling:

* **Content Coupling:** A class directly accesses or modifies the internal state of another class. This is considered the tightest form of coupling.
```c#
    class ClassA
    {
        private ClassB b;

        public void Method() {

            b.SomeMethod();

        }
    }
```
* **Common Coupling:** Classes share a common global data. Changes in the shared data affect multiple classes
```c#
    static class Common 
    {
        public static int Data;
    }

    class ClassA 
    {
        public void Method() 
        {
            Common.Data = 10;
        }
    }

    class ClassB 
    {
        public void Method() 
        {
            int data = Common.Data;
        }
    }

```
* **Control Coupling:** One class controls the flow of execution of another by passing control information.
```c#
    class ClassA 
    {
        public void Method(ClassB b) 
        {
            b.Process();
        }
    }

    class ClassB 
    {
        public void Process() 
        {
            // Do something
        }
    }
```
* **Stamp Coupling:** Classes share a composite data structure and use only a part of it.
```c#
    class Composite
    {
        public int Data;
        public string Info;
    }

    class ClassA 
    {
        public void Method(Composite c) 
        {
            int data = c.Data;
        }
    }

    class ClassB 
    {
        public void Method(Composite c) 
        {
            string info = c.Info;
        }
    }
```
* **Data Coupling:** Classes communicate by passing data through method parameters or return values. This is considered the loosest form of coupling.
```c#
    class ClassA 
    {
        public void Method(int data) 
        {
            // Do something with data
        }
    }

    class ClassB 
    {
        public int Method() 
        {
            // Generate some data
            return 10;
        }
    }
```
**Reducing class coupling is crucial for writing maintainable and flexible code.** Strategies for reducing coupling include applying design principles like SOLID, dependency injection, and using interfaces to decouple implementations.

#### Objects

Objects are instances of classes. They encapsulate both data and behavior defined by the class.

- **Instantiation:**
  - **Description:** Instantiation is the process of creating an object from a class.
  - **Example:**
    ```csharp
    Person person1 = new Person("John", 30);
    ```

- **Accessing Members:**
  - **Description:** Objects can access the members (fields, properties, methods) defined in their class.
  - **Example:**
    ```csharp
    string name = person1.Name;
    int age = person1.Age;
    person1.PrintInfo();
    ```

- **Multiple Instances:**
  - **Description:** Multiple objects can be created from the same class, each with its own set of data and behavior.
  - **Example:**
    ```csharp
    Person person2 = new Person("Alice", 25);
    ```

- **Object Initialization:**
  - **Description:** Objects can be initialized with data using constructors or by setting property values after instantiation.
  - **Example:**
    ```csharp
    Person person3 = new Person { Name = "Bob", Age = 35 };
    ```

- **Object Comparison:**
  - **Description:** Objects can be compared for equality using the Equals method or other comparison techniques.
  - **Example:**
    ```csharp
    bool isEqual = person1.Equals(person2);
    ```

### Inheritance

Inheritance is a fundamental concept in object-oriented programming that allows a class (the child or derived class) to inherit properties and behavior from another class (the parent or base class). It promotes code reuse and enables the creation of hierarchical relationships between classes.

  <img src="./img/Inh.png">

- **Base Class:** Also known as the parent or superclass, it's the class whose members are inherited by another class.
- **Derived Class:** Also known as the child or subclass, it's the class that inherits from another class.
- **Syntax:**
  ```csharp
  class BaseClass
  {
      // Base class members
  }
  
  class DerivedClass : BaseClass
  {
      // Derived class members
  }
  ```
- **Example:**
  ```csharp
  class Animal
  {
      public void Eat()
      {
          Console.WriteLine("Animal is eating.");
      }
  }
  
  class Dog : Animal
  {
      // Dog inherits the Eat() method from Animal
  }
  ```

### Composition

Composition in C# involves constructing complex objects by combining simpler ones. It promotes code reuse and maintains flexibility in object relationships.

<img src="./img/comp.jpeg">

- **Benefits:**
  * Promotes encapsulation
  * Enables better code reuse
  * Maintains loose coupling between components
- **Example:**
  ```csharp
    using System;
    // Component class
    public class Engine
    {
        public void Start()
        {
            Console.WriteLine("Engine started.");
        }
    }

    // Container class
    public class Car
    {
        // Member variable representing the Engine component
        private readonly Engine _engine;

        // Constructor where we initialize the Engine component
        public Car()
        {
            _engine = new Engine();
        }

        // Method to start the Car, which internally starts the Engine
        public void Start()
        {
            _engine.Start();
            Console.WriteLine("Car started.");
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            // Create an instance of the Car class
            Car car = new Car();

            // Call the Start method of the Car, which in turn starts the Engine
            car.Start();
        }
    }
  ```

### Polymorphism

Polymorphism is the ability of objects to take on multiple forms. In the context of inheritance, it allows a method in a derived class to have the same name as a method in its base class but with different behavior. This enables methods to be called on objects of different classes through a common interface.

<img src="./img/poly.jpg">

- **Types:**
  1. **Compile-Time Polymorphism (Method Overloading):** Occurs when multiple methods in the same class have the same name but different parameters.
  2. **Run-Time Polymorphism (Method Overriding):** Occurs when a method in a derived class has the same signature as a method in its base class, and the derived class provides its own implementation of that method.

- **Example (Method Overriding):**
  ```csharp
  class Animal
  {
      public virtual void MakeSound()
      {
          Console.WriteLine("Animal makes a sound.");
      }
  }
  
  class Dog : Animal
  {
      public override void MakeSound()
      {
          Console.WriteLine("Dog barks.");
      }
  }
  ```

### Interfaces

Interfaces in C# provide a way to define a contract that classes can implement. They allow for polymorphic behavior and facilitate loose coupling between components.

<img src="./img/interface.png">

- **Syntax:**
  To define an interface in C#, you use the interface keyword followed by the interface name and a set of member declarations enclosed in curly braces {}. Each member declaration includes the member's signature (method name, property name, event name, or indexer) and its return type (for methods and properties) or other relevant modifiers.

  ```csharp
  interface InterfaceName
    {
        // Member declarations
        ReturnType MethodName(ParameterList);
        ReturnType PropertyName { get; set; }
        // Event declaration
        event EventHandler EventName;
        // Indexer declaration
        ReturnType this[int index] { get; set; }
    }
  ```

- **Implementation:**
  Classes that implement an interface must provide concrete implementations for all of its members.

  ```csharp
  using System;
    // Define an interface
    public interface IShape
    {
        // Interface members (methods and properties)
        double CalculateArea();
        double CalculatePerimeter();
    }

    // Implement the interface in a class
    public class Rectangle : IShape
    {
        // Implement interface members
        public double Width { get; set; }
        public double Height { get; set; }

        public double CalculateArea()
        {
            return Width * Height;
        }

        public double CalculatePerimeter()
        {
            return 2 * (Width + Height);
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            // Create an instance of the Rectangle class
            Rectangle rectangle = new Rectangle { Width = 5, Height = 3 };

            // Use interface methods through the instance
            Console.WriteLine("Area of Rectangle: " + rectangle.CalculateArea());
            Console.WriteLine("Perimeter of Rectangle: " + rectangle.CalculatePerimeter());
        }
    }
  ```

Interfaces serve as powerful tools in C# development, enhancing both **testability and extensibility of software systems**. They promote ***abstraction***, ***enabling dependency injection*** and ***facilitating unit testing*** through isolation and mocking, thus contributing to the robustness and maintainability of applications.

Additionally, interfaces foster modularity, flexibility, and interchangeability, allowing for seamless integration of new functionality without modifying existing code. This promotes ***the development of maintainable*** and ***scalable applications*** that can easily adapt to changing requirements.


<img src="./img/Interface-relationships.webp">

#### Interfaces vs Testability
Interfaces play a significant role in enhancing testability in C# codebases. They facilitate unit testing, mocking, and dependency injection, leading to more maintainable and testable code.

**Benefits of Interfaces for Testability:**
- **Isolation**: Interfaces allow components to be isolated and tested independently of their concrete implementations.
- **Flexibility**: Interfaces enable the substitution of real dependencies with mock implementations during testing, allowing for more thorough and flexible testing scenarios.
- **Maintainability**: By promoting loose coupling and dependency inversion, interfaces contribute to cleaner and more maintainable code, making it easier to write and maintain unit tests.
  
#### Interfaces vs Extensibility
Interfaces contribute to the extensibility of software systems by promoting loose coupling and separation of concerns. They allow for the addition of new functionality without modifying existing code, facilitating the development of modular and maintainable applications.

**Benefits of Interfaces for Extensibility:**
- **Modularity**: Interfaces promote modular design by defining contracts for behavior, allowing components to be added or replaced independently.
- **Flexibility**: Interfaces enable the integration of new functionality without modifying existing code, providing flexibility to adapt to changing requirements.
- **Interchangeability**: Components can interact with each other through interfaces, enabling interchangeable implementations and promoting code reuse.
  
### Abstraction
Abstraction refers to the ability to focus on the essential aspects of an object while hiding the non-essential or irrelevant details. Simply put, it reduces complexity for the average user. It is mainly used to solve problems at the design level, mainly the conceptual part.

<img src="">

- **Benefits:**
  1. **Simplicity and Manageability:** Abstraction allows complex systems to be simplified by focusing on essential features, making it easier to understand and manage the codebase.
  2. **Encapsulation of Complexity:** By hiding implementation details, abstraction encapsulates the complexity of objects, reducing cognitive load and promoting modular design.
  3. **Enhanced Reusability:** Abstraction promotes reusable code components by creating generalized interfaces that can be applied across different contexts, saving time and effort in development.
- **Example:**
  ```csharp
    class Book
    {
        public string Title { get; set; }
        public string Author { get; set; }
        public int PublicationYear { get; set; }
        
        public void DisplayDetails()
        {
            Console.WriteLine($"Title: {Title}, Author: {Author}, Publication Year: {PublicationYear}");
        }
    }

    class Member
    {
        public string Name { get; set; }
        public int Age { get; set; }
        public string Email { get; set; }
        
        public void DisplayInformation()
        {
            Console.WriteLine($"Name: {Name}, Age: {Age}, Email: {Email}");
        }
    }

    class Library
    {
        private List<Book> borrowedBooks = new List<Book>();
        private List<Member> registeredMembers = new List<Member>();
        
        // Methods for borrowing books, registering members, etc.
    }
  ```

### Encapsulation

Encapsulation is the process of wrapping of data (fields or properties) and methods (functions or procedures) that operate on the data into a single unit, typically a class. It hides the internal state of an object and only exposes the necessary functionality through well-defined interfaces. Encapsulation helps in achieving data abstraction, information hiding, and modular programming.

<img src="./img/enca.jpeg">

- **Benefits:**
  1. **Data Hiding:** Encapsulation allows the internal state of an object to be hidden from outside interference, preventing unauthorized access and modification.
  2. **Abstraction:** It presents a simplified view of an object by exposing only essential features while hiding the implementation details.
  3. **Modularity:** Encapsulation promotes modularity by organizing code into self-contained units, making it easier to manage, maintain, and reuse.

- **Example:**
  ```csharp
  class BankAccount
  {
      private decimal balance;
  
      public void Deposit(decimal amount)
      {
          balance += amount;
      }
  
      public void Withdraw(decimal amount)
      {
          if (amount <= balance)
              balance -= amount;
          else
              Console.WriteLine("Insufficient funds.");
      }
  
      public decimal GetBalance()
      {
          return balance;
      }
  }
  ```

### Methods
In object-oriented programming, a class acts as a blueprint or template for creating objects. Central to this blueprint are the methods the actionable components that define the behavior of the objects created from the class.

Methods encapsulate functionality within a class, representing the actions or behaviors that objects of that class can perform. Each method typically performs a specific task or set of tasks, enabling objects to interact with each other and manipulate data.

**Characteristics:**

- **Name and Signature:** Each method has a unique name and signature, consisting of the method's name and its parameters, if any. This signature differentiates one method from another within the same class.
    ```c#
    public class MyClass
        {
            // Method with name 'MyMethod' and no parameters
            public void MyMethod()
            {
                // Method implementation
            }
            
            // Method with name 'Add' and two parameters of type int
            public int Add(int a, int b)
            {
                // Method implementation
                return a + b;
            }
        }
    ```
  
- **Return Type:** Methods may return a value after performing their tasks, indicated by a return type such as int, string, or void if no value is returned.
  ```c#
    public class MyClass
        {
            // Method with return type int
            public int Multiply(int a, int b)
            {
                // Method implementation
                return a * b;
            }
            
            // Method with no return type (void)
            public void DisplayMessage(string message)
            {
                // Method implementation
                Console.WriteLine(message);
            }
        }
  ```
  
- **Parameters:** Methods may accept input parameters, enabling them to receive data necessary for their operation.
  ```c#
    public class MyClass
        {
            // Method with parameters
            public int Subtract(int a, int b)
            {
                // Method implementation
                return a - b;
            }
            
            // Method with no parameters
            public void Greet(string name)
            {
                // Method implementation
                Console.WriteLine($"Hello, {name}!");
            }
        }
  
  ```



### Access Modifiers

In C#, various elements such as **methods, variables, constructors, and sometimes even classes**, come equipped with access modifiers. These modifiers, including `public`, `private`, `protected`, and `readonly`, dictate the visibility and accessibility of these elements from other classes. By employing access modifiers, developers can precisely control how their code interacts with other parts of the program, enhancing encapsulation and facilitating robust software design.

#### Public Modifier
The public access modifier makes a member accessible from any other class. It has the widest scope among all access modifiers and allows the member to be accessed from outside the defining class, including from other assemblies.
```c#
  // Public class accessible from anywhere
  public class MyClass
    {
        // Public field accessible from anywhere
        public string MyPublicField;

        // Constructor with public access
        public MyClass(int value)
        {
            MyPublicField = "value";
        }

        // Public method accessible from anywhere
        public void MyPublicMethod()
        {
            // Method implementation
        }
    }
```

#### Private Modifier
The private access modifier restricts access to the member to within the same class or struct. It is the most restrictive access level and is typically used to hide implementation details.
```c#
    public class MyClass
    {
        // Private field accessible only within the class
        private int myPrivateField;
        // Private method accessible only within the class
        private void MyPrivateMethod()
        {
            // Method implementation
        }
    }
```
#### Protected Modifier
The protected access modifier allows access to the member within the same class or by derived classes. It is commonly used to encapsulate implementation details and provide access to derived classes for overriding or extending functionality.
```c#
    public class MyClass
    {
        // Protected field accessible within the class and derived classes
        protected int protectedField;
    }

    public class MyDerivedClass : MyClass
    {
        // Protected method accessible within the class and derived classes
        protected void AccessProtectedField()
        {
            protectedField = 10; // Accessing protected field from the base class
        }
    }
```
#### Internal Modifier
The internal access modifier limits access to the member to within the same assembly. Members marked as internal can be accessed from any class in the same assembly but not from classes in external assemblies.
```c#
    // Internal class accessible within the same assembly
    internal class MyInternalClass
    {
        // Internal field accessible within the same assembly
        internal int internalField;
        // Internal method accessible within the same assembly
        internal void InternalMethod()
        {
            // Method implementation
        }
    }
```
#### Internal Protected Modifier
The protected internal access modifier combines the behavior of both protected and internal. It allows access to the member within the same assembly and by derived classes, regardless of the assembly in which they reside.
```c#
    public class MyClass
    {
        // Protected internal field accessible within the same assembly and by derived classes
        protected internal int protectedInternalField;
    }

    internal class MyDerivedClass : MyClass
    {
        // Protected internal method accessible within the same assembly and by derived classes
        protected internal void AccessProtectedInternalField()
        {
            protectedInternalField = 20; // Accessing protected internal field
        }
    }
```

#### Readonly Modifier
The readonly modifier can be applied to fields and indicates that the field's value can only be assigned once, either when it's declared or in a constructor. Once initialized, the value of a readonly field cannot be changed.
```c#
    public class MyClass
    {
        // Readonly field can only be assigned once, either when declared or in constructor
        public readonly int ReadonlyField;

        public MyClass(int value)
        {
            ReadonlyField = value; // Assigning value in constructor
        }

        // Readonly method cannot be overridden
        public readonly void ReadonlyMethod()
        {
            Console.WriteLine("Readonly method called.");
        }
    }
```

### Upcasting and Downcasting

Upcasting and downcasting are essential concepts in object-oriented programming, particularly in languages like C#. They involve converting between different types in the class hierarchy, such as base classes and derived classes.

#### Upcasting
- **Definition**: Upcasting involves converting a reference of a derived class to a reference of its base class.
- **Example**: Suppose we have a base class Shape and a derived class Circle. Upcasting allows us to treat a Circle object as a Shape object.
- **Syntax**: Upcasting is implicit and doesn't require explicit syntax. It happens automatically when assigning a derived class object to a base class reference.

```csharp
Circle circle = new Circle();
Shape shape = circle; // Upcasting
```
- **Use cases**: Upcasting is useful when you want to work with objects at a higher level of abstraction, treating derived class objects as instances of their base class.
  
#### Downcasting
- **Definition**: Downcasting involves converting a reference of a base class to a reference of its derived class.
- **Example**: Continuing from the previous example, downcasting allows us to treat a Shape object as a Circle object if we're certain it's actually a circle.
- **Syntax**: Downcasting requires explicit casting using the type of the derived class in parentheses.
  
```csharp
Shape shape = new Circle();
Circle circle = (Circle)shape; // Downcasting
```
- **Use cases**: Downcasting is useful when you need to access specific members or behaviors of a derived class that are not available in the base class.

## 3. System.IO in C#

In C#, the `System.IO` namespace provides classes for performing various I/O operations, including reading from and writing to files, working with directories, and more. Here are some commonly used classes and methods:

### File Operations

File operations involve interacting with files, including checking for existence, deleting, copying, moving, and opening files.

- **File.Exists(string path):** Checks if a file exists at the specified path.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string filePath = "example.txt"; // Path to the file

        // Check if the file exists
        if (File.Exists(filePath))
        {
            Console.WriteLine("File exists.");
        }
        else
        {
            Console.WriteLine("File does not exist.");
        }
    }
}
```

- **File.Delete(string path):** Deletes the specified file.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string filePath = "example.txt"; // Path to the file to delete

        // Check if the file exists before deleting
        if (File.Exists(filePath))
        {
            // Delete the specified file
            File.Delete(filePath);
            Console.WriteLine("File deleted successfully.");
        }
        else
        {
            Console.WriteLine("File does not exist.");
        }
    }
}
```

- **File.Copy(string sourceFileName, string destFileName):** Copies a file from one location to another.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string sourceFile = "source.txt";
        string destFile = "destination.txt";

        File.Copy(sourceFile, destFile);

        Console.WriteLine("File copied successfully.");
    }
}
```

- **File.Move(string sourceFileName, string destFileName):** Moves a file from one location to another.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string sourceFile = "source.txt"; // Path to the source file
        string destFile = "destination.txt"; // Path to the destination file

        // Move the file from source to destination
        File.Move(sourceFile, destFile);

        Console.WriteLine("File moved successfully.");
    }
}
```

- **File.Open(string path, FileMode mode):** Opens a file in the specified mode (read, write, etc.).
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string filePath = "example.txt"; // Path to the file

        try
        {
            // Open the file in read mode
            using (FileStream fs = File.Open(filePath, FileMode.Open))
            {
                Console.WriteLine("File opened successfully.");
                // Perform operations on the file
            }
        }
        catch (IOException e)
        {
            Console.WriteLine("Error opening the file: " + e.Message);
        }
    }
}
```

### Directory Operations

Directory operations entail tasks related to directories, such as retrieving directory contents, creating, deleting, and moving directories.

- **Directory.GetDirectories(string path):** Retrieves an array of directory names from the specified path.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string directoryPath = @"C:\Users"; // Path to the directory

        try
        {
            // Retrieve an array of directory names from the specified path
            string[] directories = Directory.GetDirectories(directoryPath);

            // Display each directory name
            foreach (string directory in directories)
            {
                Console.WriteLine(directory);
            }
        }
        catch (IOException e)
        {
            Console.WriteLine("Error accessing directories: " + e.Message);
        }
    }
}

```
- **Directory.GetFiles(string path):** Retrieves an array of file names from the specified path.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string directoryPath = @"C:\Users"; // Path to the directory

        try
        {
            // Retrieve an array of file names from the specified path
            string[] files = Directory.GetFiles(directoryPath);

            // Display each file name
            foreach (string file in files)
            {
                Console.WriteLine(file);
            }
        }
        catch (IOException e)
        {
            Console.WriteLine("Error accessing files: " + e.Message);
        }
    }
}
```
- **Directory.CreateDirectory(string path):** Creates a new directory at the specified path.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string directoryPath = @"C:\Temp\NewDirectory"; // Path to the new directory

        try
        {
            // Create a new directory at the specified path
            Directory.CreateDirectory(directoryPath);

            Console.WriteLine("Directory created successfully.");
        }
        catch (IOException e)
        {
            Console.WriteLine("Error creating directory: " + e.Message);
        }
    }
}
```
- **Directory.Delete(string path):** Deletes the specified directory.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string directoryPath = @"C:\Temp\ToDelete"; // Path to the directory to delete

        try
        {
            // Delete the specified directory
            Directory.Delete(directoryPath);

            Console.WriteLine("Directory deleted successfully.");
        }
        catch (IOException e)
        {
            Console.WriteLine("Error deleting directory: " + e.Message);
        }
    }
}
```
- **Directory.Move(string sourceDirName, string destDirName):** Moves a directory from one location to another.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string sourceDir = @"C:\Temp\ToMove"; // Source directory
        string destDir = @"C:\Temp\Moved"; // Destination directory

        try
        {
            // Move the directory from source to destination
            Directory.Move(sourceDir, destDir);

            Console.WriteLine("Directory moved successfully.");
        }
        catch (IOException e)
        {
            Console.WriteLine("Error moving directory: " + e.Message);
        }
    }
}
```

### Path Operations

Path operations involve working with file and directory paths, including combining paths and extracting path components.

- **Path.Combine(params string[] paths):** Combines strings into a path.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string basePath = @"C:\";
        string fileName = "example.txt";

        // Combine strings into a path
        string fullPath = Path.Combine(basePath, fileName);

        Console.WriteLine("Full Path: " + fullPath);
    }
}
```
- **Path.GetExtension(string path):** Retrieves the extension of the specified path.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string filePath = @"C:\Temp\example.txt";

        // Retrieve the extension of the specified path
        string extension = Path.GetExtension(filePath);

        Console.WriteLine("File Extension: " + extension);
    }
}
```
- **Path.GetFileName(string path):** Retrieves the file name and extension from the specified path.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string filePath = @"C:\Temp\example.txt";

        // Retrieve the file name and extension from the specified path
        string fileName = Path.GetFileName(filePath);

        Console.WriteLine("File Name: " + fileName);
    }
}
```
- **Path.GetDirectoryName(string path):** Retrieves the directory name from the specified path.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string filePath = @"C:\Temp\example.txt";

        // Retrieve the directory name from the specified path
        string directoryName = Path.GetDirectoryName(filePath);

        Console.WriteLine("Directory Name: " + directoryName);
    }
}
```

### Stream-based Operations

Stream-based operations utilize stream classes for reading from and writing to files.

- **StreamReader:** Reads characters from a stream.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string filePath = "example.txt"; // Path to the file to read

        try
        {
            // Open the file for reading using StreamReader
            using (StreamReader sr = new StreamReader(filePath))
            {
                // Read and display lines from the file until the end
                string line;
                while ((line = sr.ReadLine()) != null)
                {
                    Console.WriteLine(line); // Output each line to the console
                }
            }
        }
        catch (IOException e)
        {
            Console.WriteLine("Error reading the file: " + e.Message);
        }
    }
}
```
- **StreamWriter:** Writes characters to a stream.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string filePath = "example.txt"; // Path to the file to write

        try
        {
            // Open the file for writing using StreamWriter
            using (StreamWriter sw = new StreamWriter(filePath))
            {
                // Write some text to the file
                sw.WriteLine("Hello, world!"); // Write a line of text to the file
            }

            Console.WriteLine("Text written to the file successfully.");
        }
        catch (IOException e)
        {
            Console.WriteLine("Error writing to the file: " + e.Message);
        }
    }
}
```
- **FileStream:** Provides a stream for a file.
```c#
using System;
using System.IO;

class Program
{
    static void Main()
    {
        string filePath = "example.txt"; // Path to the file

        try
        {
            // Open the file for reading and writing using FileStream
            using (FileStream fs = new FileStream(filePath, FileMode.OpenOrCreate, FileAccess.ReadWrite))
            {
                // Perform operations on the file stream
                // For example, you can read or write bytes directly to the stream
                byte[] buffer = new byte[1024]; // Buffer to hold data read from the file
                int bytesRead = fs.Read(buffer, 0, buffer.Length); // Read bytes from the file
                // Process the bytes read, if needed
                // Similarly, you can write data to the file using fs.Write()
            }

            Console.WriteLine("File stream operation completed successfully.");
        }
        catch (IOException e)
        {
            Console.WriteLine("Error working with file stream: " + e.Message);
        }
    }
}
```

## Other Functionalities

### DateTime and TimeSpan
DateTime is a struct in C# that represents a specific point in time, including both date and time components. It's commonly used for tasks involving date and time calculations, such as scheduling, time tracking, and event handling. TimeSpan, also a struct, represents a duration of time, such as a number of days, hours, minutes, etc.
```c#
using System;

class Program
{
    static void Main()
    {
        // DateTime methods and properties

        DateTime now = DateTime.Now; // Get current date and time
        DateTime futureDate = DateTime.Now.AddHours(1); // Add 1 hour to current time
        DateTime pastDate = DateTime.Now.Subtract(TimeSpan.FromDays(7)); // Subtract 7 days from current date
        string dateString = DateTime.Now.ToString("yyyy-MM-dd HH:mm:ss"); // Format current date and time as string
        int comparisonResult = DateTime.Now.CompareTo(futureDate); // Compare current date and future date

        // DateTime properties

        DateTime currentDate = DateTime.Now.Date; // Get current date without time component
        DayOfWeek day = DateTime.Now.DayOfWeek; // Get current day of the week
        int dayOfYear = DateTime.Now.DayOfYear; // Get current day of the year
        long ticks = DateTime.Now.Ticks; // Get ticks representing current date and time

        // TimeSpan methods and properties

        TimeSpan futureTime = TimeSpan.FromHours(1).Add(TimeSpan.FromMinutes(30)); // Add 1 hour and 30 minutes to TimeSpan
        TimeSpan remainingTime = TimeSpan.FromHours(3).Subtract(TimeSpan.FromMinutes(45)); // Subtract 45 minutes from 3 hours
        TimeSpan positiveTime = TimeSpan.FromMinutes(-15).Duration; // Get absolute value of TimeSpan
        int days = TimeSpan.FromDays(5).Days; // Get days component of TimeSpan
        int hours = TimeSpan.FromHours(2).Hours; // Get hours component of TimeSpan
        int minutes = TimeSpan.FromMinutes(30).Minutes; // Get minutes component of TimeSpan
        int seconds = TimeSpan.FromSeconds(45).Seconds; // Get seconds component of TimeSpan

        // Output results

        Console.WriteLine("Current Date and Time: " + now);
        Console.WriteLine("Future Date: " + futureDate);
        Console.WriteLine("Past Date: " + pastDate);
        Console.WriteLine("Formatted Date String: " + dateString);
        Console.WriteLine("Comparison Result: " + comparisonResult);

        Console.WriteLine("Current Date: " + currentDate);
        Console.WriteLine("Day of the Week: " + day);
        Console.WriteLine("Day of the Year: " + dayOfYear);
        Console.WriteLine("Ticks: " + ticks);

        Console.WriteLine("Future Time: " + futureTime);
        Console.WriteLine("Remaining Time: " + remainingTime);
        Console.WriteLine("Positive Time: " + positiveTime);
        Console.WriteLine("Days: " + days);
        Console.WriteLine("Hours: " + hours);
        Console.WriteLine("Minutes: " + minutes);
        Console.WriteLine("Seconds: " + seconds);
    }
}
```
### StringBuilder
StringBuilder is a class in C# that provides an efficient way to manipulate strings, especially when dealing with multiple string concatenations. Unlike the String class, which creates a new string object each time you modify it, StringBuilder allows you to modify a single string buffer without creating new objects, leading to better performance, especially for large strings or many concatenations.
```c#
using System;
using System.Text;

class Program
{
    static void Main()
    {
        // StringBuilder methods and properties
        StringBuilder sb = new StringBuilder(); // Create a new StringBuilder instance

        sb.Append("Hello"); // Append "Hello" to the StringBuilder
        sb.Append(" "); // Append a space
        sb.Append("World"); // Append "World"

        string result = sb.ToString(); // Convert StringBuilder to string

        // Output result
        Console.WriteLine("Result: " + result);
    }
}
```
### StopWatch
The Stopwatch class in C# provides a high-resolution timer that can measure elapsed time with precision. It's particularly useful for performance analysis, benchmarking, and profiling code execution times.

- **Creating a Stopwatch**:
  * **Namespace**: The Stopwatch class is available in the System.Diagnostics namespace.
    ```csharp
    using System.Diagnostics;
    ```
  * **Initialization**: To use Stopwatch, create an instance of the class using the new keyword.
    ```csharp
    Stopwatch stopwatch = new Stopwatch();
    ```
  * **Basic Operations**: Starting and Stopping: Use the Start() and Stop() methods to control the stopwatch.
    ```csharp
    stopwatch.Start(); // Start the stopwatch
    // Code to measure
    stopwatch.Stop(); // Stop the stopwatch
    ```
  * **Resetting**: Use the Reset() method to reset the stopwatch to zero.
    ```csharp
    stopwatch.Reset();
    ```
  * **Elapsed Time**: Retrieve the elapsed time using the Elapsed property, which returns a TimeSpan representing the elapsed time.
    ```csharp
    TimeSpan elapsed = stopwatch.Elapsed;
    ```
- **Advanced Operations**:
  * **Restarting**: Use the Restart() method to stop and reset the stopwatch in a single operation.
    ```csharp
    stopwatch.Restart();
    ```
  * **Reading Elapsed Time**: Retrieve the elapsed time in different units such as milliseconds, microseconds, or ticks using properties like ElapsedMilliseconds, ElapsedMicroseconds, or ElapsedTicks.
    ```csharp
    long elapsedMilliseconds = stopwatch.ElapsedMilliseconds;
    ```
  * **High Resolution**: The Stopwatch class provides high-resolution timing by utilizing the underlying system timer with precision down to the nanosecond level.

- **Example Usage**:
```csharp
    using System;
    using System.Diagnostics;

    class Program
    {
        static void Main(string[] args)
        {
            Stopwatch stopwatch = new Stopwatch();

            // Start measuring time
            stopwatch.Start();

            // Perform some operation to measure
            for (int i = 0; i < 1000000; i++)
            {
                // Some computational task
            }

            // Stop measuring time
            stopwatch.Stop();

            // Get elapsed time
            TimeSpan elapsed = stopwatch.Elapsed;
            Console.WriteLine("Elapsed Time: " + elapsed.TotalMilliseconds + " milliseconds");
        }
    }
```

## Summary and conclusions

This documentation provides a condensed overview of fundamental C# concepts for beginners. It covers primitive types, variables, operators, control flow structures, loops, type conversions, non-primitive types, input/output operations, and handling dates and times. By understanding these concepts, beginners gain a solid understanding of C# programming essentials, enabling them to write basic programs and build a foundation for further learning and exploration in the languag