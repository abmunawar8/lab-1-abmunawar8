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
    > [Type your answer here]
*   **What was the syntax/format bug?**
    > [Type your answer here]

### Exercise 2: Access Control
*   **Why did the program allow any password to work?**
    > [Type your answer here]
*   **How did you fix the "System Disarmed" message printing every time?**
    > [Type your answer here]

### Exercise 3: Shipping Test Case
Run your finished `ex3_shipping.c` with the following inputs. What is the final cost?

**Test Case A:**
*   Weight: `10`
*   Distance: `50`
*   Overnight: `0`
*   **Your Result:** $________

**Test Case B:**
*   Weight: `2`
*   Distance: `200`
*   Overnight: `1`
*   **Your Result:** $________

**Test Case C (Error Check):**
*   Weight: `-5`
*   **Did your program print an error message?** (Yes/No)