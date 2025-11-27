## 🎫 Week 5: Queues, Circular Queues & Deques

Welcome to **Week 5**. While Stacks (Week 4) were LIFO, Queues are **FIFO** (First-In, First-Out). This week explores how to manage data that needs to be processed in the exact order it arrived (like printer jobs or CPU scheduling).

## 📂 Topics Covered

### 1. The Linear Queue
The standard "waiting line" structure.
* **Enqueue:** Add item to the **Rear**. ($O(1)$)
* **Dequeue:** Remove item from the **Front**. ($O(1)$)
* **The Problem:** In a fixed-size array implementation, dequeuing creates empty, unusable space at the front. The queue "drifts" through memory until it hits the limit.



### 2. The Circular Queue (Ring Buffer)
To fix the "wasted space" problem, we treat the array as a circle.
* **The Logic:** When we reach the end of the array, the `Next` pointer wraps around to index 0.
* **The Formula:** We use Modulo Arithmetic: `Next Position = (Current + 1) % Size`.
* **Full vs. Empty:** Distinguishing between a full buffer and an empty one often requires a `count` variable or sacrificing one slot.



### 3. Double Ended Queue (Deque)
This is a hybrid structure.
* **Flexibility:** You can Enqueue or Dequeue from **both** the Front and the Rear.
* **Use Cases:** Undo/Redo operations, or checking for Palindromes.
* **Input/Output Restricted:** Variations where insertion is allowed at both ends but deletion is only one (or vice versa).



## 📝 Exam Cheat Sheet

| Type | Order | Key Feature | Complexity |
| :--- | :--- | :--- | :--- |
| **Linear Queue** | FIFO | Simple, but wastes space (in arrays). | $O(1)$ ops |
| **Circular Queue** | FIFO | Reuses empty slots at the front. | $O(1)$ ops |
| **Deque** | Hybrid | Insert/Delete at **both** ends. | $O(1)$ ops |
| **Priority Queue** | Ranked | Highest priority leaves first (Week 8 preview). | $O(\log n)$ |

---
*Tip: For the exam, memorize the Circular Queue formula: `(rear + 1) % size`. If you forget the modulo operator `%`, the logic breaks!*
