# Week 3 Assignment

### Problem 1:   Maximum Depth of Binary Tree

Given the root of a binary tree, return its maximum depth.

A binary tree's maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.

 ![](https://assets.leetcode.com/uploads/2020/11/26/tmp-tree.jpg)

**Example 1:**

```
Input: root = [3,9,20,null,null,15,7]
Output: 3
Example 2:

Input: root = [1,null,2]
Output: 2
```

**Constraints:**

 - The number of nodes in the tree is in the range [0, 104].
 - 100 <= Node.val <= 100



### Problem 2 : Validate a Binary Tree

Given the root of a binary tree, determine if it is a valid binary search tree (BST).

A valid BST is defined as follows:

The left subtree of a node contains only nodes with keys less than the node's key.
The right subtree of a node contains only nodes with keys greater than the node's key.
Both the left and right subtrees must also be binary search trees.
 

**Example 1:**

![](https://assets.leetcode.com/uploads/2020/12/01/tree1.jpg)
```
Input: root = [2,1,3]
Output: true
```

**Example 2:**

![](https://assets.leetcode.com/uploads/2020/12/01/tree2.jpg)
```
Input: root = [5,1,4,null,null,3,6]
Output: false
Explanation: The root node's value is 5 but its right child's value is 4.
``` 

**Constraints:**

- The number of nodes in the tree is in the range [1, 104].
- 2<sup>31</sup> <= Node.val <= 2<sup>31</sup> - 1


### Problem 3:   Binary Tree Level Order Traversal

Given the root of a binary tree, return the level order traversal of its nodes' values. (i.e., from left to right, level by level).

**Example 1:**

![example 1 image](https://assets.leetcode.com/uploads/2021/02/19/tree1.jpg)

```
Input: root = [3,9,20,null,null,15,7]
Output: [[3],[9,20],[15,7]]
```
**Example 2:**

```
Input: root = [1]
Output: [[1]]
```
**Example 3:**

```
Input: root = []
Output: []
 ```

**Constraints:**

- The number of nodes in the tree is in the range [0, 2000].
- -1000 <= Node.val <= 1000



### Problem 4: Find if Path Exists in Graph
There is a bi-directional graph with n vertices, where each vertex is labeled from 0 to n - 1 (inclusive). The edges in the graph are represented as a 2D integer array edges, where each edges[i] = [ui, vi] denotes a bi-directional edge between vertex ui and vertex vi. Every vertex pair is connected by at most one edge, and no vertex has an edge to itself.

You want to determine if there is a valid path that exists from vertex source to vertex destination.

Given edges and the integers n, source, and destination, return true if there is a valid path from source to destination, or false otherwise.

 

**Example 1:**

![](https://assets.leetcode.com/uploads/2021/08/14/validpath-ex1.png)
```
Input: n = 3, edges = [[0,1],[1,2],[2,0]], source = 0, destination = 2
Output: true
Explanation: There are two paths from vertex 0 to vertex 2:
- 0 → 1 → 2
- 0 → 2
```
**Example 2:**

![](https://assets.leetcode.com/uploads/2021/08/14/validpath-ex2.png)
```
Input: n = 6, edges = [[0,1],[0,2],[3,5],[5,4],[4,3]], source = 0, destination = 5
Output: false
Explanation: There is no path from vertex 0 to vertex 5.
```

**Constraints:**
- 1 <= n <= 2 * 105
- 0 <= edges.length <= 2 * 105
-  edges[i].length == 2
- 0 <= ui, vi <= n - 1
- ui != vi
- 0 <= source, destination <= n - 1
- There are no duplicate edges.
 -There are no self edges.


### Problem 4: Find the Town Judge
In a town, there are n people labeled from 1 to n. There is a rumor that one of these people is secretly the town judge.

If the town judge exists, then:
    1. The town judge trusts nobody.
    2. Everybody (except for the town judge) trusts the town judge.
    3. There is exactly one person that satisfies properties 1 and 2.
    
You are given an array trust where trust[i] = [ai, bi] representing that the person labeled ai trusts the person labeled bi.
Return the label of the town judge if the town judge exists and can be identified, or return -1 otherwise.

**Example 1:**
```
Input: n = 2, trust = [[1,2]]
Output: 2
```
**Example 2:**
```
Input: n = 3, trust = [[1,3],[2,3]]
Output: 3
```
**Example 3:**
```
Input: n = 3, trust = [[1,3],[2,3],[3,1]]
Output: -1
``` 

**Constraints:**
- 1 <= n <= 1000
- 0 <= trust.length <= 104
- trust[i].length == 2
- All the pairs of trust are unique.
- ai != bi
- 1 <= ai, bi <= n

### Problem 6: All Path from source to target

Given a directed acyclic graph (DAG) of n nodes labeled from 0 to n - 1, find all possible paths from node 0 to node n - 1 and return them in any order.

The graph is given as follows: graph[i] is a list of all nodes you can visit from node i (i.e., there is a directed edge from node i to node graph[i][j]).

**Example 1:**

![](https://assets.leetcode.com/uploads/2020/09/28/all_1.jpg)

```
Input: graph = [[1,2],[3],[3],[]]
Output: [[0,1,3],[0,2,3]]
Explanation: There are two paths: 0 -> 1 -> 3 and 0 -> 2 -> 3.
```
**Example 2:**

![](https://assets.leetcode.com/uploads/2020/09/28/all_2.jpg)

```
Input: graph = [[4,3,1],[3,2,4],[3],[4],[]]
Output: [[0,4],[0,3,4],[0,1,3,4],[0,1,2,3,4],[0,1,4]]
```
**Constraints:**
- n == graph.length
- 2 <= n <= 15
- 0 <= graph[i][j] < n
- graph[i][j] != i (i.e., there will be no self-loops).
- All the elements of graph[i] are unique.
- The input graph is guaranteed to be a DAG.
