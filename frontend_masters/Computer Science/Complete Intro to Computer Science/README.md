https://btholt.github.io/complete-intro-to-computer-science/intro/

https://www.frontendhappyhour.com/

## Iterative Sorts

### Bubble Sort

- Stable
- Destructive
- Best Complexity: O(n)
- Average Complexity: O(n^2)
- Worst Complexity: O(n^2)
- Space Complexity: O(1)

### Insertion Sort

- Better than Bubble Sorted
- Mostly sorted list are best
- Stable
- Destructive
- Best Complexity: O(n)
- Average Complexity: O(n^2)
- Worst Complexity: O(n^2)
- Space Complexity: O(1)

## Recursive Sorts

https://www.scheme.org/

### Recursion

- base condition
- sometime iterative is faster than recusrive

### Nested Addition

### Factorial

### Merge Sort

<!-- - Stable -->
<!-- - Destructive -->

- Divide and Conquer
- Best Complexity: O(nlogn)
- Average Complexity: O(nlogn)
- Worst Complexity: O(nlogn)
- Space Complexity: O(n)

### Quick Sort

- Non Stable
- Divide and Conquer
- Non-Destructive / Destructive
- Best Complexity: O(nlogn)
- Average Complexity: O(n^2)
- Worst Complexity: O(n^2)
- Space Complexity: O(logn) Destructive
- Space Complexity: O(n) Non Destructive
- Variations: quicksort3

## Non-Comparison Sort

### Radix Sort

- use method called bucketing
- Big O: O(n \_ k)
- Space Complexity: O(n + k)

## Binary Search

- works on sorted array
- Big O: O(log n)
- Space Complexity: O(1)

## Lists

### ArrayList

- replace and lookup: O(1)
- deletion, insertion: O(n)

### LinkedList

- lookup: O(n)
- deletion, Insertionition: O(1)
- variation: doublyLinkedList has head and tail
- never implemented in JS, but in C/C++ more

## Trees

### Binary Search Tree

- Always sorted
- Best Case Scenario: Root: O(1)
- Worst Case Scenario: O(n)
- Add Elements to array
- Delete Elements to array
- Lookup Best for Searchability: O(log n)
- Used in Database indexes, MongoDB

### Self Balancing AVL Trees

- Everything same as BST except adding it will balance itself
- Single Rotation
- Uses Recursive Add
- Double Rotation
- Database Indexes is a good use of this
- ALso there are Red/Black Trees

https://visualgo.net/en/bst?mode=AVL

### Depth First Tree Traversals

- preorder traversal
- inorder traversal (Good for traversing BST)
- postorder traversal
- Recursive

### Breadth First Tree Traversals

- uses a queue
- Traverses Height Wise
- Iterative(Mostly Used) or Recursive
- Find nearest to Height
- Used for PathFinding

### Heap Sort

- usually Heap is an array that represents a tree like data structure
- used to represent a priority queue
- binary heap is an array whereas BST is made up of Node
- All the numbers underneath the node are smaller in a binary heap
- Inorder traversal in binary heap doesn't give a sorted array
- Binary Heap is a complete binary tree
- Comes into two flavors:
  - Max Heap : Used for sorting numbers
  - Min Heap: Used for reverse sorting
- Max Heap: The top node is the largest number in the heap
- The way to represent a binary tree as an array is that for any index of an array n, its leff child is stored at 2n+1 and its right child is at 2n+2. The root node will always be 0.
- Heapify: Move the child node above and so on
- Space Complexity: O(1)
- Worst Case Time Complexity: O(n log n)
- Use case of Heap Sort: where memory is concerned, where array is already sorted use Insertion Sort

https://www.bigocheatsheet.com/

## Applying Tree algorithms

### Graphs

- Like Tree but no Hierarchy
- Edge describes a relationship
- Neo4J uses Graph Database
- Can be Bidirectional or Unidirectional
- Can use Depth First Traversal or Breadth First Traversal on it
- Complexity: Depends on Degree of Separation

https://neo4j.com/

https://frontendmasters.com/courses/databases/

### Pathfinding

- Djikstra Algorithm (https://stackoverflow.com/questions/25449781/what-is-difference-between-bfs-and-dijkstras-algorithms-when-looking-for-shorte)

https://qiao.github.io/PathFinding.js/visual/

-
