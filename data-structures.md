# Data Structures

## Inbox

- array lists
- heaps
- hash tables
- vectors
- matrices

---

## Log

---

## Notes

### data structures

- can be linear or non linear
  - linear
    - elements are arranged sequentially, elements are attached to their previous and next elements
    - can be static or dynamic
      - linear / static
        - static structures have a fix memory size
        - cannot be altered during runtime, but easier to access
        - array
      - linear / dynamic
        - not a fixed size
        - can be updated while program is running
        - queue
        - stack
        - linked list
  - non linear
    - elements are not arrange sequentially
    - cannot traverse all elements in a single run
    - tree
    - graph

### arrays

- a structure of fixed size
- holds items of the same data type
- can store complex data with nD arrays
- items are indexed
- being indexed allows random access
- operations
  - traverse, go through the elements
  - reverse
  - search, find an element by value of index
  - update, updated an element by index
  - ! insert / delete cannot be done in a straightforward manner because of fixed size, a new array must be created
- applications
  - building block for other structures
  - algorithms
    - insertion sort
    - quick sort
    - bubble sort
    - merge sort

### linked list

- a sequence of items in a linear order linked together
- must access data sequentially, random access not possible
- elements in a list are known as nodes
- each node contains a key and a pointer to the next node, known as `next`
- the `head` of the list points to the first node
- the last element is known as the `tail`
- various types:
  - singly linked list
    - single direction list (points one way)
    - null at the end
  - doubly linked list
    - double direction pointers, contains an extra `previous` pointer which points to the previous node
    - null at the end
  - circular linked list
    - the first node and last node are connected
    - one direction, but no null at the end
  - circular doubly linked lists
    - combination of the two above
- can perform various types of operations: traversal, insertion, sort, deletion,  search

### stack

- a stack is last in first out structure, it is linear
- elements placed into the structure last can be accessed first
- like a stack of dinner plates or pancakes
- two typical stack operations are push and pop
  - push is inserting an element to the top of the stack
  - pop is removing the top element from a stack

### queue

- first in first out data structure, it is linear
- the element which was placed in first can be accessed first
- all additions are made at one end while all deletions are made at the other end
- two typical queue operations are enqueue and dequeue
  - enqueue is adding an element to the end of the queue
  - dequeue is to delete the element from the beginning of the queue

---

## END

---
