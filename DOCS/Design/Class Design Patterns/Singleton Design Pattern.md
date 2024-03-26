
This pattern states that Singleton class can have only 1 object instantiated throughout the application life cycle !

Rules :
* Create private static field to store reference of the class !
* Make constructor as private !
* Create public static method to get reference of the class !
* Implement double check locking for thread safe singleton class !


```java
// Java Program to write double checked locking 
// of Singleton class 

class Singleton { 
	private volatile static Singleton instance; 

	private Singleton() {} 

	// 1st version: creates multiple instances if two thread 
	// access this method simultaneously 
	public static Singleton getInstance1() 
	{ 
		if (instance == null) { 
			instance = new Singleton(); 
		} 

		return instance; 
	} 

	// 2nd version : this is thread-safe and only 
	// creates one instance of Singleton on concurrent 
	// environment but it is unnecessarily expensive due to 
	// cost of synchronization at every call. 
	public static synchronized Singleton getInstance2() 
	{ 
		if (instance == null) { 
			instance = new Singleton(); 
		} 
		return instance; 
	} 

	// 3rd version : An implementation of double checked 
	// locking of Singleton. Intention is to reduce cost 
	// of synchronization and improve performance, by only 
	// locking critical section of code, the code which 
	// creates instance of Singleton class. 
	public static Singleton getInstance3() 
	{ 
		if (instance == null) { 
			synchronized (Singleton.class) 
			{ 
				if (instance == null) { 
					instance = new Singleton(); 
				} 
			} 
		} 
		return instance; 
	} 
}

```


```java
// Breaking Singleton using reflection API

Singleton s1 = Singleton.getInstance3();

Constructor<Singleton> constructor = Singleton.class
.getDeclaredConstructor();

constructor.setAccessible(flag:true);

Singleton s2 = constructor.newInstance();

// Both objects will have unique hashcode
System.out.println(s1.hashCode()); 
System.out.println(s2.hashCode());
```


```java
// Final Implementation

class Singleton { 
	private volatile static Singleton instance; 

	private Singleton() {
		if(instance != null){
			throw new RuntimeException("Using Reflection to call private constructor is prohibited !");
		}
	} 

	// 1st version: creates multiple instances if two thread 
	// access this method simultaneously 
	public static Singleton getInstance1() 
	{ 
		if (instance == null) { 
			instance = new Singleton(); 
		} 

		return instance; 
	} 

	// 2nd version : this is thread-safe and only 
	// creates one instance of Singleton on concurrent 
	// environment but it is unnecessarily expensive due to 
	// cost of synchronization at every call. 
	public static synchronized Singleton getInstance2() 
	{ 
		if (instance == null) { 
			instance = new Singleton(); 
		} 
		return instance; 
	} 

	// 3rd version : An implementation of double checked 
	// locking of Singleton. Intention is to reduce cost 
	// of synchronization and improve performance, by only 
	// locking critical section of code, the code which 
	// creates instance of Singleton class. 
	public static Singleton getInstance3() 
	{ 
		if (instance == null) { 
			synchronized (Singleton.class) 
			{ 
				if (instance == null) { 
					instance = new Singleton(); 
				} 
			} 
		} 
		return instance; 
	} 
}

```