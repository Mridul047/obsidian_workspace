Stack Memory:

* Store Temporary Variables and separate memory block for methods.
* Store Primitive data types 
* Store Reference of the heap objects
	* Strong reference
	* [Soft reference](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/lang/ref/WeakReference.html)
- Each thread has its own Stack memory.
- Variables within a SCOPE is only visible and as soon as any variable goes out of the SCOPE, it get deleted from the Stack (in LIFO order)
- When Stack memory goes full, its throws "java.lang.StackOverflowError"

Heap Memory:

- Store Objects.
- There is no order of allocating the memory.
- Heap memory is shared with all the threads.
- Heap also contains the String Pool.
- When Heap memory goes full, its throws "java.lang.OutofMemoryError"
- Heap memory is further divided into:
	- Young Generation (minor GC happens here)
		- Eden Space
		- Survivor Space ( S0 , S1 )
	* Old/Tenured Generation (major GC happens here)
* Garbage Collector is used to delete the unreferenced objects from the heap.
	- Mark and Sweep Algorithm
	- Types of GC:
		- Serial GC
		- Parallel GC
		- CMS (concurrent Mark Sweep)
		- G1
		- ZGC