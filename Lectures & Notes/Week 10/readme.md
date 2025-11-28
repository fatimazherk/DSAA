<h1>Week 10: Binary Heaps, Heap Sort, and Priority Queues</h1>

This week focuses on the <strong>Heap</strong> data structure, a critical component in efficient algorithm design. We cover the internal mechanics of Binary Heaps, how to use them to sort data (Heap Sort), and their application in building Priority Queues.</p>

<hr>

<h2>📚 Table of Contents</h2>

<ul>
<li><a href="#binary-heap">1. Binary Heap</a>
<ul>
<li><a href="#structure--properties">Structure & Properties</a></li>
<li><a href="#array-representation">Array Representation</a></li>
<li><a href="#operations">Operations</a></li>
</ul>
</li>
<li><a href="#heap-sort">2. Heap Sort</a>
<ul>
<li><a href="#algorithm">Algorithm</a></li>
<li><a href="#complexity">Complexity</a></li>
</ul>
</li>
<li><a href="#priority-queue">3. Priority Queue</a></li>
<li><a href="#implementation-examples">4. Implementation Examples</a></li>
</ul>

<hr>

<h2 id="binary-heap">1. Binary Heap</h2>

<p>A <strong>Binary Heap</strong> is a specialized tree-based data structure that satisfies the <em>heap property</em>. It is essentially a complete binary tree.</p>

<h3 id="structure--properties">Structure & Properties</h3>
<p>There are two main types of binary heaps:</p>
<ul>
<li><strong>Max-Heap</strong>: The key present at the <em>root</em> node must be greatest among the keys present at all of its children. The same property must be recursively true for all sub-trees.</li>
<li><strong>Min-Heap</strong>: The key present at the <em>root</em> node must be minimum among the keys present at all of its children.</li>
</ul>

<p><strong>Key Characteristics:</strong></p>
<ul>
<li><strong>Complete Binary Tree</strong>: All levels are completely filled except possibly the last level, and the last level has all keys as left as possible.</li>
<li><strong>Heap Property</strong>: The parent is always greater (Max-Heap) or smaller (Min-Heap) than its children.</li>
</ul>

<h3 id="array-representation">Array Representation</h3>
<p>Binary Heaps are typically implemented using arrays because they are complete binary trees.</p>
<p>For a node at index <code>i</code> (0-based index):</p>
<ul>
<li><strong>Parent:</strong> <code>(i - 1) // 2</code></li>
<li><strong>Left Child:</strong> <code>2 * i + 1</code></li>
<li><strong>Right Child:</strong> <code>2 * i + 2</code></li>
</ul>

<h3 id="operations">Operations</h3>

<table>
<thead>
<tr>
<th>Operation</th>
<th>Description</th>
<th>Time Complexity</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Insert</strong></td>
<td>Add a new key at the end of the tree and "bubble up" (heapify up) to restore the heap property.</td>
<td>O(log N)</td>
</tr>
<tr>
<td><strong>Extract Max/Min</strong></td>
<td>Remove the root. Replace it with the last element, then "bubble down" (heapify down).</td>
<td>O(log N)</td>
</tr>
<tr>
<td><strong>Peek/Get Max/Min</strong></td>
<td>Return the root element without removing it.</td>
<td>O(1)</td>
</tr>
<tr>
<td><strong>Build Heap</strong></td>
<td>Create a heap from an arbitrary array.</td>
<td>O(N)</td>
</tr>
</tbody>
</table>

<hr>

<h2 id="heap-sort">2. Heap Sort</h2>

<p><strong>Heap Sort</strong> is a comparison-based sorting algorithm based on the Binary Heap data structure. It is similar to selection sort where we first find the minimum element and place the minimum element at the beginning. We repeat the same process for the remaining elements.</p>

<h3 id="algorithm">Algorithm</h3>
<ol>
<li><strong>Build a Max-Heap</strong> from the input data.</li>
<li><strong>Swap</strong> the root (largest element) with the last item of the heap.</li>
<li><strong>Reduce</strong> the heap size by 1.</li>
<li><strong>Heapify</strong> the root of the tree to ensure the heap property holds for the new root.</li>
<li>Repeat steps 2-4 until the heap size is 1.</li>
</ol>

<h3 id="complexity">Complexity</h3>
<ul>
<li><strong>Time Complexity:</strong> O(N log N) for all cases (Best, Average, Worst).</li>
<li><strong>Space Complexity:</strong> O(1) (In-place sorting).</li>
<li><strong>Stability:</strong> Not stable.</li>
</ul>

<hr>

<h2 id="priority-queue">3. Priority Queue</h2>

<p>A <strong>Priority Queue</strong> is an abstract data type similar to a regular queue or stack data structure in which each element additionally has a "priority" associated with it. In a priority queue, an element with high priority is served before an element with low priority.</p>

<p>While Priority Queues can be implemented with arrays or linked lists, <strong>Heaps</strong> are the most efficient implementation for general usage.</p>

<h3>Standard Operations</h3>
<ol>
<li><strong>enqueue(item, priority)</strong>: Insert an item with a specific priority.</li>
<li><strong>dequeue()</strong>: Remove and return the element with the highest priority.</li>
<li><strong>peek()</strong>: View the highest priority element without removing it.</li>
</ol>

<h3>Applications</h3>
<ul>
<li><strong>Dijkstra's Algorithm</strong>: Finding the shortest path in a graph.</li>
<li><strong>Prim's Algorithm</strong>: Minimum Spanning Tree.</li>
<li><strong>Huffman Coding</strong>: Data compression.</li>
<li><strong>OS Task Scheduling</strong>: Managing processes based on priority.</li>
</ul>

<hr>
