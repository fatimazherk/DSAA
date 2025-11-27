# 🔗 Week 2: Linked List Operations

## 📂 Topics Covered

### 1. The Structure
* **Node Anatomy:** Understanding that a Node = `Data` + `Next Pointer`.
* **Head & Tail:** Managing the entry points of the list.
* **Why Linked Lists?** Dynamic size vs. Fixed size (Arrays).


### 2. Insertion Operations
We cover adding nodes at various positions. Remember: *Order matters* to avoid losing the rest of the list!
* **At Beginning:** Update Head to point to new node. ($O(1)$)
* **At End:** Traverse to the last node and link. ($O(n)$)
* **At Position/Middle:** Traverse to `n-1`, link new node to `n`, then link `n-1` to new node.

### 3. Deletion Operations
Removing nodes requires careful pointer re-linking to prevent memory leaks or broken chains.
* **Delete Head:** Move Head pointer to `Head.next`.
* **Delete by Value/Key:** Search for the value, then bypass the node (`prev.next = current.next`).

### 4. Search & Sorting
* **Linear Search:** Since Linked Lists do not have indexes (Random Access), we must iterate sequentially from the Head. Complexity: $O(n)$.
* **Sorting:**
    * **Bubble Sort:** Swapping data (easier) or swapping pointers (harder).
    * **Merge Sort:** The preferred algorithm for Linked Lists as it doesn't require random access.

---

## 📝 Exam Cheat Sheet (Complexity)

| Operation | Complexity | Note |
| :-------- | :--------- | :--- |
| **Access** | $O(n)$ | No random access (unlike arrays). |
| **Insert (Head)** | $O(1)$ | Very fast. |
| **Insert (Tail)** | $O(n)$ | Unless you maintain a `tail` pointer. |
| **Search** | $O(n)$ | Must traverse linearly. |

---
*Tip: For the exam, always draw the boxes and arrows on scratch paper before writing the code!*
