## Static Members
- functions that are not related to each object of the class but it is related to the class itself.
- ex:
```public static int fact(int num)```
- The function 'fact' returns the same thing for any object so we made it static and now we have to call it using the class name not the object
```int x = mathHealper.fact(5);```  // ```mathHealper``` is the class 

- The same for variables as if we had a class employee and we want a variable to dtore the number of employees.

- Static functions cannot see or deal with any member unless if this member is also static but the non-static functions can deal with static members.
- In the static member functions there is no ```this``` because there is no object that we call the function with
--- 
## Operator overload 
For arithmetic & logical operators, implicit and explicit 

- We have to make it static so the one how calls the function is the class itself not any object from the parameters.
#### To overload an arithmetic operator 
```
public static complex operator+(complex c1, complex c2) {
//the code to add 2 obejects of this class}
```
- The functions takes any type of parameters so we can 
```public static complex operator +(complex c1, int num)```
- To use the first operator 
``` complex c3 = c1 + c2;```
- To use the second operator 
``` complex c3 = c1 + 5;```

#### To overload a logical operator 
- If overloaded the logical operator == you have to overload != as well
```
        public static bool operator==(complex c1, complex c2)
        {
            return c1.real == c2.real && c1.img == c2.img;
        }
        public static bool operator!=(complex c1, complex c2)
        {
            return c1.real != c2.real || c1.img != c2.img;
        }
```
#### To overload implicit and explicit 
```
        public static implicit operator complex(int num)
        {
            return new complex(num, num);
        }

        public static explicit operator int(complex c)
        {
            return c.real;
        }
```
###### To use them 
```
            int num = (int)c1; // explicit casting
            complex c = 5; // implicit casting
```

- if we have operator to implicit cast from int to complex and an addition overload function that takes two objects c1 and c2, we can add c1 to and integer directly (will implicitly cast the int to complex)
```complex c2 = c1 + 5;```

- Some operators cannot be overloaded 
- postfix and prefix c1++ & ++c1 can be overloaded in the same function





