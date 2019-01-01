# Data-Structures

This repository aims to review and implement popular data structures with python programming language (Version 3)

## Part 1 - Introduction - efficiency
**Efficiency**: In algorithms concept, It is also called **complexity**. It is how well you are using your computer resources to get a particular job done. We can think about it in terms of **space** (How much storage space needed?) and time (How long the code takes to run?).

The important tradeoff in algorithms complexity discussion:

1. Time Efficiency
2. Storage Space Efficiency

Open an algorithms&dataStructures book and study the complexity notations (It won't take much time) which we are going to use for explaining the algorithms complexity in this repository also,

This Part is Done!

## Part 2 - List-based Collection

The main work begins here. Be ready for coding and enjoying DataS and AD :)

We can review the list of the list-based data structures in following order:

1. **Arrays**
    (1) The most common implementation of the Lists
    (2) fixed length
    (3) hard to exploit
    (4) Messy Insertion and Deletion (index finiding for accesses - shiftings are needed by the programmer - order: O(n) -> very inefficient) 
2. **Linked Lists**: 
    (1) Insertion and Deletion is more easier and neater than Array - Order O(1) 
    (2) Each element has the next element (or even previous element in DLL (Doubled Linked List)) pointer
3. **Stacks**:
    (1) Push and Pop Operations are done by order of O(1)
    (2) We can use Linked List to implement a Stack by focusing on its head
    (3) Stack is know as LIFO (Last-In-First-Out) Structure
4. **Queues**:
    (1) It is a FIFO (First-In-First-Out) Structure
    (2) It is oposite of a stack
    (3) Head -> Oldest Element in the Queue, Tail -> Newest Element in the Queue
    (4) Enqueue -> Adding an Element to the tail
    (5) Dequeue -> Removing the Head Element
    (6) Peak Operation -> Viewing Head Element without changing it
    (7) It can be implemented by a Linked-List
    (8) Deque --> It is a double ended queue that goes both ways. We can enqueue and dequeue from either end. A Deque is a general version of both stacks and queues.
    (9) Priority Queue: Each element has a priority number when we insert them into the queue. When we are going to dequeue, element with maximum priority goes to be removed.

**Python list**
Python has an interesting data stucture called a "list" that is much more than a mere list. In fact, a Python list actually encompasses the functionality of almost every list-based data structure came above. 

**Linked List**
There is not a built-in data structure in python that look likes a linked list. but you can see how it is implemented in python v3 in [here](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season1_List_based_Collection/Linked-List/linked-list.py)

**Stack**
I want to make you happy that you don't need to implement the stack in the python because The Python has the stack functionality in built-in way. Python with `append()` and `pop()` functions does push and pop functionalities. You can find Stack implementation in python v3 [here](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season1_List_based_Collection/Stack/stack.py)

**Queue**
Be Happy! Python has a built-in class for Queues and the following example shows how to use python built-in queues. But we are going to implement it ourselves, you can view it [here](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season1_List_based_Collection/Queue/queue.py)

```python
import queue
q = queue.Queue()
for i in range(5):
    q.put(i)
while not q.empty():
    print(q.get())
```

Part 2 Finished! Let's go to the next Part :)

## Part 3 - Searching and Sorting
**Linear Search**
In this search method, we have to compare our key to all of the elements in the list one by one - **O(n)**

**Binary Search**
Requirement -> Our List has to be ordered -> So our sorting algorithm has effect on the total time complexity. -**max(O(log(n)), Sorting Method Time Complexity)**

Binary Search implementations code can be found here.[Iterative Implementation](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season2_search_sort/01-binary_search_iterative.py), [Recursive Implementation](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season2_search_sort/02-binary_search_recursive.py)

**Sorting**

**Bubble Sort**

Other name for this sorting algorithm -> **Sinking Sort**

It is a naive approach (Efficiency -> **O(n^2)**). It is an in-place sorting algorithm, space complexity is constant **O(1)**. In this algorithm we go through the list and comparing elements side by side and switching them on correct condition. This sorting algorithm python implementation can be found [here](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season2_search_sort/03-bubble_sort.py).

**Merge Sort**

It is a divide and conquer algorithm. It divides input array in two halves and then merges two halves. This sorting algorithm time complexity in three cases: best, average and worst is **O(nlogn)**. This sorting algorithm recurrence relation is **T(n)=2*T(n/2)+n**. This relation shows that in each step, merge sort divides the input array in 2 parts then merges that two sorted arrays in linear time. This is not a in-place sorting algorithm. It needs auxillary space from **O(n)** order. Merge sort implementation can be found [here](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season2_search_sort/04-merge_sort.py).

**Quick Sort**

This is one of the most efficient sorting algorithms. In this algorithm, in each step we choose an element as pivot and move other elements in regards to the value of the chosen pivot. we continue recursively picking pivots in lower and upper section and it is continued until the whole array is sorted.

This Sorting algorithm time complexity in three cases differs and this is what makes this algorithm an amazing one :D.

Best Case: **O(nlogn)**, Average Case: **O(nlogn)**, Worst Case:  **O(n^2)** -> occurs when we have reversed sorted input

This is an in-place sorting algorithm -> so space complexity is: **O(1)**

**Note**: The intersting thing about this sorting algorithm is that, we can avoid worst case by having a function which shuffles our input list. So we'll always have **O(nlogn)**. It is important to add that the coefficient of the nlogn in merge sort is bigger that quich sort, So if you are questioned about choosing between merge sort and quick sort, don't think or anything else, only choose quick sort. 

Quick sort implementation can be found [here](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season2_search_sort/05-quick_sort.py).

In Data Structures, It is enough for sorting algorithms, we saw their most popular ones. We will examine them more on Algorithms repository which you can go there by this [link](https://github.com/ehsanyousefzadehasl/Algorithms/).

## Part 4 - Hashing

**Set**

set is a data structures that the stored content in it do not have any order. The elements never duplicate in a set. It is exactly like a abstract set concept in mathematics.

**Map**

Map is a data structure consisted of tuples (2 elemented tuples) or we can show it in a better way like **Map=<key, value>**. If we look to the keys and values as lists, it is important to say that key list is a set. It means that in a Map we don't have duplicated key, but we may have same values for multiple keys. For a better view you can consider the map as a dictionary. It is implemented with dictionary keyword (**dict**) in python programming language.

Look at the Following exmaple:

```python
our_dictionary = dict()
our_dictionary['a'] = 1
our_dictionary['b'] = 2
our_dictionary['c'] = 3
our_dictionary['d'] = 4
our_dictionary['e'] = 5
our_dictionary['f'] = 6
our_dictionary['g'] = 7

print(our_dictionary)
# {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5, 'f': 6, 'g': 7}
```

Dictionaries are wonderfully flexible—you can store a wide variety of structures as values. You store another dictionary or a list. Look at the following example:

```python
our_dictionary = dict()
our_dictionary['a'] = [1]
our_dictionary['b'] = [2]
our_dictionary['c'] = [3]
our_dictionary['d'] = [4]
our_dictionary['b'].append(5)
our_dictionary['e'] = [6]
our_dictionary['f'] = [7]
our_dictionary['g'] = [8]
our_dictionary['h'] = [9]
our_dictionary['i'] = [10]
print(our_dictionary)
# {'a': [1], 'b': [2, 5], 'c': [3], 'd': [4], 'e': [6], 'f': [7], 'g': [8], 'h': [9], 'i':[10]}
```

There is a good solved exercise for playing with the dictionaries is [here](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season3_hashing/01-dict_example.py).

### Hashing

Now, if we want to find an element in our previously checked data structures - like list - except stack and priority queues, we have to linear time search. So, we like to get an ability to be able to search for and find each element constantly. Hash Functions help us to get this ability.

**Hash Functions**

Purpose of hash function: Transforming some value into one that can be stored and retrieved easily.

Hash function inputs some value, converts the value based on some formula and produces a coded version of the value that's often the index in an array.

**Collision Concept**

The collision occurs when a hash function produces the same hash value for two differrent inputs.

This problem can be solved by two methods:

1. Changing the value in the hash function or the hash function completely - **Requirement is a lot of space to store your values and totally effects the complexity in terms of both size and time**
2. Changing the structure of the hashed values array - instead of storing one hash value in each slot, store some type of lists that contains all values hashed at that spot -> These lists are generally called buckets in this context - **Requirement: Iteration through some collection**

Hash functions have a constant lookup time in the average case, but because of the bucket system, you could end up storing every value in one bucket and then you are essentially just iterating through a list. In that worst case this actually turns into O(m).

**Note:** There is no one perfect way to design a hash function. We have to be aware to nature of our data and choose the most appropriate one to our job.

**Good Idea:** Inside a large bucket we can use another hash function to split up those elements even more

**Emphasize:** There is No perfect way to design a hash function

**Load Factor:** This gives us a sense of how "full" a hash table is.

Load Factor = (Number of Entries - values wanna to hash) / (Number of Buckets)

**Note:** Load factor closer to 1 is better - when it is 1 meaning the number of values equals the number of buckets, the better it would be for us to rehash and add more buckets.

**Note:** Any table with a load value greater than 1 is guaranteed to have collisions.

### Hash Map
Hash maps are one the main places that we can see hash functions show up. A Python dictionary is a hash map.
There is a good example which is implemented in Python and you can see it [here](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season3_hashing/02-String_Keys_Practice.py). This example has written a hash table and hash function that uses string keys. This hash table stores strings in buckets by their first two letters, according to the following formula:

Hash Value = (ASCII Value of First Letter * 100) + ASCII Value of Second Letter 

You can see the Python function ord() which goes to get the ASCII value of a letter, and chr() to get the letter associated with an ASCII value. You see that there is a HashTable class and methods to store and lookup values, and a helper function to calculate a hash value given a string.

## Part 5 - Trees
For understanding this part, first you need to be familiar with graph theory and tree concept from discrete structures course but we are going to shortly review some important concepts. 
**Tree**: is really an extension of linked list. In a linked list, each element points only to next element (we consider it a horizontal structure) but in a tree each element can point to some elements (we consider it a vertical structure).

For trees, we have 2 kinds (1) Connected - all nodes are connected to each other - (2) Unconnected -there are two nodes that there is not any path from them to each other-.

**A cycle in a tree**: occurs when on a path we encounter a node twice.

**Level of a node**: in a Tree is the number of connection which should has been taken to reach the root plus 1.

**Child and parent terminology**: The node with higher level is the child of the node with that level minus 1. Note that in a tree, a node may have both child and parent roles. The node with lowest level is **Ancestor** and the with highest level is Descendant.

**Leaf**: The node in a tree which has not any child. It's other name is **external node**. The nodes other than leaves are called **Internal Leaves**.

**Height of a node**: is the number of edges between the node and the furthest leaves. The height of a tree is equal to the height of the root. (Height of a leaf is zero)

**Depth of a node**: is the number of edges between the root and the node.

### Tree Traversal

Tree is not a linear data structure like a list, so there is no clear way to traverse through every element. The tree traverse is important because without visiting all elements, searching and sorintg the elements can not be correctly done. There are two broad ways to traverse trees: **DFS (Depth First Search)**, **BFS (Breadth First Search)**

#### DFS (Depth First Search)
DFS is a recursive concept which there is a child to visited go inside and repeat it. There are several approaches to DFS a tree: (1) **Pre-order** -> We check off a node as we see it in this approach. (2) **In-order** -> We check off a node when we have checked off its left child. (3) **Post-order** -> We check off a node when we have checked off its left and right child.

#### BFS (Breadth First Search)
BFS is a level order traverse which all nodes in a same level are visited then movement to higher level occurs.

### Binary Trees
Binary trees are trees that parents have at most 2 children. 

Searching for an element on a tree with **n** number of elements is from **O(n)** time complexity, because we traverse the tree in a linear way and there is no relation between the parent and its children values. 

Deleting an element from a binary tree has **O(n)** time complexity because search operation and some additional shift operations are needed to have a connected tree.

Inserting an element to a binary tree has **O(height of the tree)** time complexity, because in the worst case, we have to move equal to the height of the binary tree. In a perfect binary tree in level **L** we have **(2 ^ (L - 1))** nodes, so the insertion complexity is **O(log(n))**.

You can find a implementation of a BT (Binary Tree) [here](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season4_tree/01_binary_tree.py).

### Binary Search Tree (BST)
BST is a binary tree (We add a more rule to binary trees and name them Binary Search Trees) that for any node on it, the node's value is smaller than its right child's value and larger than its left child's value. This tree is good for doing search operation. If BST be a balanced tree, the search complexity is **O(log(n))** - we consider it common case -. In the worst case our BST will be an unbalanced binary tree like a chain, in this situation the complexity will be **O(n)**. You can find a BST implementation [here](https://github.com/ehsanyousefzadehasl/Data-Structures/blob/master/season4_tree/02_BST.py).

### Heaps
Heap is another specific type of tree with its own rules. In a heap elements are arranged in a increasing or decreasing order such that the root element is either the maximum element or the minimum element of the tree. There are two different types of heaps: (1) **Max Heaps** - a parent always has a value larger than its children values and the root value the maximum number of the tree - (2) **Min Heaps** - a parent always has a value smaller than its children values and the root value the minimum number of the tree

**Note**: Heaps don't need to be a binary tree.

**Heaps Time Complexity Analysis**: in a max/ min heap, finding max/ min element is done by **O(1)** complexity. Searching for an element complexity is **O(n)**.

**Heapify**: is the operation which in we reorder the elements based on the **heap**.

**Extract**: is the operation of elimination the root and bringing the rightest last level leaf to the root and Heapifying the tree.

**Note**: The time complexity of **Extract** operation is **O(log(n))** because we may swip the root to the number equal to height of the tree.

**Note**: Every sorted array can be shown as a **heap**.

**Note**: If we receive a series of number one after another, we can put them in a suitable heap then we'll be able to create a increasing/ decreasing list of the given numbers.

### Self Balancing Trees
The tree that minimizes the number of levels that it uses. There are some algorithms with insertion and deletion to keep it balanced and nodes themselves might have additional properties. The most common example of these trees is **Red-Black** tree which is **an extension of BST**. In red-black trees, the nodes have one additional property, **color**. All leaf nodes must be colored black. If a node is red, both of its children must be black. The rule which is optional is that the color of the root must be black. Every path from a node to its descendant null nodes must contain the same number of black nodes. These rules guarantee that the tree will change to a unbalanced tree.

## Part 6 - Graphs
