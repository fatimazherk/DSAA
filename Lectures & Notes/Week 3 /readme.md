# 🔄 Week 3: Doubly & Circular Linked Lists

## 📂 Topics Covered

### 1. Doubly Linked Lists (DLL)
Unlike the Singly Linked List, a DLL node has **three** parts: `Data`, `Next`, and `Prev`.
* **Bidirectional Traversal:** You can move forward and backward.
* **The Trade-off:** Operations are faster (like deleting a node if you already have a pointer to it is $O(1)$), but each node takes up more memory.

### 2. Circular Linked Lists (CLL)
In a Circular list, there is no `NULL` at the end. The **Tail** connects back to the **Head**.
* **Singly Circular:** A standard chain where the last node points to the first.
* **Doubly Circular:** A ring where you can traverse both ways indefinitely.
* **Stopping Condition:** Since `current.next` is never NULL, we stop traversing when `current == head`.

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/eb2cfafa-af1c-4fe4-89f8-eb2c95d9c15f" />



### 3. Complex Operations
We cover the specific logic required to maintain these structures:
* **DLL Insertion:** Requires updating **4 pointers** (New Node's Prev/Next and Neighbor's Prev/Next).
* **DLL Deletion:** "Bridging the gap" by connecting the previous node directly to the next node.
* **CLL Insertion:** If inserting at the Head, you must also update the Tail to point to the new Head.

## 📝 Exam Cheat Sheet (Comparison)

| Structure | Traversal | Memory Per Node | Key Advantage |
| :--- | :--- | :--- | :--- |
| **Singly** | Forward only | Low | Simple, strictly linear. |
| **Doubly** | Forward & Back | High (2 pointers) | Can delete a node in $O(1)$ if you have the address. |
| **Circular** | Infinite Loop | Low/High | Good for Round-Robin scheduling or playlists. |

---
*Tip: In the exam, if you are asked to write code for a Circular List, remember to check if the list is empty first, or your `do-while` loop might crash!*
