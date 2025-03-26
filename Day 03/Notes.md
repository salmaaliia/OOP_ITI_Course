### Association 
- class A uses class B 
- week relation
- the time for this relation is little (till the function get destroyed)
```
        public void writeOnBoeard(Marker marker)
        {

        }
```

---
### Aggregation
- class A contain an object from class B
- the relation is for a longer time than for the association
```
	    Instructor instructor;

        public Room()
        {
            instructor = null;
        }
        public void instructorEntered(Instructor ins)
        {
            instructor = ins;
        }
```

---
### Composition
- class A consists of class B
- creation of one of them depends on the other
```
        head h;

        public humanBody()
        {
            h = new head();
        }
```

---
### Inheritance 
- private members in the ancestor cannot be accessed in any place 
- protected members can be accessed in the child but not by the object
- when you create an object from the child the compiler creates an object from the parent
- ``` base``` keyword is for the ancestors
- To choose the constructor that being called from the parent class we use base keyword
```       
		public human() : base()
        {
        }
```
