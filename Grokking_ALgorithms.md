# Grokking Algorithms

1.   Introduction to algorithms
-------------------------------
* Binary search is a lot faster than simple search.
* O(log n) is faster than O(n), but it gets a lot faster once the list of items you’re searching through grows.
* Algorithm speed isn’t measured in seconds.
* Algorithm times are measured in terms of growth of an algorithm.
* Algorithm times are written in Big O notation.


2. selection sort
-----------------

> ***Array != List***

### 2.1 Linked Lists

* Suppose you want to read the last item in a linked list. You can’t just read it, because you don’t know what address it’s at.
* Instead, you have to go to item #1 to get the address for item #2. Then you have to go to item #2 to get the address for item #3. And so on, until you get to the last item.
* _Linked lists are great if you’re going to read all the items one at a time;_ you can read one item, follow the address to the next item, and so on.
* But if you’re going to keep jumping around, linked lists are terrible.

### 2.2 Arrays

* Arrays are different. You know the address for every item in your array.
* For example, suppose your array contains five items, and you know it starts at address 00. What is the address of item #5? Simple math tells you: it’s 04.
* _Arrays are great if you want to read random elements_; because you can look up any element in your array instantly. With a linked list, the elements aren’t next to each other, so you can’t instantly calculate the position of the fifth element in memory.
