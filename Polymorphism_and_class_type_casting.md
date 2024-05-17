# Polymorphism
Concept: the condition of occurring in several different forms. In **C++**, it is referring to the situation where serveral classes share the **same ancestor class** whose functions may
be **overriden** to provide **class-specific** functionalities.


When an **instance** of a class calls a method, whether it be virtual or non-virtual, the compiler is going to search for the method  through its ancestor tree starting from itself until the method definition is found.
The method found will be called.

When an **pointer** of a class calls a method, the behavior of calls depends on the types of methods called and the type of instance it is referencing.
When a non-virtual method is called, the method lookup starts from the static type of class of the pointer through its ancestor tree.
When a virtual method is called, the method lookup starts from the the class type of the isntance it points to through its ancestor tree.


## Summary:
When a **non-virtual method is called**, we look at the static type of the caller and if it is not there, check its ancestors until we find it.\
When a **virtual method is called**, we look at the underlying referenced object type and if it is not there, check its ancestors until we find it.
