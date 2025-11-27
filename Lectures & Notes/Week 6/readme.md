# 📉 Week 6: Elementary Sorting Techniques
<img width="1000" height="420" alt="image" src="https://github.com/user-attachments/assets/59f9fea4-ec18-4164-b119-b346b0376045" />


Welcome to **Week 6**. This week we explore the foundational algorithms for sorting data. While these are not the fastest for massive datasets (see Merge/Quick Sort next week), they are crucial for understanding algorithmic logic and invariant maintenance.

**Key Characteristic:** All three algorithms here have an average time complexity of $O(n^2)$.

## 📂 Topics Covered

### 1. Bubble Sort 🫧
The simplest sorting algorithm to implement, but usually the slowest in practice.
* **The Logic:** Repeatedly step through the list, compare adjacent elements, and **swap** them if they are in the wrong order. The largest elements "bubble" to the top (end) of the list.
* **Optimization:** If you go through a pass with *zero* swaps, the list is already sorted, and you can stop early.


### 2. Selection Sort 🎯
This algorithm focuses on finding the extreme values first.
* **The Logic:** Divide the list into a "sorted" part (left) and "unsorted" part (right). Repeatedly **select** the smallest element from the unsorted side and swap it with the first element of the unsorted side.
* **Key Detail:** It minimizes swaps (max $n$ swaps), but it *always* takes $O(n^2)$ time, even if the array is already sorted.



### 3. Insertion Sort 🃏
The "Card Player's Sort." This is often the fastest of the three for small or nearly-sorted datasets.
* **The Logic:** Build the final sorted array one item at a time. Take the next element and "insert" it into its correct position within the already sorted neighbors.
* **Best Case:** If the data is nearly sorted, this runs in $O(n)$ time!



---


## 📝 Exam Cheat Sheet (Comparison)

| Algo | Time (Avg) | Time (Best) | Stable?* | Note |
| :--- | :--- | :--- | :--- | :--- |
| **Bubble** | $O(n^2)$ | $O(n)$ | Yes | Good for checking if a list is already sorted. |
| **Selection**| $O(n^2)$ | $O(n^2)$ | No | Performs the fewest memory writes (swaps). |
| **Insertion**| $O(n^2)$ | $O(n)$ | Yes | Excellent for small lists (< 50 items) or nearly sorted data. |

*\*Stable means that if two items have the same value, their original order is preserved.*

---
*Tip: For the exam, memorize the inner loops! Bubble Sort compares `j` vs `j+1`. Selection Sort looks for `min_index`. Insertion Sort shifts elements `while value < arr[j]`.*
