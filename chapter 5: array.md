# 📘 Arrays in C++

## Introduction

Sometimes we need to store many values in a program. If we create a separate variable for each value, the program becomes long and difficult to manage.

To solve this problem, C++ provides **arrays**.

An array lets us store **many values of the same data type** in **one variable**.

---

# Definition

An **array** is a variable that stores **more than one value** of the **same data type**.

Instead of creating many variables, we create **one array**.

---

# Why Do We Use Arrays?

Suppose you want to store the marks of 5 students.

Without an array, you need five variables.

```cpp
int mark1 = 85;
int mark2 = 90;
int mark3 = 78;
int mark4 = 88;
int mark5 = 95;
```

This works, but if there are 100 students, you need 100 variables.

Using an array, all the marks can be stored in one variable.

```cpp
int marks[5] = {85, 90, 78, 88, 95};
```

Now the program is shorter and easier to understand.

---

# Advantages of Arrays

* Store many values in one variable.
* Reduce the number of variables.
* Make programs easier to write.
* Work well with loops.
* Save time when writing code.

---

# Array Declaration

Before using an array, we must declare it.

### Syntax

```cpp
data_type array_name[size];
```

### Example

```cpp
int marks[5];
```

Here,

* `int` → data type
* `marks` → array name
* `5` → number of values the array can store

---

# Array Initialization

Initialization means giving values to an array.

```cpp
int marks[5] = {85, 90, 78, 88, 95};
```

Now the array contains five values.

---

# Array Index

Every value in an array has a position.

This position is called the **index**.

The index always starts from **0**.

| Index | Value |
| ----: | ----: |
|     0 |    85 |
|     1 |    90 |
|     2 |    78 |
|     3 |    88 |
|     4 |    95 |

For an array of size **5**, the index goes from **0 to 4**.

---

# Accessing Array Elements

To get a value from an array, we use its index.

Example:

```cpp
cout << marks[0];
```

Output

```
85
```

`marks[0]` gives the first value of the array.

---

# Printing All Array Elements

Instead of printing each value one by one, we use a loop.

```cpp
for(int i = 0; i < 5; i++)
{
    cout << marks[i] << " ";
}
```

Output

```
85 90 78 88 95
```

The loop prints every value in the array.

---

# Taking Input into an Array

We can also store values entered by the user.

```cpp
for(int i = 0; i < 5; i++)
{
    cin >> marks[i];
}
```

This loop stores five values in the array.

---

# Finding the Sum of Array Elements

We use a loop to add all the values in an array.

```cpp
sum = sum + marks[i];
```

After the loop ends, the variable `sum` contains the total of all elements.

---

# Finding the Largest Element

Start by assuming the first value is the largest.

Then compare it with the remaining values.

If a larger value is found, update the largest value.

After checking all the elements, we get the largest number in the array.

---

# Finding the Smallest Element

The logic is the same as finding the largest element.

Start with the first value and replace it whenever a smaller value is found.

---

# Types of Arrays

### One-Dimensional (1D) Array

A 1D array stores values in a single list.

```cpp
int marks[5];
```

---

### Two-Dimensional (2D) Array

A 2D array stores values in rows and columns.

```cpp
int matrix[3][3];
```

It is mainly used for tables and matrices.

---

# Common Mistakes

* Starting the index from **1** instead of **0**.
* Accessing an index outside the array size.
* Writing the wrong loop condition.
* Declaring the wrong array size.

---

# Important Points

* An array stores multiple values.
* All values must have the same data type.
* The first index is always **0**.
* Arrays are mostly used with loops.
* Each value in an array is called an **element**.

---

# Summary

An array is a variable that stores multiple values of the same data type. It helps reduce the number of variables and makes programs shorter and easier to understand. Arrays are commonly used with loops to store and process many values.

