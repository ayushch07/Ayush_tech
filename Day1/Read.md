# Variables, Statements, and Expressions: A Learning Task


## 2.1.1. Learning Goals

### Understand the basics of variables, expressions, and statements in Python.

#### Variable-
A variable is a name that refers to a value stored in memory.In python, you don't need to declare a variable before using it; you just assign a value to it.

 python
    x= 10  # x is a variable storing the integer 10
    name = "Ayush"#name is a variable storing the string "Ayush"
    pi = 3.14  # pi stores a floating-point number
 

#### Expression -
An expression is a combination of values, variables, and operators that Python evaluates to produce another value.

python
a = 5
b = 10
c = a + b  # Expression: a + b evaluates to 15
d = (a * b) / 2  # Expression: (5 * 10) / 2 = 25.0



#### Statement -
A statement is a unit of code that performs an action. A statement may or may not produce a value.
python
x = 100  # Assignment statement
print("Hello, World!")  # Print statement
if x > 50:  # Conditional statement
    print("x is greater than 50")


### Differentiate between data types and apply type conversions.
A data type defines the kind of value a variable can hold. Python has several built-in data types:
##### Datatype- 
int,float,char,boolean,string, list, boolean ,set , tuple,custom datatype, Dictionary
##### TypeConversion- 
Type conversion is the process of converting one data type into another.
#### Implicit Type Conversion (Automatic)-
python
a = 5   # int
b = 2.5 # float
c = a + b  # Python converts 'a' to float, so c becomes 7.5 (float)
print(type(c))  # Output: <class 'float'>


#### Explicit Type Conversion (Automatic)-
You can manually convert data types using functions like int(),float(), str(), etc.
python
x = "100"
y = int(x)  # Convert string to int
z = float(y)  # Convert int to float

print(type(x))  # Output: <class 'str'>
print(type(y))  # Output: <class 'int'>
print(type(z))  # Output: <class 'float'>



### Properly name variables following Python conventions-
- Use letters (a-z, A-Z), digits (0-9), and underscores (_) only.

python
valid_name = "Ayush"
age_21 = 21

- Must start with a letter or an underscore (_), but not a digit.

python

_private_variable = "Hidden"
name1 = "John" 
# 1name = "Invalid" ❌ (Starts with a 
### Properly name variables following Python conventions-digit)


- Case-sensitive: name, Name, and NAME are different variables.

python
user = "Alice"
User = "Bob"  # Different from 'user'


- Cannot use Python keywords (reserved words).

python
#  if = 10  ❌ (Invalid, 'if' is a keyword)

- Avoid using -  special characters (!@#$%^&*), starting with a number, using reserved word


###  Grasp the flow of execution through function calls and expressions-
The flow of execution determines the order in which statements and function calls are executed in a Python program.

1. Flow of Execution in Function Calls
How Function Calls Work
- The main script starts executing from the first line.
- When a function is called, execution jumps to the function definition.
- The function executes its statements.
- Once the function completes, execution returns to the point where it was called.

python
def greet(name):  # Function definition
    print("Hello,", name)  # Executes when function is called

print("Start of program")  # Step 1
greet("Ayush")  # Step 2: Function call (execution jumps to function)
print("End of program")  # Step 3: Execution resumes here after function call

2. Flow of Execution in Expressions-

Expressions are evaluated before being used in statements.

Example: 
python
a = 5
b = 10
c = a + b * 2  # Multiplication (*) happens first, then addition (+)
print(c)  # Output: 25

3. Function Call Stack (Nested Calls)

When multiple functions call each other, execution follows a stack (Last-In-First-Out).
python
def multiply(x, y):
    return x * y  # Step 3

def calculate():
    result = multiply(3, 4)  # Step 2: Calls multiply()
    print(result)  # Step 4

calculate()  # Step 1: Calls calculate()

4. Flow Control with Conditional and Loop Statements

Functions and expressions execute sequentially unless modified by conditionals (if-else) or loops (for, while).
python
def countdown(n):
    while n > 0:  # Step 2: Loop executes until n = 0
        print(n)  
        n -= 1  # Step 3: Decreases n

    print("Blast off!")  # Step 4: Executes after loop ends

countdown(3)  # Step 1: Calls countdown()


### Update and reassign variables effectively.
Variables in Python can be updated and reassigned dynamically, allowing for flexible and efficient code.

1. Reassigning Variables:

A variable can be assigned a new value at any point in the program.
python
x = 10  # Initial assignment
print(x)  # Output: 10

x = 20  # Reassignment
print(x)  # Output: 20

2. Updating Variables (Using Current Value):

You can update a variable using its existing value.
python
count = 5
count = count + 1  # Updates count by adding 1
print(count)  # Output: 6

3. Swapping Values Without a Temporary Variable:
Python allows swapping values in a single step.
python
a = 5
b = 10
a, b = b, a  # Swap values
print(a, b)  # Output: 10 5

4. Reassigning with Different Data Types:

Python variables are dynamically typed, meaning they can hold values of different types at different times.
python
x = 10  # Integer
x = "Hello"  # String
x = [1, 2, 3]  # List
print(x)  # Output: [1, 2, 3]

✔ Python allows changing types without restrictions.


## 2.2. Values and Data Types

1. *Research:*
 
 -   What is a value in Python?

A value in Python is a piece of data stored in memory that can be assigned to a variable or used directly in expressions. Values represent data that Python programs manipulate.
Each value in Python has an associated data type, which determines how Python stores and manipulates the value.

2. *Identify different data types in Python (e.g., integers, floats, strings, booleans).:*
    1. Numeric -int,float,
    2. Sequence- string,list,tuple,range
    3. Dictionary- key and value pairs
    4. Boolean- bool
    5. None- when value is not assigned
    6. Set- set,frozenset
    7. Custom Datatype
    8. Binary - bytes, bytearray

 3. *Exercise:*
 python
 # Assigning values to variables
num = 42               # Integer
pi = 3.14             # Float
name = "Ayush"        # String
is_python_fun = True  # Boolean
fruits = ["apple", "banana", "cherry"]  # List
coordinates = (10, 20)  # Tuple
unique_nums = {1, 2, 3}  # Set
student = {"name": "Ayush", "age": 22}  # Dictionary
binary_data = bytes([65, 66, 67])  # Bytes

# Printing the type of each variable
print("Type of num:", type(num))
print("Type of pi:", type(pi))
print("Type of name:", type(name))
print("Type of is_python_fun:", type(is_python_fun))
print("Type of fruits:", type(fruits))
print("Type of coordinates:", type(coordinates))
print("Type of unique_nums:", type(unique_nums))
print("Type of student:", type(student))
print("Type of binary_data:", type(binary_data))



## 2.3. Operators and Operands

 *Research:*
   - Learn about arithmetic, comparison, and logical operators

        In Python, operators are special symbols that perform operations on values (operands). They can be classified into different categories:

1. Arithmetic Operators- +, - , * , / , // , %, **
2. Relational Operators- ==	Equal to,!=	Not equal to,>	Greater than, <	Less than, >=	Greater than or equal to,<=Less than equal to
3. Logical Operators- and, or ,not
4. Bitwise Operators- &(and),`(or),^(xor),~(bitwise not),<<(Left shift),>>(Right shift)
5.  Assignment Operators- ==,+=,*=,-= and many more.
6. Identity Operators- is ,is not
7. Membership Operator- in, not in

 *Exercise :*
  Create a Python script that demonstrates:
     - Addition, subtraction, multiplication, and division.
     - Comparisons between numbers.
     - Logical operations like and, or, not.
python
# Arithmetic Operations
a = 10
b = 5

print("Addition:", a + b)        # 10 + 5 = 15
print("Subtraction:", a - b)     # 10 - 5 = 5
print("Multiplication:", a * b)  # 10 * 5 = 50
print("Division:", a / b)        # 10 / 5 = 2.0

# Comparison Operations
x = 15
y = 20

print("\nIs x equal to y?", x == y)   # False
print("Is x not equal to y?", x != y) # True
print("Is x greater than y?", x > y)  # False
print("Is x less than or equal to y?", x <= y)  # True

# Logical Operations
p = True
q = False

print("\nLogical AND (p and q):", p and q)  # False
print("Logical OR (p or q):", p or q)       # True
print("Logical NOT (not p):", not p)        # False


## 2.4. Function Calls

### 2.4.1. Function Calls as Part of Complex Expressions

1. *Fun Fact:*
   - In Python, functions are first-class objects, meaning they can be assigned to variables and passed as arguments.
2. *Exercise:*
   - Write a program that uses built-in functions inside expressions:
     python
     numbers = [5, 3, 8, 1]
     print(max(numbers) - min(numbers))
     


### 2.4.2. Functions are Objects; Parentheses Invoke Functions

1. *Exercise:*
   - Assign a function to a variable, then call the function using the new variable:
     python
     greet = print
     greet('Hello, World!')
     

In Python, functions are first-class objects, meaning they can be assigned to variables, passed as arguments, and returned from other functions.
##### Explanation:
The print function is assigned to greet.
When calling greet('Hello, World!'), it behaves exactly like print('Hello, World!').

## 2.5. Data Types

1. *Research:*
   - Investigate Python’s dynamic typing.