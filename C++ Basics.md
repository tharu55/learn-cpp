# 📘 C++ Basics

Before writing C++ programs, it is important to understand the basic building blocks of the language. These include **functions, keywords, data types, operators,** and **header files**. Together, they help us write efficient and organized programs.

---

# 📖 What is a Function?

A **function** is a block of code that performs a specific task. Functions help organize a program into smaller, reusable parts, making the code easier to write, understand, test, and maintain.

Every C++ program must contain a `main()` function because it is the starting point of program execution.

### Why Do We Use Functions?

- Reuse code without writing it multiple times.
- Improve code readability.
- Make programs easier to debug and maintain.
- Break large problems into smaller tasks.
- Improve program organization.

---

# 📖 What are Keywords?

**Keywords** are reserved words in C++ that have predefined meanings. They are part of the language syntax and cannot be used as variable or function names.

**Examples:** `int`, `return`, `if`, `else`, `while`, `for`, `class`

---

## Common C++ Functions & Keywords

| Function / Keyword | Description | Example / Usage |
|--------------------|-------------|-----------------|
| `main()` | Entry point of every C++ program. | Program execution begins here. |
| `cout` | Displays output on the console. | `cout << "Hello";` |
| `cin` | Accepts input from the user. | `cin >> number;` |
| `endl` | Moves the cursor to the next line. | `cout << endl;` |
| `return` | Exits a function and optionally returns a value. | `return 0;` |
| `#include <iostream>` | Includes the input/output library. | Required for `cin` and `cout`. |
| `using namespace std;` | Allows the use of standard library names without `std::`. | `using namespace std;` |

---

# 📖 What are Data Types?

**Data types** define the type of data a variable can store. Choosing the correct data type helps the compiler allocate memory efficiently and perform operations correctly.

## Common Data Types

| Data Type | Description | Example |
|-----------|-------------|---------|
| `int` | Stores whole numbers. | `int age = 20;` |
| `float` | Stores decimal numbers. | `float pi = 3.14;` |
| `double` | Stores larger decimal values with higher precision. | `double salary = 50000.75;` |
| `char` | Stores a single character. | `char grade = 'A';` |
| `string` | Stores text. | `string name = "Tharun";` |
| `bool` | Stores `true` or `false`. | `bool isPassed = true;` |

---

# 📖 What are Operators?

**Operators** are symbols that perform operations on variables and values, such as arithmetic calculations, comparisons, and assignments.

## Common Operators

| Operator | Purpose | Example |
|----------|---------|---------|
| `+` | Addition | `a + b` |
| `-` | Subtraction | `a - b` |
| `*` | Multiplication | `a * b` |
| `/` | Division | `a / b` |
| `%` | Modulus (Remainder) | `a % b` |
| `=` | Assignment | `x = 10;` |
| `==` | Equal to | `a == b` |
| `!=` | Not equal to | `a != b` |
| `>` | Greater than | `a > b` |
| `<` | Less than | `a < b` |

---

# 📖 What are Header Files?

**Header files** contain declarations of predefined functions, classes, and libraries. They allow us to use built-in features in our C++ programs by including them with the `#include` directive.

## Common Header Files

| Header File | Purpose |
|-------------|---------|
| `<iostream>` | Input and output operations |
| `<string>` | String manipulation |
| `<cmath>` | Mathematical functions |
| `<iomanip>` | Output formatting |
| `<fstream>` | File handling |

> **Note:** As I continue learning C++, I will update this section with new functions, keywords, libraries, and concepts.

# 💻 Example Programs

---

## 1. Hello World Program

### Program

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!";
    return 0;
}
```

### Output

```
Hello, World!
```

### Explanation

- `#include <iostream>` includes the input/output library.
- `using namespace std;` allows us to use `cout` without `std::`.
- `main()` is the starting point of the program.
- `cout` displays text on the screen.
- `return 0;` ends the program successfully.

---

## 2. Input and Output Program

### Program

```cpp
#include <iostream>
using namespace std;

int main() {
    string name;

    cout << "Enter your name: ";
    cin >> name;

    cout << "Hello, " << name;

    return 0;
}
```

### Sample Output

```
Enter your name: Tharun
Hello, Tharun
```

### Concepts Used

- `cin`
- `cout`
- `string`
- `main()`
- `return`

---

## 3. Program Using Different Data Types

### Program

```cpp
#include <iostream>
using namespace std;

int main() {
    int age = 20;
    float height = 5.8;
    char grade = 'A';
    bool passed = true;

    cout << "Age: " << age << endl;
    cout << "Height: " << height << endl;
    cout << "Grade: " << grade << endl;
    cout << "Passed: " << passed << endl;

    return 0;
}
```

### Output

```
Age: 20
Height: 5.8
Grade: A
Passed: 1
```

### Concepts Used

- Data Types
- Variables
- `cout`
- `endl`

---

## 4. Arithmetic Operators

### Program

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int b = 5;

    cout << "Addition: " << a + b << endl;
    cout << "Subtraction: " << a - b << endl;
    cout << "Multiplication: " << a * b << endl;
    cout << "Division: " << a / b << endl;
    cout << "Remainder: " << a % b << endl;

    return 0;
}
```

### Output

```
Addition: 15
Subtraction: 5
Multiplication: 50
Division: 2
Remainder: 0
```

---

## 5. Simple Function Example (`main()`)

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Welcome to C++!";
    return 0;
}
```

### Output
```
Welcome to C++!
```

---

