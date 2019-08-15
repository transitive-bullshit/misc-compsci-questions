# Misc CompSci Questions

## Problem 1

Given an undirected graph represented as an edge list of integer nodes, write a function that returns an array containing each connected subgraph.

```js
/*
// example 1
const input = [
  [ 1, 3 ],
  [ 2, 7 ],
  [ 1, 4 ],
  [ 3, 4 ],
  [ 6, 2 ]
]

// => [ [ 1, 3, 4 ], [ 2, 6, 7 ] ]

// example 2
const input = [
  [ 0, 10 ],
  [ 1, 6 ],
  [ 3, 4 ],
  [ 2, 8 ],
  [ 4, 5 ],
  [ 0, 3 ],
  [ 8, 9 ],
]

// => [ [ 0, 3, 4, 5, 10 ], [ 1, 6 ], [ 2, 8, 9 ] ]
*/
```

## Problem 2

Implement a recursive function called `increment(number)` that takes in a stack of 0’s and 1’s representing a binary number `k`, and returns another stack representing the binary number `k + 1`.

Examples:
  - `increment([1,0,0,0]) → [1,0,0,1]`
  - `increment([1]) → [1,0]`
  - `increment([0,0,1]) → [0,1,0]`

## Problem 3

Given a phonebook that contains an array of `[ name, number ]` pairs sorted alphabetically ascending by name, write a function to return the number for a given name or `undefined` if it doesn't exist.

## Problem 4

Suppose a curriculum consists of n courses, all mandatory, all of them lasting one semester, and all of them offered every semester (i.e. the limit does not exist). The prerequisite structure of the curriculum can be organized in a graph, where each node is a course, and there’s a directed edge from node A to node B if and only if A is a prerequisite for B. (Note that if A is a prereq for B and B for C, then that implicitly makes A a prereq for C. The arrow from A to C may or may not be included in the graph.) A course may have any number of prerequisites.

Write pseudocode for an algorithm that computes the minimum number of semesters needed to complete the curriculum. (You may take any
number of courses in each semester). The run time of your algorithm should be O(|V| + |E|) where V = number of vertices and E = number of edges.

## Problem 5

The proof of Dijkstra’s algorithm relies on all the weights being non-negative.  Consider the following algorithm for computing shortest paths in the presence of negative weights.

Let m be the weight of the most negative (i.e., smallest) edge.  Add |m| to the weight of each edge, thus making all weights non-negative. Now use Dijkstra’s algorithm to find the shortest path. Does this work? Explain why, or give a counterexample.

## Problem 6

Consider the problem of finding the length of the **longest** path from a vertex s to a vertex t in a directed acyclic graph `G = (V, E)` with edge-weights `w`.

- Student A thinks that they can solve this problem using an altered Dijkstra’s Algorithm that stores the maximum cost of each node and uses a maximum cost priority queue (a priority queue that returns the maximum value instead of the minimum value). Why would this **not** work?
- Describe and write pseudocode for an algorithm that would work. If there exists no path between s and t, then return ∞.

## Problem 7

You are given a non-empty stack S of integers. Write pseudocode for a method that sorts the stack in ascending order from the bottom-up (i.e. the bottom element is the smallest integer). You are allowed to use the push() , pop(), peek(), isEmpty() methods of a stack. You may use another stack in order to solve this problem, but you may not use other data structures in your solution.

Hint: You can accomplish this by creating one more stack in your method, and transfer elements into the new stack each time checking that the transfer doesn’t violate the sort order.

Example: Here’s a stack S
```
— 5 —
— 2 —
— 3 —
— 1 —
— 4 —
```

Your method should return a stack that looks like this:

```
— 5 —
— 4 —
— 3 —
— 2 —
— 1 —
```

## Problem 8

Given a binary search tree, design an algorithm which creates a linked list of all the nodes at each depth. For example, if you have a tree with depth D, you’ll have D linked lists. Your function should take in the root of the BST (which has pointers to any child nodes it may have), and return an array of linked lists.

## Problem 9

Design an algorithm and write code to find the first (farthest from the root) common ancestor of two nodes in a binary tree. Avoid storing additional nodes in a data structure.

Note: This is not necessarily a binary search tree.

## Problem 10

Design a data structure that stores integers and efficiently implements these methods:

- `insert(n)`
- `remove(n)`
- `getMedian()`

Don't code your solution, just describe a few possible ways of creating such a data structure and their corresponding big-O runtimes for each of these methods in terms of n.
