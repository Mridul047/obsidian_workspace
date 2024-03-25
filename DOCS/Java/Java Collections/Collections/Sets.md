
## HashSet

* package : java.util
* Introduced in Java 1.2
* Implements Set directly
* Uses HashMap internally
* Properties of HashSet: 
	* HashSet is not index based DS. Values are stored based on hashCode value.
	* HashSet stores the value as a key inside the map. Thus hashSet doesn't store duplicate values.
	* HashSet doesn't follow  Insertion order.
	* HashSet doesn't follow  Sorting order.
	* HashSet is Non Synchronized i.e not thread safe.
## TreeSet

* package: java.util
* Introduced in Java 1.2
* Implements NavigableSet directly
* Uses NavigableMap ( implemented by TreeMap ) which is a Balanced Tree internally (Red black tree) 
* Properties of TreeSet
	* TreeSet is not index based DS.
	* TreeSet doesn't follow Insertion order.
	* TreeSet follows  Sorting order.
	* TreeSet returns values using following algo. Left-Root-Right i.e in-order traversal.
	* TreeSet can't store duplicate elements.
	* TreeSet is Non Synchronized i.e not thread safe.
	* TreeSet can't store null values.