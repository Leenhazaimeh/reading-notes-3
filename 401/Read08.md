# List Comprehensions in Python

- a very short syntax with a powerful logic. 
- its basic rules that it starts with square brackets since its result is always a list.
- its basic syntax:
    [ expression for item in list if conditional ]
    
- This is equivalent to:
``
    for item in list:
        if conditional:
            expression
``
- we can divide it into three parts:
1. the expression which is the main operation also called transformation such as multiply , sum , calling a function ..etc.
2. for that is responsible for iteration 
3. conditional for specifying conditions for each item in the list.

- simple example for creating a simple list: 
    x = [i for i in range(10)]
    print x
    ### This will give the output:
    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

- using it in functions: 
    ### Create a function and name it double:
        def double(x):
        return x*2

    ### If you now just print that function with a value in it, it should look like this:
        >>> print double(10)
        20

- most advantages with functions: 1)put in conditions  2) add more arguments

    ### putting in conditions:

        >>> [double(x) for x in range(10) if x%2==0]
            [0, 4, 8, 12, 16]

    ### Adding more arguments:

        >>> [x+y for x in [10,30,50] for y in [20,40,60]]
            [30, 50, 70, 50, 70, 90, 70, 90, 110]