# Python Scope

- Python turns your program’s main script into a module called __main__ to hold the main program’s execution. Whenever you run a Python program or an interactive session, the interpreter executes the code in the module or script that serves as an entry point to your program.

- To investigate the names within your main global scope, you can use dir() , If you call it without arguments, then you’ll get the list of names that inside your current global scope while You can access or reference the value of any global name from any place in your code.

- If you try to assign a value to a global name inside a function, then you’ll be creating that name in the function’s local scope, shadowing the global name. This means that you won’t be able to change most variables that have been defined outside the function from within the function.

### Modifying global names is generally considered bad programming practice because it can lead to code that is:

1. Difficult to debug
2. Hard to understand
3. Impossible to reuse

- Good programming practice recommends using local names rather than global names. Here are some tips:

1. Write self-contained functions that rely on local names rather than global ones.
2. Try to use unique objects names, no matter what scope you’re in.
3. Avoid global name modifications throughout your programs.
4. Avoid cross-module name modifications.
5. Use global names as constants that don’t change during your program’s execution.
6. Modifying the Behavior of a Python Scope


**Definition of The global Statement:** when you try to assign a value to a global name inside a function, you create a new local name in the function scope. To modify this behavior, you can use a global statement , good to know that in global statement you can define a list of names that are going to be treated as global names.


**The nonlocal Statement Definition :** nonlocal names can be accessed from inner functions, but not assigned or updated , If you want to modify them, then you need to use a nonlocal statement.

- Unlike global, you can’t use nonlocal outside of a nested or enclosed function ,because nonlocal only works inside an inner or nested function, you will get a SyntaxError that you can’t use nonlocal in a module scope.

- you can’t use nonlocal to create lazy nonlocal names. Names must already exist in the enclosing Python scope if you want to use them as nonlocal names. This means that you can’t create nonlocal names by declaring them in a nonlocal statement in a nested function.