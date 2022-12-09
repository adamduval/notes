# Python

## Inbox

- self

---

## Log

---

## Notes

### dictionary

- built in data type

#### dictionary.get()

- get(key, value)
- returns the dictionary value for the specified key
- if the key is not found it returns the specified value
- if there is no value specified it returns None

### list

- built in data type
- ordered, mutable, heterogeneous, allows duplicates

#### list.sort()

- the sort method for the list class
- modifies the values of the list in place
- does not return anything

### Enum

- class from enum library
- set of symbolic members bound to unique constant values
- can be iterated to return members
- members are hashable and can be used as keys in a dictionary or elements of a set

### enumerate()

- built in method
- adds a counter to an iterable and returns the enumerated object

```Python
enumerate(iterable, start=0)
# iterable: sequence that supports iteration
# start: optional, where the index starts counting from
```

### sorted()

- a built in function to sort an iterable
- returns the sorted iterable

### set

- built in data type
- unordered, unchangeable and do not allow duplicate values

### string

- built in data type
- string are immutable
- an array of unique characters
- python does not have characters, a character is a string with a length of one

### dunder variables

- also called attributes
- used to convey information about a python program or to a program
- `__doc__` stores docstring information
- `__name__` stores the names of classes, modules and functions

[Python Morsels:](https://www.pythonmorsels.com/dunder-variables/#:~:text=Dunder%20variables%201%20Dunder%20variables%20convey%20information%20Python,variables%2C%20attributes%2C%20and%20methods%20have%20two%20purposes%3A%20)  

> Classes use these dunder attributes:  
>`__name__`: stores their name  
>`__dict__`: stores their attributes (see where attributes are stored)  
>`__module__`: stores the name of the module they were defined in within  
>`__bases__`: stores their base classes (see inheritance)  
>`__mro__`: stores their method resolution order  
>
>Functions use these dunder attributes:  
>`__name__`: stores their name  
>`__dict__`: stores their attributes  
>`__module__`: stores the name of the module they were defined in within  
>`__defaults__` and `__kwdefaults__`: store their default argument values  
>
>Modules use these dunder attributes:  
>`__name__`: stores their name  
>`__dict__`: stores their attributes  
>`__file__`: the file this module was loaded from (though some modules are missing this)  
>
>All objects use these dunder attributes:  
>`__class__`: stores the class of the object attribute  
>`__dict__`: stores their attributes (well, usually)  

`__name__` for modules

- is assigned depending on how it's containing script is executed
- when a script is run directly python sets the `__name__` variable to `__main__`
- if a module is imported then the `__name__` variable is set to the name of the module

### **kwargs

- a magic variable
- allows you to pass in an unspecified number of keyword arguments to a function

---

## END

---
