# 📘 C++ Notes

# Conditional Statements and Loops

---

# 1. Conditional Statements

## Definition

A **conditional statement** is used to make decisions in a program.

It checks whether a condition is **true** or **false**. Based on the result, the program decides which block of code to execute.

**Simple Definition:**

> A conditional statement allows the program to make decisions.

---

## Why do we use Conditional Statements?

We use conditional statements when a program needs to choose between different actions.

### Examples

* Check if a person is eligible to vote.
* Find the largest number.
* Check whether a number is even or odd.
* Display a grade based on marks.

---

# Types of Conditional Statements

1. `if`
2. `if-else`
3. `else if` Ladder
4. Nested `if`
5. `switch`
6. Ternary Operator (`?:`)

---

# 1. if Statement

## Definition

The **if statement** executes a block of code **only if the condition is true**.

If the condition is false, the program skips that block.

### Syntax

```cpp
if(condition)
{
    // code
}
```

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    int age = 20;

    if(age >= 18)
    {
        cout << "You can vote.";
    }

    return 0;
}
```

### Output

```
You can vote.
```

### Explanation

* `age >= 18` is the condition.
* Since age is 20, the condition is true.
* The code inside the `if` block executes.

---

# 2. if-else Statement

## Definition

The **if-else statement** is used when there are **two possible choices**.

* If the condition is true → `if` block executes.
* If the condition is false → `else` block executes.

### Syntax

```cpp
if(condition)
{
    // code if true
}
else
{
    // code if false
}
```

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    int age = 16;

    if(age >= 18)
    {
        cout << "Eligible to vote";
    }
    else
    {
        cout << "Not eligible to vote";
    }

    return 0;
}
```

### Output

```
Not eligible to vote
```

---

# 3. else if Ladder

## Definition

The **else if ladder** is used when there are **more than two conditions**.

The program checks the conditions **from top to bottom**.

As soon as one condition becomes true, its block executes and the remaining conditions are skipped.

### Syntax

```cpp
if(condition1)
{
    // code
}
else if(condition2)
{
    // code
}
else
{
    // code
}
```

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    int marks = 82;

    if(marks >= 90)
    {
        cout << "Grade A";
    }
    else if(marks >= 75)
    {
        cout << "Grade B";
    }
    else if(marks >= 50)
    {
        cout << "Grade C";
    }
    else
    {
        cout << "Fail";
    }

    return 0;
}
```

### Output

```
Grade B
```

---

# 4. Nested if

## Definition

A **Nested if** means writing an `if` statement inside another `if` statement.

It is used when one condition should be checked only after another condition is true.

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    int age = 20;
    bool hasLicense = true;

    if(age >= 18)
    {
        if(hasLicense)
        {
            cout << "You can drive.";
        }
    }

    return 0;
}
```

### Output

```
You can drive.
```

---

# 5. switch Statement

## Definition

A **switch statement** is used when one variable has many fixed values.

It is often simpler than writing many `else if` statements.

### Syntax

```cpp
switch(variable)
{
    case value:
        // code
        break;

    default:
        // code
}
```

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    int day = 3;

    switch(day)
    {
        case 1:
            cout << "Monday";
            break;

        case 2:
            cout << "Tuesday";
            break;

        case 3:
            cout << "Wednesday";
            break;

        default:
            cout << "Invalid Day";
    }

    return 0;
}
```

### Output

```
Wednesday
```

---

# 6. Ternary Operator

## Definition

The **ternary operator** is a short form of the `if-else` statement.

### Syntax

```cpp
(condition) ? true_statement : false_statement;
```

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    int age = 20;

    (age >= 18) ? cout << "Adult" : cout << "Minor";

    return 0;
}
```

### Output

```
Adult
```

---

# What is a Loop?

## Definition

A **loop** is used to execute the same block of code **again and again** until a condition becomes false.

**Simple Definition:**

> A loop repeats a task multiple times.

---

## Why do we use Loops?

Instead of writing the same code many times, we use loops.

### Example

Without a loop:

```cpp
cout << "Hello";
cout << "Hello";
cout << "Hello";
cout << "Hello";
cout << "Hello";
```

With a loop:

```cpp
for(int i = 1; i <= 5; i++)
{
    cout << "Hello\n";
}
```

---
## Important Idea About Loops

A loop is useful when:

* you want to repeat a task,
* you want to print numbers,
* you want to work with arrays,
* you want to run code until a condition changes.

### Real-Life Examples

* Printing attendance numbers from 1 to 50.
* Showing menu options again and again.
* Counting steps in a game.
* Reading many values from the user.

---

## Parts of a Loop

Most loops have three main parts:

1. **Initialization**
   This gives the starting value.

2. **Condition**
   This checks whether the loop should continue.

3. **Update**
   This changes the value after each repetition.

### Example

```cpp
for(int i = 1; i <= 5; i++)
{
    cout << i << " ";
}
```

### Explanation

* `int i = 1` → initialization
* `i <= 5` → condition
* `i++` → update

---

## How a Loop Works

A loop works step by step:

1. The starting value is set.
2. The condition is checked.
3. If the condition is true, the code inside the loop runs.
4. The update part changes the value.
5. The condition is checked again.
6. This continues until the condition becomes false.

---

## Types of Loops

1. `while`
2. `do-while`
3. `for`

---

# 1. while Loop

## Definition

A **while loop** checks the condition first.

If the condition is true, the loop runs.

If the condition is false, the loop stops.

### Syntax

```cpp
while(condition)
{
    // code
}
```

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    int i = 1;

    while(i <= 5)
    {
        cout << i << " ";
        i++;
    }

    return 0;
}
```

### Output

```
1 2 3 4 5
```

### Explanation

* `i` starts from 1.
* The condition `i <= 5` is checked.
* If true, the number is printed.
* `i++` increases the value by 1.
* The loop repeats until `i` becomes 6.

### When to use while Loop?

Use `while` when:

* you do not know the exact number of repetitions,
* the loop should continue until a condition becomes false,
* the condition must be checked before running the code.

### Example Use Case

Keep asking the user for input until they enter the correct password.

---

# 2. do-while Loop

## Definition

A **do-while loop** executes the code **at least one time**, even if the condition is false.

This is because the condition is checked **after** the code runs.

### Syntax

```cpp
do
{
    // code
}
while(condition);
```

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    int i = 1;

    do
    {
        cout << i << " ";
        i++;
    }
    while(i <= 5);

    return 0;
}
```

### Output

```
1 2 3 4 5
```

### Explanation

* First, the code inside `do` runs.
* Then the condition `i <= 5` is checked.
* If the condition is true, the loop repeats.
* If the condition is false, the loop stops.

### Special Point

Even if the condition is false at the beginning, the `do-while` loop runs one time.

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    int i = 10;

    do
    {
        cout << i << " ";
        i++;
    }
    while(i <= 5);

    return 0;
}
```

### Output

```
10
```

### When to use do-while Loop?

Use `do-while` when:

* the code must run at least once,
* you want to show a menu at least one time,
* you want to take input first and check later.

---

# 3. for Loop

## Definition

A **for loop** is used when we already know how many times the loop should run.

It is very useful for counting and repeating a task a fixed number of times.

### Syntax

```cpp
for(initialization; condition; update)
{
    // code
}
```

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    for(int i = 1; i <= 5; i++)
    {
        cout << i << " ";
    }

    return 0;
}
```

### Output

```
1 2 3 4 5
```

### Explanation

* `int i = 1` starts the loop.
* `i <= 5` checks the condition.
* `i++` increases the value after each round.

### When to use for Loop?

Use `for` when:

* the number of repetitions is known,
* you want to print a series of numbers,
* you want to work with arrays,
* you want a compact loop structure.

### Example Use Case

Printing numbers from 1 to 100.

---

# Difference Between while and do-while

| while Loop                                                         | do-while Loop                              |
| ------------------------------------------------------------------ | ------------------------------------------ |
| Checks the condition first.                                        | Executes the code first.                   |
| May execute zero times.                                            | Executes at least one time.                |
| Used when the condition should be checked before running the code. | Used when the code must run at least once. |

---

# Difference Between for and while

| for Loop                                                       | while Loop                                                                        |
| -------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Best when the number of repetitions is known.                  | Best when the number of repetitions is not known.                                 |
| Initialization, condition, and update are written in one line. | Initialization is written before the loop, and update is written inside the loop. |
| More compact and easy for counting.                            | More flexible for condition-based repetition.                                     |

---

# Loop Control Statements

Sometimes we want to change the normal flow of a loop. For this, we use loop control statements.

## 1. break

The `break` statement stops the loop immediately.

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    for(int i = 1; i <= 5; i++)
    {
        if(i == 3)
        {
            break;
        }
        cout << i << " ";
    }

    return 0;
}
```

### Output

```
1 2
```

### Explanation

* When `i` becomes 3, the loop stops.
* The remaining values are not printed.

---

## 2. continue

The `continue` statement skips the current iteration and moves to the next one.

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    for(int i = 1; i <= 5; i++)
    {
        if(i == 3)
        {
            continue;
        }
        cout << i << " ";
    }

    return 0;
}
```

### Output

```
1 2 4 5
```

### Explanation

* When `i` becomes 3, that value is skipped.
* The loop continues with the next number.

---

# Infinite Loop

## Definition

An **infinite loop** is a loop that never stops because its condition always remains true.

### Example

```cpp
while(true)
{
    cout << "Hello";
}
```

### Why is it dangerous?

* It keeps running forever.
* It can make the program hang.
* It uses system resources continuously.

### Common Cause

* Forgetting to update the loop variable.
* Writing a condition that never becomes false.

---

# Nested Loop

## Definition

A **nested loop** means one loop inside another loop.

It is often used for patterns, tables, and grids.

### Example

```cpp
#include <iostream>
using namespace std;

int main() {

    for(int i = 1; i <= 3; i++)
    {
        for(int j = 1; j <= 2; j++)
        {
            cout << i << " " << j << endl;
        }
    }

    return 0;
}
```

### Output

```
1 1
1 2
2 1
2 2
3 1
3 2
```

### Use of Nested Loops

* Printing patterns
* Working with rows and columns
* Printing multiplication tables

---

# Common Mistakes in Loops

1. **Forgetting to update the variable**

   * This can create an infinite loop.

2. **Writing the wrong condition**

   * The loop may stop too early or never stop.

3. **Using ****`=`**** instead of ****`==`**

   * `=` is for assignment.
   * `==` is for comparison.

4. **Wrong placement of semicolon**

   * A small mistake can change the loop behavior.

---

# Key Points to Remember

* `if` checks one condition.
* `if-else` chooses between two options.
* `else if` checks multiple conditions.
* `Nested if` places one `if` inside another.
* `switch` is useful for fixed choices.
* The ternary operator is a short form of `if-else`.
* A loop repeats code.
* `while` checks the condition before each iteration.
* `do-while` runs the code once before checking the condition.
* `for` is best when the number of repetitions is known.
* A loop usually has initialization, condition, and update.
* `break` stops a loop.
* `continue` skips one iteration.
* An infinite loop never ends.
* Nested loops are useful for patterns and tables.
 
