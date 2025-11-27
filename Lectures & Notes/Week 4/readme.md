# 🥞 Week 4: Recursion & The Stack

Welcome to **Week 4**. This week deals with the "Last-In, First-Out" (LIFO) principle and how it powers one of the most important concepts in computer science: Recursion.

Understanding the Stack is the key to understanding how your code actually runs in memory!

## 📂 Topics Covered

### 1. The Stack ADT
The Stack is a linear data structure that follows the **LIFO** (Last-In, First-Out) order. Think of a stack of plates in a cafeteria.
* **Push:** Add an item to the top. ($O(1)$)
* **Pop:** Remove the item from the top. ($O(1)$)
* **Peek/Top:** Look at the top item without removing it.


### 2. Recursion
Recursion occurs when a function calls itself to solve a smaller instance of the problem.
* **The Base Case:** The condition to **stop** the recursion (prevents infinite loops).
* **The Recursive Case:** The logic that breaks the problem down and moves towards the base case.
* **Tail Recursion:** A special form where the recursive call is the very last action (can be optimized by compilers).

### 3. The "Call Stack" (The Missing Link)
Why do we teach Stacks and Recursion together?
* Every time a function is called, a **Stack Frame** (containing local variables and return addresses) is "Pushed" onto the system memory stack.
* When the function returns, the frame is "Popped."
* **Stack Overflow:** This happens when you have infinite recursion. You run out of memory space on the stack!


## 📝 Exam Cheat Sheet

| Concept | Explanation | Complexity |
| :--- | :--- | :--- |
| **LIFO** | The last thing added is the first thing removed. | N/A |
| **Stack Space** | The memory used by recursion depth. | $O(d)$ where $d$ is depth. |
| **Base Case** | **CRITICAL.** If you forget this, the program crashes. | N/A |
| **Iterative** | Uses loops (`for`/`while`). | Usually $O(1)$ space. |
| **Recursive** | Uses function calls. | Uses Stack memory space. |

---
*Tip: If an exam question asks you to "Trace" a recursive function, draw a literal stack of boxes on your paper. Add a box when called, cross it out when returned.*
