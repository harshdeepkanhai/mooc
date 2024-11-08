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
