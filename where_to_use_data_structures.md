# Usage of Data Structures List, Tuple, Set, Dict, Stack and Queue
Following are some of the tips on when to use what data structure,
### 1. List
* To store collection of heterogeneous (different data types) elements.
* If we want the insertion order to be preserved.
* Can store duplicate elements.
* To extend or modify the collection or list dynamically.
### 2. Tuple
* To store collection of heterogeneous elements.
* When we want the insertion order to be preserved.
* Can store duplicate elements.
* Don’t want to modify the collection (tuple is immutable)
### 3. Set
* To store collection of heterogeneous elements.
* Insertion order can’t be preserved.
* Can’t store duplicate elements.
* Can extend or modify the collection.
* It offers O(1) time complexity for searching an item in this collection.
### 4. Dictionary
* To store collection of Key,Value Pairs
* Value can be Any Data type.
* Key can be integer or string or float.
* Insertion order can’t be preserved.
* can’t store duplicate keys.
* Can extend or modify the collection.
* If offers O(1) time complexity when searching for a Key in this collection.
### 5. Stack
* To append the element at the end of the list in O(1) time Complexity.
* To delete the element from the end of the list in O(1) time Complexity.
* We can implement the Stack in Python using **deque** Libray or **Lists** itself.
### 6. Queue
* To append the element at the element at the beginning (or) starting index of the list in O(1) Time Complexity.
* To delete the element from the begining of the list in O(1) Time Complexity.
* We can implement the Queue in Python using **deque** Library.
