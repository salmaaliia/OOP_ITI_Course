### Polymorphism 
- we can see an object as a part of different classes. we can see Ahmed as an object of class human and also class creature.
```

            human h = new human();

            Creature c = new human();
```
- ينفع نشاور على ال child class ب ريفرينس من ال parent بس مينفعش العادي
- بيتعامل مع ال object على حسب نوع ال ref
- if there are 2 move functions one in human class and the other in creature class, calling move by ```c``` will call the function from creature. If we need to call the move function from human we need 2 steps 
	- give permission from creature using virtual keyword
	- override the function in human class using override keyword
```
// in creture class
        public virtual void move()
        {
            Console.WriteLine("Creature is moving...");

        }
```

```
// in human class
        public override void move() 
        {
            Console.WriteLine("Human is moving...");
        }
```

- virtual keyword makes the compiler search for the override function if it does not exist (the keyword override or the function itself) the creature move function will be the one to execute.

```
        static void moveCreature(Creature c)
        {
            c.move();
            //
            //
            //
        }
```
- All creature objects and all its children can use this function and passing any children object wont cause any issues because the parent ref can store the address of its child. If any child override the move function its function will be the one to get executed.
- 

