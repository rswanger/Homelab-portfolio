In Python, **methods** are ==functions that "belong" to a specific object or class==. Unlike independent functions, methods are called on an object using "dot notation" (e.g., `object.method()`) and often act upon the data contained within that object. 



In Python, there are three primary types of methods used within classes: ==**Instance methods**, **Class methods**, and **Static methods**==. [[1](https://realpython.com/instance-class-and-static-methods-demystified/), [2](https://www.geeksforgeeks.org/python/class-method-vs-static-method-vs-instance-method-in-python/)]

1. Instance Methods

These are the most common type of methods. They are used to access or modify the state of a specific object (an "instance"). [[1](https://realpython.com/courses/python-method-types/), [2](https://realpython.com/python-classes/), [3](https://realpython.com/instance-class-and-static-methods-demystified/)]

- **Key Feature**: They take `self` as the first parameter, which points to the specific instance of the class.
- **Usage**: Used for operations that require data unique to a single object.
- **Example**: `def my_method(self):` [[1](https://softwareengineering.stackexchange.com/questions/306092/what-are-class-methods-and-instance-methods-in-python), [2](https://www.youtube.com/watch?v=FLh-gbWoEZc), [3](https://dev.to/harshm03/python-classes-and-objects-4d53), [4](https://realpython.com/instance-class-and-static-methods-demystified/)]

2. Class Methods

These methods are bound to the class itself rather than a specific object. They can modify the state of the class that applies across all instances. [[1](https://www.youtube.com/watch?v=g-qRKZD3FgE), [2](https://www.tutorialspoint.com/python/python_class_methods.htm), [3](https://labex.io/tutorials/python-how-to-effectively-use-class-methods-in-python-398183)]

- **Key Feature**: They use the `@classmethod` decorator and take `cls` as the first parameter, which refers to the class.
- **Usage**: Often used as "factory methods" to create class instances or to change class-level variables.
- **Example**:
    
    python
    
    ```
    @classmethod
    def my_class_method(cls):
        pass
    ```
    
    Use code with caution.
    
    [[1](https://realpython.com/instance-class-and-static-methods-demystified/), [2](https://python.plainenglish.io/python-class-methods-understanding-the-roles-of-staticmethod-and-classmethod-c87d7db870f6), [3](https://www.youtube.com/watch?v=g-qRKZD3FgE), [4](https://www.youtube.com/watch?v=FLh-gbWoEZc)]

3. Static Methods

Static methods are like regular functions that happen to live inside a class. They do not have access to either the instance (`self`) or the class (`cls`). [[1](https://www.youtube.com/watch?v=PIKiHq1O9HQ&t=179), [2](https://blog.teclado.com/python-methods-instance-static-class/), [3](https://realpython.com/courses/python-method-types/)]

- **Key Feature**: They use the `@staticmethod` decorator and take no mandatory first argument.
- **Usage**: Used for utility or helper functions that logically belong to the class but don't need to change its state.
- **Example**:
    
    python
    
    ```
    @staticmethod
    def my_static_method():
        pass
    ```
    
    Use code with caution.
    
    [[1](https://blog.teclado.com/python-methods-instance-static-class/), [2](https://medium.com/python-for-everything/class-methods-in-python-made-easy-for-beginners-e7eef6e584e0), [3](https://www.youtube.com/watch?v=PIKiHq1O9HQ&t=179), [4](https://realpython.com/courses/python-method-types/), [5](https://www.youtube.com/watch?v=FLh-gbWoEZc)]

Comparison Summary

|Feature [[1](https://docs.python.org/3/library/functions.html), [2](https://realpython.com/courses/python-method-types/), [3](https://realpython.com/instance-class-and-static-methods-demystified/)]|Instance Method|Class Method|Static Method|
|---|---|---|---|
|**Decorator**|None|`@classmethod`|`@staticmethod`|
|**First Argument**|`self` (the instance)|`cls` (the class)|None|
|**Access**|Can access instance & class|Can access class only|Neither|
|**Purpose**|Object-specific behavior|Class-level operations|General utility|

For further reading on object-oriented programming concepts in Python, you can explore the [Real Python guide to OOP](https://realpython.com/python3-object-oriented-programming/) or the official [Python documentation on built-in types](https://docs.python.org/3/library/stdtypes.html). [[1](https://realpython.com/python3-object-oriented-programming/), [2](https://docs.python.org/3/library/stdtypes.html)]

[[Strings]]
