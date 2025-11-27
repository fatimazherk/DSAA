# 🚀 Week 7: Advanced Sorting (Merge & Quick)

Welcome to **Week 7**. We leave behind the slow "Quadratic" sorts of last week. This week focuses on **Divide and Conquer** algorithms, which are the industry standard for sorting large datasets efficiently.

**The Goal:** Achieve $O(n \log n)$ time complexity.

## 📂 Topics Covered

### 1. The Divide and Conquer Strategy
Both algorithms follow this pattern:
1.  **Divide:** Break the problem into sub-problems.
2.  **Conquer:** Solve the sub-problems recursively.
3.  **Combine:** Join the answers to form the final result.

### 2. Merge Sort 🧩
The "Safe and Steady" choice.
* **The Logic:** Recursively cut the list in half until you have single items. Then, **Merge** the sub-lists back together in sorted order.
* **Space Trade-off:** It is faster, but it requires "Auxiliary Space" (an extra array) to hold the data while merging.
* **Key Feature:** It is **Stable** (preserves original order of equals) and guarantees $O(n \log n)$ even in the worst case.



### 3. Quick Sort ⚡
The "Risky but Rapid" choice.
* **The Logic:** Pick a **Pivot** element. Reorder the list so everything smaller than the pivot is on the left, and everything larger is on the right (**Partitioning**). Then recurse on both sides.
* **The Pivot Problem:** If you pick a bad pivot (e.g., the smallest item), the algorithm degrades to $O(n^2)$.
* **Key Feature:** It is done **In-Place** (saves memory) and is usually faster than Merge Sort in practice due to hardware caching, despite the worst-case risk.



---

## 📝 Exam Cheat Sheet (The Showdown)

| Feature | Merge Sort | Quick Sort |
| :--- | :--- | :--- |
| **Strategy** | Divide & Conquer | Divide & Conquer |
| **Avg Time** | $O(n \log n)$ | $O(n \log n)$ |
| **Worst Time**| $O(n \log n)$ | $O(n^2)$ (Bad pivot) |
| **Space** | $O(n)$ (Heavy) | $O(\log n)$ (Stack only) |
| **Stable?** | Yes | No |
| **Best For** | Linked Lists | Arrays |

---
