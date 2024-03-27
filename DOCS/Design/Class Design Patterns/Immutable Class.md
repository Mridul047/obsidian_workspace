
Once an object of an Immutable class  has been created then, user should not be able to alter the state of the object.


Rules :
* Make class as final.
* Make all fields as final.
* Setter methods should not be provided in the class.
* Create getter methods to get the object.
* Create custom constructor to initialize the fields in the class.
* If the class has-a reference variable or reference to a collection then:
	* perform deep-copy to initialize the reference variable or collection.
	* perform deep-copy before returning the variable in getter method.
