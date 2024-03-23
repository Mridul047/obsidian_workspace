Stack Memory:

* Store Temporary Variables and separate memory block for methods.
* Store Primitive data types 
* Store Reference of the heap objects
	Strong reference
	Soft reference
- Each thread has its own Stack memory.
- Variables within a SCOPE is only visible and as soon as any variable goes out of the SCOPE, it get deleted from the Stack (in LIFO order)
- When Stack memory goes full, its throws "java.lang.StackOverflowError"