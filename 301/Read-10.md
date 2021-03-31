# The call stack

- we can take an indication from its name, A process where javascript keeps tracking of its execution of the code(functions) , when a function called by a script it's added to call stack , when it's finished , the call stack removes it from the stack and the script will stop when the stack is empty.


- An understanding of the call stack will help us clarify how the “function hierarchy and execution order” works in the JavaScript engine,it's mainly used when invoking functions one at time from top to bottom which means it's synchronous 


- If the stack takes up more space than it had assigned to it, it results in a “stack overflow” error,maximum javascript call stack size stack 65536



# Error messages

- The first thing that indicates you that something is wrong with your code is the famous error message, it usually appears on your console (deeveloper tools of the browser, terminal or whatever else you are using).


### Syntax errors

- I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

### Range errors

- Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

### Reference errors**

### This is as simple as when you try to use a variable that is not yet declared you get this type of errors.

### Type errors

- Like the name indicates, this types of errors show up when the types (number, string...) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

# Debugging
- To debug your JS code, the easiest and maybe the most common way its to simply console.log() the variables you want to check or, by using chrome developer tools, open your page with your JS code (cmd+o in macOS/Ctrl+o in Windows) and choose your file to debug, click the line you want to debug,refresh your page again and here you go.
