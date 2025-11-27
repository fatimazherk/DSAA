# 🌳 Week 9: Binary Trees (Properties & Types)

Welcome to **Week 9**. We are breaking away from linear data structures (Arrays, Linked Lists) to explore **Hierarchical** structures.

A **Binary Tree** is a structure where every node has at most **two children** (Left and Right). This structure forms the foundation for advanced databases and file systems.

## 📂 Topics Covered

### 1. Tree Terminology
You cannot pass the exam without knowing the vocabulary:
* **Root:** The topmost node (no parent).
* **Leaf:** A node with no children.
* **Height:** The length of the path from the Root to the deepest Leaf.
* **Depth/Level:** The distance from the Root to the current node.



### 2. Properties ( The Math )
Binary Trees follow strict mathematical rules useful for complexity analysis:
* **Max Nodes:** A tree of height $h$ has at most $2^{h+1} - 1$ nodes.
* **Min Height:** To store $n$ nodes, the minimum height is $\lfloor \log_2 n \rfloor$.
* **Edges:** A tree with $n$ nodes always has exactly $n-1$ edges.

### 3. Types of Binary Trees
Distinguishing these is a common "Multiple Choice" exam topic.

#### 🟢 Full Binary Tree (Strict)
* **Rule:** Every node has either **0** or **2** children.
* **No:** Nodes with only 1 child are forbidden.

#### 🔵 Complete Binary Tree
* **Rule:** All levels are completely filled, except possibly the last level.
* **Constraint:** The last level must be filled from **Left to Right**.
* **Why it matters:** This is required for Heaps (Week 10).

#### 🟣 Perfect Binary Tree
* **Rule:** All internal nodes have 2 children, and all leaves are at the same level.
* **Stats:** It has the maximum possible number of nodes for its height.



---


## 📝 Exam Cheat Sheet (Definitions)

| Type | Definition | Key Visual |
| :--- | :--- | :--- |
| **Full** | 0 or 2 children. | No single children allowed. |
| **Complete**| Filled Left-to-Right. | No gaps on the left side of the bottom row. |
| **Perfect** | Symmetrical triangle. | Every level is 100% full. |
| **Balanced**| Minimized Height. | Left and Right subtrees differ in height by max 1. |

---
