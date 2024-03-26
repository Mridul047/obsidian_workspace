
Interface Segmentation Principle:
	Interface should be designed keeping in mind the children should NOT BE IMPLEMENT UNNECESSARY BEHAVIOUR THAT THEY DON'T NEED !
	
Single Responsibility Principle:
	Class should have ONLY 1 REASON TO CHANGE !

Open-Close Principle:
	Class should NOT BE MODIFIED but CAN BE EXTENDED !

Liskov-Substitution Principle:
	If ClassB is child of ClassA, then we should be able to replace ObjectA with ObjectB WITHOUT BREAKING THE BEHAVIOUR OF THE PROGRAM.
	 I.E : Child should add on to the capability of the parent & not narrow it down !
	 
Dependency Inversion Principle:
	Class should depend on Interface & not on concrete class. This helps in achieving loosely coupled code !