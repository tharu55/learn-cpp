# 📘 Flowcharts & Pseudocode

Before writing a program, it is important to understand the problem and plan the solution. **Flowcharts** and **Pseudocode** help us organize our ideas and create a clear algorithm before coding.

---

# 📖 What is a Flowchart?

A **Flowchart** is a graphical representation of an algorithm or process. It uses standard symbols connected by arrows to show the sequence of steps required to solve a problem.

### Example

Instead of writing code immediately, we first create a flowchart to visualize how the program should work.

---

# 🎯 Why Do We Use Flowcharts?

* Helps understand the program logic.
* Makes problem-solving easier.
* Identifies mistakes before coding.
* Improves communication among developers.
* Simplifies debugging and maintenance.
* Serves as a blueprint for writing programs.

---

# 📐 Common Flowchart Symbols

| Symbol          | Name           | Purpose                                          |
| --------------- | -------------- | ------------------------------------------------ |
| ⬭ Oval          | Terminator     | Indicates the **Start** or **End** of a program. |
| ▱ Parallelogram | Input / Output | Used to read input or display output.            |
| ▭ Rectangle     | Process        | Represents calculations or instructions.         |
| ◇ Diamond       | Decision       | Used for conditions (Yes/No, True/False).        |
| ➜ Arrow         | Flow Line      | Shows the direction of execution.                |

---

# 📖 What is Pseudocode?

**Pseudocode** is a simple, language-independent way of writing the steps of an algorithm using plain English. It focuses on the program's logic without worrying about programming syntax.

Unlike programming languages, pseudocode has **no fixed rules**. Its purpose is to make the algorithm easy to understand.

---

# 🎯 Why Do We Use Pseudocode?

* Easy to write and understand.
* Focuses on the solution rather than syntax.
* Can be converted into any programming language.
* Improves logical thinking.
* Reduces coding errors.
* Makes algorithms easier to explain.

---

# 🔄 Flowchart vs Pseudocode

| Flowchart                     | Pseudocode                     |
| ----------------------------- | ------------------------------ |
| Graphical representation      | Text-based representation      |
| Uses symbols and arrows       | Uses simple English statements |
| Easy to visualize the process | Easy to write and modify       |
| Better for presentations      | Better for planning algorithms |

---
*problem 1 :  Finding the Minimum of Two Numbers

1.Pseudocode

START
  DECLARE Integer num1, num2, minimum
  
  DISPLAY "Enter the first number:"
  INPUT num1
  DISPLAY "Enter the second number:"
  INPUT num2
  
  IF num1 < num2 THEN
    minimum = num1
  ELSE
    minimum = num2
  ENDIF
  
  DISPLAY "The minimum number is: ", minimum
END

2.Flowchart

<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/2eab322d-0237-4658-915d-c926eb9aa761" />

*problem 2 : Calculate the Area of a Square

 1.Pseudocode
START
  DECLARE Float side, area
  
  DISPLAY "Enter the length of the square's side:"
  INPUT side
  
  area = side * side
  
  DISPLAY "The area of the square is: ", area
END

2.Flowchart
<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/b63f5da9-47eb-4873-9a75-47fdcbab958a" />

*problem 3 : Sum of Numbers from 1 to N

1.Pseudocode 
START
  DECLARE Integer N, current_num, total_sum
  
  // Input: Get the limit 'N'
  DISPLAY "Enter a positive integer N:"
  INPUT N
  
  // Initialization
  total_sum = 0
  current_num = 1
  
  // Processing: The Loop
  // We add 'current_num' to the 'total_sum' as long as current_num is less than or equal to N.
  WHILE current_num <= N DO
    total_sum = total_sum + current_num
    current_num = current_num + 1
  END WHILE
  
  // Output: Display the final result
  DISPLAY "The sum of numbers from 1 to ", N, " is: ", total_sum
END

2.Flowchart
<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/2712fcba-6764-40e0-973d-f35de3afad70" />

*problem 4: Give Number Is Prime Or Not
// Input: integer n (n > 1)
// Output: TRUE if n is prime, FALSE otherwise

FUNCTION isPrime(integer n) RETURNS BOOLEAN
    
    // Check if number is 1, which is a special case (not prime)
  
    IF n <= 1 THEN
        RETURN FALSE
    END IF
    
    // Check if number is 2 or 3, which are primes
    IF n <= 3 THEN
        RETURN TRUE
    END IF
    
    // Check divisible by 2 or 3 (handles all even and many small composites)
    IF n % 2 == 0 OR n % 3 == 0 THEN
        RETURN FALSE
    END IF
    
    // Optimization: All primes > 3 are of form 6k ± 1
    // We only need to check up to the square root of n.
    SET i = 5
    WHILE i * i <= n DO
        // Check for n % i and n % (i + 2)
        IF n % i == 0 OR n % (i + 2) == 0 THEN
            RETURN FALSE
        END IF
        SET i = i + 6
    END WHILE
    
    // If no divisors found up to sqrt(n), n is prime
    RETURN TRUE
END FUNCTION

// Main routine
START
    PRINT "Enter an integer > 1 to test for primality:"
    n = INPUT
    isPrime(n)
END

2.Flowchart
<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/db82caba-ef8e-4547-9222-d2bf3ac6c281" />


