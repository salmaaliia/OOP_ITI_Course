
- All local variables --> stack 
- dynamic allocated variables (object) --> Heap
---
- Data Types
	- Values
		- struct --> int num;
		- enum
		-  store data 
	- Reference 
		- class
		- car c; --> ref not object 
		- ref stores address not data
		- new car(); --> object
		- car c = new car();  --> c is a reference that stores the address of the object
		- more than one ref can have the address of the same object
---
### For Local variables
- we cannot use any local variable before any initialization
- `Car c1 = null; c1.price = 1200;` --> runtime error not compiler error
- value types are non-nullable value types `int num = null` --> compiler error 
---
### For Member variables
- When we create new object --> all members of this object are going to be initialized with (0, false, null)
---
- passing ref type to a function --> passing by reference so any change will affect the object in the main
---
### For Member Function 
- the first parameter by default is a ref from the same class (hidden) and it name is `this`
- `public void Display(car this) {Console.WriteLine($"Price is {this.price}, Number is {this.number}");}` --> the compiler is the one which adds this keyword and if we added `car this` it will cause an error but writing `this.price` won’t cause an error but we do not need to add it.
---
### Constructor
- Does not have a return type
- Has the same class name
- Has a body 
- take parameters
- you can only call it while creating the object from the class
- The compiler creates a default constructor of we did not create a one
-  We cannot make an object without a constructor but the constructor does not create the object, you first create the object then call the constructor.
- for constructor chaining
```
        public point() : this(20, 10, 30)
        {

        }
        public point(int x, int y, int z)
        {
            this.x = x;
            this.y = y;
            this.z = z;

        }
```
