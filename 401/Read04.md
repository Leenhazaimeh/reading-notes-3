# Classes and Objects
- Objects are an encapsulation of variables and functions into a single entity that get them from classes but classes are most like template or a blueprint to create your objects

Example:
``
    class MyClass: variable = "blah"

    def function(self): print("This is a message inside the class.")

    myobject = MyClass()
``


- you can create as many objects as you want from the class as long as you assigning the object and for the class call, you can access the variables inside the object using dot notation , and thats for functions as well with the call (): 

```
    myobject.variable
```



# Thinking Recursively in Python

- Recursive function : a function that calls itself directly or indirectly which in most cases seems to work as a loop , and of its functionality is to divide the problem into simpler parts until it becomes straightforward move which calls base cases (no more subdivisions)

## Fixtures:

- fixtures are different than global variables , and cas be accessed by calling their names inside the test's parameters list ,you define fixtures using a combination of the pytest.fixture decorator, along with a function definition.

### Coverage

you should have code coverage which make sure that you run tests for all of the code specially when the software become complex you'll not be able to track it easily.