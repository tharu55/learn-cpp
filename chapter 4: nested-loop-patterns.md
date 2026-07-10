Absolutely! These are **nested loop pattern programs**, and once you understand **what `i` and `j` do**, every pattern becomes easy.

---

# 📘 C++ Nested Loops Notes

## What is a Nested Loop?


A nested loop is a loop inside another loop. It is mainly used to print patterns, work with rows and columns, and solve problems involving 2D arrays.

The outer loop controls how many rows will be printed, while the inner loop controls how many times something is printed in each row.

* **Outer loop (`i`)** → Controls the **rows**.
* **Inner loop (`j`)** → Controls what is printed in each **column**.

### Basic Syntax

```cpp
for(int i = 0; i < rows; i++) {
    for(int j = 0; j < columns; j++) {
        // Print something
    }
    cout << endl;
}
```

### Easy Remember

| Loop             | Work                   |
| ---------------- | ---------------------- |
| Outer Loop (`i`) | Controls rows          |
| Inner Loop (`j`) | Controls columns       |
| `cout << endl;`  | Moves to the next line |

---

# Program 1 - Print Numbers in a Square Pattern

Program: 

```cpp
#include <iostream>
using namespace std;
int main() {
    int n=3;
    int num=1;
    for(int i=0; i<n; i++){ //this line conrols rows
        for(int j=0; j<n; j++){ // this line conrols columns
            cout << num; 
            num++;
    
        }
        cout << endl;

    }
    return 0;
}
```

## Output

```
123
456
789
```

## Step-by-Step Explanation

### Variables

```cpp
int n = 3;
```

Means there are **3 rows** and **3 columns**.

```cpp
int num = 1;
```

Printing starts from **1**.

---

### Outer Loop

```cpp
for(int i=0; i<n; i++)
```

Runs **3 times**.

| i | Row        |
| - | ---------- |
| 0 | First Row  |
| 1 | Second Row |
| 2 | Third Row  |

---

### Inner Loop

```cpp
for(int j=0; j<n; j++)
```

Runs **3 times** in every row.

During each loop:

```cpp
cout << num;
num++;
```

prints the number and increases it by 1.

### Execution

Row 1

```
1 2 3
```

Row 2

```
4 5 6
```

Row 3

```
7 8 9
```

---

# Program 2 - Square Star Pattern

Program: 

```cpp
#include <iostream>
using namespace std;
int main() {
    int n=4;
    for(int i=0; i<n; i++){
        for(int j=0; j<n; j++){
            cout << "*";
    
        }
        cout << endl;

    }
    return 0;
}
```

## Output

```
****
****
****
****
```

## Explanation

Outer loop runs **4 rows**.

Inner loop prints **4 stars** in every row.

### Table

| Row | Stars Printed |
| --- | ------------- |
| 1   | ****          |
| 2   | ****          |
| 3   | ****          |
| 4   | ****          |

---

# Program 3 - Number Triangle

Program: 

```cpp
#include <iostream>
using namespace std;
int main() {
    int n=4;
    
    for(int i=0; i<n; i++){
        for(int j=0; j<i+1; j++){
            cout << i+1;
            
        }
        cout << endl;

    }
    return 0;
}
```

## Output

```
1
22
333
4444
```

## Why `i+1`?

Because `i` starts from **0**.

| i | i+1 |
| - | --- |
| 0 | 1   |
| 1 | 2   |
| 2 | 3   |
| 3 | 4   |

---

### Why `j < i+1`?

This controls how many numbers are printed.

| Row | Times Printed |
| --- | ------------- |
| 1   | 1             |
| 2   | 2             |
| 3   | 3             |
| 4   | 4             |

---

# Program 4 - Alphabet Triangle

Program: 

```cpp
#include <iostream>
using namespace std;
int main() {
    int n=4;
    
    for(int i=0; i<n; i++){
        for(int j=0; j<i+1; j++){
            cout << char('A'+i);
            
        }
        cout << endl;

    }
    return 0;
}
```

## Output

```
A
BB
CCC
DDDD
```

## Explanation

ASCII values

```
A = 65
B = 66
C = 67
D = 68
```

When

```
i = 0
'A'+0 = A
```

```
i = 1
'A'+1 = B
```

```
i = 2
'A'+2 = C
```

---

# Program 5 - Reverse Number Pattern

Program: 

```cpp
#include <iostream> // revers order
using namespace std;
int main (){
    int n=4;
    for (int i=0; i<n; i++){
for (int j=i+1; j>0;j--){
    cout <<j;
}
cout <<endl;
    }
    return 0;
   
}
```

## Output

```
1
21
321
4321
```

## Explanation

Row 1

```
j = 1
```

Print

```
1
```

Row 2

```
j = 2
```

Print

```
2 1
```

Row 3

```
j = 3
```

Print

```
3 2 1
```

Each row counts backwards to 1.

---

# Program 6 - Continuous Number Triangle

Program: 

```cpp
#include <iostream>
using namespace std;
int main (){
    int n=4;
    int num=1;
    for (int i=0; i<n; i++){
        for (int j=0; j<i+1;j++){
            cout << num;
            num++;
        }
        cout <<endl;

    }
    return 0;
}
```

## Output

```
1
23
456
78910
```

## Explanation

Unlike Program 1, the variable `num` is **not reset** after each row.

It continues increasing.

| Print | Value |
| ----- | ----- |
| 1     | 1     |
| 2     | 2     |
| 3     | 3     |
| 4     | 4     |
| 5     | 5     |
| 6     | 6     |
| 7     | 7     |
| 8     | 8     |
| 9     | 9     |
| 10    | 10    |

---

# Program 7 - Inverted Number Pattern

Program: 

```cpp
#include <iostream>
using namespace std;
int main (){
    int n=4;
for (int i=0; i<n;i++){
    for(int j=0; j<i; j++){
        cout <<  " ";
    }
        for(int j=0; j<n-i; j++){
        cout << i+1 ;
        }
    cout << endl;
    
}
return 0;
}
```

## Output

```
1111
 222
  33
   4
```

## Explanation

### First Loop

```cpp

for(int j=0;j<i;j++)
```

Prints spaces.

| Row | Spaces |
| --- | ------ |
| 1   | 0      |
| 2   | 1      |
| 3   | 2      |
| 4   | 3      |

---

### Second Loop

```cpp
for(int j=0;j<n-i;j++)
```

Prints numbers.

| Row | Numbers Printed |
| --- | --------------- |
| 1   | 4               |
| 2   | 3               |
| 3   | 2               |
| 4   | 1               |

---

# ⭐ Easy Trick to Solve Any Pattern

Whenever you see a pattern, ask yourself these 4 questions:

1. **How many rows are there?** → Outer loop (`i`)
2. **How many columns are printed in each row?** → Inner loop (`j`)
3. **What should be printed?** → `*`, number, or character
4. **Should the number of columns increase or decrease?** → Decide the inner loop condition (`j < i+1`, `j < n-i`, etc.)

## 🎯 Remember These Rules

| Pattern Type        | Inner Loop Condition  |
| ------------------- | --------------------- |
| Square              | `j < n`               |
| Increasing Triangle | `j < i+1`             |
| Decreasing Triangle | `j < n-i`             |
| Reverse Counting    | `j = i+1; j > 0; j--` |
| Spaces              | `j < i`               |

These seven programs are the **foundation of nested loops**. Once you're comfortable with them, you'll find it much easier to solve more advanced pattern questions in C++.
