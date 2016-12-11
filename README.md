HeapsJava
==

This repository aims at defining a data structure called heap. Insertion, deletion and element extraction (which includes data
reorganization) in heaps are done in O(log n) time.

A min-heap is a heap where the element with the lowest key can be extracted in constant time (data reorganization will take
O(log n) time). For a max-heap, the element with the highest key will be retrieved. For instance, for a min-heap:

- Elements with keys 1,5,8 and 3 are inserted in this order.
- The first extract-min run returns the element with key = 1
- The second returns the element with key = 3
- The third returns the element with key = 5
- The fourth returns the element with key = 8

And for a max-heap:  

- Elements with keys 1,5,8 and 3 are inserted.
- The first extract-max run returns the element with key = 8
- The second returns the element with key = 5
- The third returns the element with key = 3
- The fourth returns the element with key = 1

***

### The HeapElement class

A heap element includes:
- a key which will compare it to other elements
- an optional object whose purpose is to carry extra information the user sees suitable.

The getInfo() method returns the additional info object.

***

### The Heap interface

It includes both insertion (insertElement()) and deletion (deleteElement()) methods, as well as the getElement() method which
retrieves the min element in a min-heap and the max element in a max-heap, or throws an ad hoc exception if heap is empty (the
EmptyHeapException).
