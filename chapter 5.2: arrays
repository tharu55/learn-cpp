

## 1. Memory Address of an Array ⭐⭐⭐

Every element in an array has its own memory address.

The address of each element can be accessed using the **address-of operator (`&`)**.

### Example

```cpp
#include <iostream>
using namespace std;

int main()
{
    int marks[5] = {85, 90, 78, 88, 95};

    cout << &marks[0] << endl;
    cout << &marks[1] << endl;
    cout << &marks[2] << endl;

    return 0;
}
```

### Important Points

* Every element has a different memory address.
* The addresses are stored continuously.
* This concept is very important for learning **Pointers** later.

---

# 2. Array Size

The size of an array is the maximum number of elements it can store.

```cpp
int marks[5];
```

Here,

* Array Name = `marks`
* Size = **5**
* Valid Index = **0 to 4**

---

# 3. Array Length Using `sizeof()` ⭐⭐⭐

C++ provides the `sizeof()` operator to calculate the number of elements.

```cpp
int marks[] = {10,20,30,40,50};

int length = sizeof(marks) / sizeof(marks[0]);

cout << length;
```

### Output

```
5
```

### Why does this work?

* `sizeof(marks)` → Total size of the array in bytes.
* `sizeof(marks[0])` → Size of one element.
* Total size ÷ Size of one element = Number of elements.

---

# 4. Default Values

Default values depend on where the array is declared.

### Local Array

```cpp
int arr[5];
```

Values are **garbage values** (uninitialized).

---

### Global Array

```cpp
int arr[5];
```

Values are automatically initialized to **0**.

---

# 5. Types of Initialization ⭐⭐

### Complete Initialization

```cpp
int arr[5]={1,2,3,4,5};
```

---

### Partial Initialization

```cpp
int arr[5]={10,20};
```

Remaining elements become **0**.

Output

```
10 20 0 0 0
```

---

### Size Automatically Decided

```cpp
int arr[]={1,2,3,4,5};
```

Compiler counts the elements automatically.

---

# 6. Array Traversal

Traversal means visiting every element of an array one by one.

Traversal is usually done using:

* for loop
* while loop
* do-while loop

---

