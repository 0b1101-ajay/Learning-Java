- The name of the java file must match the class name
- A class should always start with an uppercase first letter
- The main() method is required and every program must contain the **main() method**          
- To run the file navigate to the directory where you have saved your file, and type **"javac *filename*.java"**: i.e "javac Main.java"
- This will compile your code. If there are no errors in the code, the command prompt will take you to the next line. Now, type "java *filename*" to run the file: i.e "java Main"



## println(): 
- println() method in Java is also used to display a text on the console
- This text is passed as the parameter to this method in the form of String 
- This method prints the text on the console and the **cursor remains at the start of the next line** at the console 
- The next printing takes place from next line
- It **can work without arguments**
- We can also use this method to print numbers. However, unlike text, we don't put numbers inside double quotes
- You can also perform mathematical calculations inside the println() method


## print():
- print() method in Java is used to display a text on the console
- This text is passed as the parameter to this method in the form of String 
- This method prints the text on the console and the **cursor remains at the end of the text** at the console 
- The next printing takes place from just here
- This method **only works with argument**, otherwise it is throws syntax error
- We can also use this method to print numbers. However, unlike text, we don't put numbers inside double quotes
- You can also perform mathematical calculations inside the print() method


## Comments
- Comments can be used to explain Java code, and to make it more readable. It can also be used to prevent execution when testing alternative code
  ### Single-line Comments
    - Single-line comments start with two forward slashes (//).
    - Any text between // and the end of the line is ignored by Java (will not be executed).
  ### Multi-line Comments
    - Multi-line comments start with /* and ends with */.
    - Any text between /* and */ will be ignored by Java.


## Variables
- Variables are containers for storing data values.
- To create a variable, you must specify the type and assign it a value.
    `type variableName = value;`
- You can also declare a variable without assigning the value, and assign the value later.
- If you assign a new value to an existing variable, it will overwrite the previous value:

  ### Final Variables
   - If you don't want others (or yourself) to overwrite existing values, use the final keyword.
   - This will declare the variable as "final" or "constant", which means unchangeable and read-only.
     `final int myNum = 15;
      myNum = 20;              // will generate an error: cannot assign a value to a final variable
      `
**Declare Many Variables**
- To declare more than one variable of the same type, you can use a comma-separated list.
  `int x = 5, y = 6, z = 50;`
  
**One Value to Multiple Variables**
- You can also assign the same value to multiple variables in one line.
`int x, y, z;
x = y = z = 50;`


## The general rules for naming variables are:
- Names can contain letters, digits, underscores, and dollar signs
- Names must begin with a letter
- Names should start with a lowercase letter and it cannot contain whitespace
- Names **can also begin with $ and _** 
- Names are case sensitive ("myVar" and "myvar" are different variables)
- Reserved words (like Java keywords, such as int or boolean) cannot be used as names


## Java Data Types
Data types are divided into two groups:
- **Primitive data types** - includes byte, short, int, long, float, double, boolean and char
- **Non-primitive data types** - such as String, Arrays and Classes


Numbers
Primitive number types are divided into two groups:
- Integer types stores whole numbers, positive or negative (such as 123 or -456), without decimals. Valid types are byte, short, int and long. Which type you should
  use, depends on the numeric value.
- Floating point types represents numbers with a fractional part, containing one or more decimals. There are two types: float and double.


Integer Types
Byte
The byte data type can store whole numbers from -128 to 127. This can be used instead of int or other integer types to save memory when you are certain that the value will be within -128 and 127:

Short
The short data type can store whole numbers from -32768 to 32767:

Int
The int data type can store whole numbers from -2147483648 to 2147483647. In general, and in our tutorial, the int data type is the preferred data type when we create variables with a numeric value.

Long
The long data type can store whole numbers from -9223372036854775808 to 9223372036854775807. This is used when int is not large enough to store the value. Note that you should end the value with an "L":


Floating Point Types
You should use a floating point type whenever you need a number with a decimal, such as 9.99 or 3.14515.

The float and double data types can store fractional numbers. Note that you should end the value with an "f" for floats and "d" for doubles:



Use float or double?

The precision of a floating point value indicates how many digits the value can have after the decimal point. The precision of float is only six or seven decimal digits, while double variables have a precision of about 15 digits. Therefore it is safer to use double for most calculations.


Scientific Numbers
A floating point number can also be a scientific number with an "e" to indicate the power of 10:

Example
float f1 = 35e3f;
double d1 = 12E4d;


Boolean Types
Very often in programming, you will need a data type that can only have one of two values, like:

YES / NO
ON / OFF
TRUE / FALSE
For this, Java has a boolean data type, which can only take the values true or false:

Example
boolean isJavaFun = true;
boolean isFishTasty = false;


Characters
The char data type is used to store a single character. The character must be surrounded by single quotes, like 'A' or 'c':

Example
char myGrade = 'B';

Alternatively, if you are familiar with ASCII values, you can use those to display certain characters:

Example
char myVar1 = 65, myVar2 = 66, myVar3 = 67;
System.out.println(myVar1);
System.out.println(myVar2);


Strings
The String data type is used to store a sequence of characters (text). String values must be surrounded by double quotes:

Example
String greeting = "Hello World";

A String in Java is actually a non-primitive data type, because it refers to an object. The String object has methods that are used to perform certain operations on strings.

Non-Primitive Data Types
Non-primitive data types are called reference types because they refer to objects.

The main difference between primitive and non-primitive data types are:

Primitive types are predefined (already defined) in Java. Non-primitive types are created by the programmer and is not defined by Java (except for String).
Non-primitive types can be used to call methods to perform certain operations, while primitive types cannot.
A primitive type has always a value, while non-primitive types can be null.
A primitive type starts with a lowercase letter, while non-primitive types starts with an uppercase letter.
The size of a primitive type depends on the data type, while non-primitive types have all the same size.
Examples of non-primitive types are Strings, Arrays, Classes, Interface, etc.


Java Type Casting
Type casting is when you assign a value of one primitive data type to another type.

In Java, there are two types of casting:

Widening Casting (automatically) - converting a smaller type to a larger type size
byte -> short -> char -> int -> long -> float -> double

Narrowing Casting (manually) - converting a larger type to a smaller size type
double -> float -> long -> int -> char -> short -> byte


Widening Casting
Widening casting is done automatically when passing a smaller size type to a larger size type:

Example
public class Main {
  public static void main(String[] args) {
    int myInt = 9;
    double myDouble = myInt; // Automatic casting: int to double

    System.out.println(myInt);      // Outputs 9
    System.out.println(myDouble);   // Outputs 9.0
  }
}


Narrowing Casting
Narrowing casting must be done manually by placing the type in parentheses in front of the value:

Example
public class Main {
  public static void main(String[] args) {
    double myDouble = 9.78d;
    int myInt = (int) myDouble; // Manual casting: double to int

    System.out.println(myDouble);   // Outputs 9.78
    System.out.println(myInt);      // Outputs 9
  }
}



Java Operators
Operators are used to perform operations on variables and values.

Java divides the operators into the following groups:

Arithmetic operators
Assignment operators
Comparison operators
Logical operators
Bitwise operators

Operator	Name	Description	Example	Try it
+	Addition	Adds together two values	x + y	
-	Subtraction	Subtracts one value from another	x - y	
*	Multiplication	Multiplies two values	x * y	
/	Division	Divides one value by another	x / y	
%	Modulus	Returns the division remainder	x % y	
++	Increment	Increases the value of a variable by 1	++x	
--	Decrement	Decreases the value of a variable by 1	--x


Java Assignment Operators
Assignment operators are used to assign values to variables.

In the example below, we use the assignment operator (=) to assign the value 10 to a variable called x:

Example
int x = 10;

The addition assignment operator (+=) adds a value to a variable:

Example
int x = 10;
x += 5;

A list of all assignment operators:

Operator	Example	Same As	Try it
=	x = 5	x = 5	
+=	x += 3	x = x + 3	
-=	x -= 3	x = x - 3	
*=	x *= 3	x = x * 3	
/=	x /= 3	x = x / 3	
%=	x %= 3	x = x % 3	
&=	x &= 3	x = x & 3	
|=	x |= 3	x = x | 3	
^=	x ^= 3	x = x ^ 3	
>>=	x >>= 3	x = x >> 3	
<<=	x <<= 3	x = x << 3


Java Comparison Operators
Comparison operators are used to compare two values (or variables). This is important in programming, because it helps us to find answers and make decisions.

The return value of a comparison is either true or false

Operator	Name	Example	Try it
==	Equal to	x == y	
!=	Not equal	x != y	
>	Greater than	x > y	
<	Less than	x < y	
>=	Greater than or equal to	x >= y	
<=	Less than or equal to	x <= y


Java Logical Operators
You can also test for true or false values with logical operators.

Logical operators are used to determine the logic between variables or values:

Operator	Name	Description	Example	Try it
&& 	Logical and	Returns true if both statements are true	x < 5 &&  x < 10	
|| 	Logical or	Returns true if one of the statements is true	x < 5 || x < 4	
!	Logical not	Reverse the result, returns false if the result is true	!(x < 5 && x < 10)	
