<h1>Week 11: Binary Search Trees</h1>

<hr>

<h2>📚 Table of Contents</h2>

<h3> Binary Search Trees</h3>
<ul>
<li><a href="#bst-intro">4. Binary Search Tree (BST)</a>
<ul>
<li><a href="#bst-properties">Properties</a></li>
<li><a href="#bst-operations">Operations</a></li>
</ul>
</li>
<li><a href="#bst-applications">5. Applications</a></li>
<li><a href="#bst-issues">6. Issues & Limitations</a></li>
<li><a href="#implementation-examples">7. Implementation Examples</a></li>
</ul>

<hr>

<p>A <strong>Binary Search Tree (BST)</strong> is a node-based binary tree data structure which has the following properties:</p>

<h3 id="bst-properties">Properties</h3>
<ol>
<li>The left subtree of a node contains only nodes with keys <strong>lesser</strong> than the node’s key.</li>
<li>The right subtree of a node contains only nodes with keys <strong>greater</strong> than the node’s key.</li>
<li>The left and right subtree each must also be a binary search tree.</li>
<li>There must be no duplicate nodes (typically).</li>
</ol>

<h3 id="bst-operations">Operations</h3>

<table>
<thead>
<tr>
<th>Operation</th>
<th>Description</th>
<th>Avg Case</th>
<th>Worst Case</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Search</strong></td>
<td>Traverse left or right based on value comparison.</td>
<td>O(log N)</td>
<td>O(N)</td>
</tr>
<tr>
<td><strong>Insert</strong></td>
<td>Traverse to find the correct leaf position and link new node.</td>
<td>O(log N)</td>
<td>O(N)</td>
</tr>
<tr>
<td><strong>Delete</strong></td>
<td>Remove node and rearrange children (handles 3 cases: leaf, 1 child, 2 children).</td>
<td>O(log N)</td>
<td>O(N)</td>
</tr>
<tr>
<td><strong>Traversal</strong></td>
<td>In-order traversal visits nodes in sorted (ascending) order.</td>
<td>O(N)</td>
<td>O(N)</td>
</tr>
</tbody>
</table>

<hr>

<h2 id="bst-applications">5. Applications</h2>
<ul>
<li><strong>Sorted Data Storage:</strong> Facilitates fast lookup, addition, and removal of items.</li>
<li><strong>Dynamic Sorting:</strong> Keeping a running list of sorted numbers.</li>
<li><strong>Database Indexing:</strong> Used in database implementations (though B-Trees are more common for disk storage) to index records.</li>
<li><strong>Symbol Tables:</strong> Used in compilers to store variable names and their associated values.</li>
</ul>

<hr>

<h2 id="bst-issues">6. Issues & Limitations</h2>

<h3>The Skewed Tree Problem</h3>
<p>The primary issue with a standard BST is that its shape depends on the order of insertions. </p>
<ul>
<li><strong>Best Case:</strong> If data is inserted in random order, the tree remains relatively balanced. Height ≈ log N.</li>
<li><strong>Worst Case:</strong> If data is inserted in sorted or reverse-sorted order (e.g., 1, 2, 3, 4, 5), the tree becomes a linked list (skewed).</li>
</ul>

<p><strong>Consequence:</strong> The time complexity for Search, Insert, and Delete degrades from <strong>O(log N)</strong> to <strong>O(N)</strong>.</p>

<h3>Solution: Self-Balancing Trees</h3>
<p>To overcome this, we use self-balancing BSTs (like <strong>AVL Trees</strong> or <strong>Red-Black Trees</strong>) which automatically rotate nodes during insertion/deletion to maintain a height of log N.</p>

<hr>
