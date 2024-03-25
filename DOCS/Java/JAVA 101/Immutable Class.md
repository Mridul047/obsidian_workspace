
An class  is said to be immutable if the it's object can't be modified after it has been created.
Example: String objects are immutable in nature.

Rules to make Immutable Class:
* Declare the class as final so it can't be extended.
* Make all of the fields private so that direct access is not allowed.
* Don't provide setter methods for variables.
* Make all mutable fields final so that a field's value can be assigned only once.
* Initialize all fields using a constructor method performing deep copy.
* Perform deep copy in getter of mutable fields.