# 🗻 Week 10: Binary Heaps, Priority Queues & Heap Sort

Welcome to the **Binary Heap** module. While this looks like a Binary Tree, it behaves very differently. We stop organizing by "Left is smaller, Right is bigger" (BST) and switch to "Parent is always superior to Child" (Heap).

## 📂 Topics Covered

### 1. The Binary Heap Structure
A Heap is a **Complete Binary Tree** that satisfies the **Heap Property**.
* **Max-Heap:** The Root is the largest element. Every parent > children.
* **Min-Heap:** The Root is the smallest element. Every parent < children.
* **Array Implementation:** We rarely use Nodes/Pointers for Heaps. We use Arrays with index math:
    * Left Child: $2i + 1$
    * Right Child: $2i + 2$
    * Parent: $\lfloor (i - 1) / 2 \rfloor$



### 2. Priority Queue (PQ) ⚡
The Priority Queue is the Abstract Data Type (ADT); the Heap is the data structure we use to build it efficiently.
* **Concept:** It's not FIFO (First-In, First-Out). It is "Highest Priority Out."
* **Operations:**
    * `insert`: Add to bottom, then **"Bubble Up"** (swapping with parent).
    * `deleteMax`: Remove Root, move last element to top, then **"Bubble Down"** (sink to correct spot).
    * **Complexity:** Both operations take $O(\log n)$.

### 3. Heap Sort 📉
A very efficient sorting algorithm that uses a Max-Heap.
1.  **Build Heap:** Turn the unsorted array into a Max-Heap.
2.  **Extract:** Swap the Root (max) with the last element.
3.  **Shrink & Heapify:** Ignore the last element (now sorted) and fix the heap. Repeat.
* **Pros:** $O(n \log n)$ time and $O(1)$ extra space (In-Place).
* **Cons:** Not Stable (reorders equal elements).



---

## 📝 Exam Cheat Sheet (BST vs Heap)

| Feature | Binary Search Tree (BST) | Binary Heap |
| :--- | :--- | :--- |
| **Rule** | Left < Parent < Right | Parent > Children (Max) |
| **Search** | $O(\log n)$ (Fast) | $O(n)$ (Slow - not designed for search) |
| **Find Max** | $O(\log n)$ (Go right) | $O(1)$ (It's the Root!) |
| **Structure** | Can be unbalanced | ALWAYS Complete (Filled L-to-R) |
| **Use Case** | Searching/Databases | Priority Queues/Scheduling |

---
