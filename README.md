[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/P7LOX4wp)
Welcome to your first lab! This repository contains 3 C programs.

1.  **`ex1_finance.c`**: Needs debugging (Calculations are wrong).
2.  **`ex2_access.c`**: Needs debugging (Security flaws).
3.  **`ex3_shipping.c`**: Needs logic (You must write the code).

Your goal is to fix the broken programs and implement the missing logic for the coin machine.

## Instructions

1.  **Clone** this repository to your local machine.
2.  **Compile** the files using `gcc` with the warning flags
    *   *Example:* `gcc -g -Wall -Wextra -Werror -std=c2x ex1_finance.c -o ex1`
3.  **Run** the executable.
    *   *Example:* `./ex1`
4.  **Observe** the output. Does it match what the program *should* do?
5.  **Fix/Edit** the code in your text editor.
6.  **Fill out the "Lab Report"** at the bottom of this README.
7.  **Commit** your changes and **Push** back to GitHub.

---

## The Exercises

### Exercise 1: Finance (`ex1_finance.c`)
This program attempts to calculate a year-end salary with a 10% bonus.
*   **The Problem:** The math is wrong, and the output prints wrong numbers.
*   **Your Job:** Fix the issues and report below!

### Exercise 2: Access Control (`ex2_access.c`)
This is a security system that requires a specific PIN (`1234`) to disarm.
*   **The Problem:** The system lets everyone in, no matter what number they type. Also, the output messages look messy.
*   **Your Job:** Fix the issues and report below!

### Exercise 3: Jungle Shipping (`ex3_shipping.c`)
This program calculates the shipping cost for a package based on weight, distance, and speed.
*   **The Problem:** The code logic is missing! The program runs, but costs are always $0.00.
*   **Your Job:** Write the logic to implement the pricing rules found in the comments.
    1.  **Validation:** Reject negative weights or distances.
    2.  **Base Cost:** \$5.00 base. Add \$2/kg only for weight *above* 5kg.
    3.  **Distance:** Add $0.10/km only for distance *above* 100km.
    4.  **Express:** Double the total price if the `is_overnight` boolean is `true`.

---

## Lab Report

### Exercise 1: Finance
*   **What was the logic bug?**
    > The logic bug was in line 9. Since both bonus_percentage (10) and 100 are integers, C performs integer division. This evaluates to 0 which cuts off the decimal portion. To fix this, I changed 100 to 100.0 to force floating-point division.
*   **What was the syntax/format bug?**
    > The syntax/format bug was in line 18. The variable final_salary is an integer (int), but the format specifier used is %f (which is for floats). This error will cause printf to display something other than an integer. It should be %d.

### Exercise 2: Access Control
*   **Why did the program allow any password to work?**
    > The error was in line 11. The code uses only 1 equals sign =, which is the assignment operator, instead of 2 equals signs ==, which is the comparison operator. This assigns the value 1234 to user_input inside the condition. Since 1234 is a non-zero number, C thinks the condition is True, which is why access was always granted regardless of what the user typed.
*   **How did you fix the "System Disarmed" message printing every time?**
    > I added curly braces {} around the lines after the if statement. Without braces, an if statement only controls the line of code that comes after it. Grouping them with braces ensures both lines only run when the condition is true.

### Exercise 3: Shipping Test Case
Run your finished `ex3_shipping.c` with the following inputs. What is the final cost?

**Test Case A:**
*   Weight: `10`
*   Distance: `50`
*   Overnight: `n`
*   **Your Result:** $15.00

**Test Case B:**
*   Weight: `2`
*   Distance: `200`
*   Overnight: `y`
*   **Your Result:** $30.00

**Test Case C (Error Check):**
*   Weight: `-5`

*   **Did your program print an error message?** Yes
