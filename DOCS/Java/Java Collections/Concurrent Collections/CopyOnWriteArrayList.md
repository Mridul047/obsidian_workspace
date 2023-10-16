
Properties of COW.AL:
	1. Update operation creates a cloned copy of the arrayList
	2. Allows concurrent reads &  thread safe update operations
	3. Best suited for read operations & less write operations
	4. Insertion order is preserved
	5. Insertion of null value is possible
	6. Insertion of duplicate values is possible
	7. Iterator of COW.AL can't perform remove operation as compared to ArrayList
	8. Throws UnsupportedOperationException if remove operation is performed while using Iterator
	9. Doesn't throw ConcurrentModificationException