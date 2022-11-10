# Linked List & Array
- Array: Arrays store elements in contiguous memory locations, resulting in easily calculable addresses for the elements stored and this allows faster access to an element at a specific index.

- Linked List: Linked lists are less rigid in their storage structure and elements are usually not stored in contiguous locations, hence they need to be stored with additional tags giving a reference to the next element. 
## computer’s memory 
![memory](https://cdn-media-1.freecodecamp.org/images/uxNDqnrhHuS197WjrTeak8WQq2QZKAJD5xp4)
- o understand how they work, it’s very helpful to visualize your computer’s memory as a grid, just like the one below. Each piece of information is stored in one of those small elements (squares) that make the grid


- Arrays take advantage of this “grid” structure to store lists of related information in adjacent memory locations to guarantee extreme efficiency for finding those values.
 🔳🔳🔳🔳

You can think of arrays like this:

![memory](https://cdn-media-1.freecodecamp.org/images/HjKZtf6JKxcrH8t51iRrId-4lTqjOlGtICip)

##  Linked list provides the following two advantages over arrays:
- Dynamic size 
- Ease of insertion/deletion 
## Disadvantages of Linked Lists:
- Random access is not allowed. We have to access elements 
- sequentially starting from the first node. So we cannot do a binary search with linked lists. 
- Extra memory space for a pointer is required for each element of the list. 
- Arrays have a better cache locality that can make a pretty big difference in performance.
- It takes a lot of time in traversing and changing the pointers.
- It will be confusing when we work with pointers.

## Advantages of Arrays:
- Arrays store multiple data of similar types with the same name.
- It allows random access to elements.
- As the array is of fixed size and stored in contiguous memory locations there is no memory shortage or overflow.

- It is helpful to store any type of data with a fixed size.
- Since the elements in the array are stored at contiguous memory locations it is easy to iterate in this data structure and unit time is required to access an element if the index is known.

## Disadvantages of Arrays:
- The array is static in nature. Once the size of the array is declared then we can’t modify it.
- Insertion and deletion operations are difficult in an array as elements are stored in contiguous memory locations and the - shifting operations are costly.
- The number of elements that have to be stored in an array should be known in advance.
- Wastage of memory is the main problem in the array. If the array size is big the less allocation of memory leads to wastage of memory.
## references
- [freecodecamp](https://cdn-media-1.freecodecamp.org/images/uxNDqnrhHuS197WjrTeak8WQq2QZKAJD5xp4)
- [geeksforgeeks](https://www.geeksforgeeks.org/linked-list-vs-array/)
