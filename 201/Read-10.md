# JS Debugging 

When writing a long script, nobody gets everything right in their first attempt. The error messages that a browser gives look cryptic at first, but they can help you determine what went wrong in your JavaScript and how to fix it.

during executing script , it passes through several stages when trying to perform a specific tasks, it's called execution contexts, Each time a script enters a new execution context, there are two phases
of activity :Prepare & Execute.

Prepare : The preparation phase is often described as taking all of the variables and functions and hoisting them to the top of the execution context. Or you can think of them as having been prepared.

Execute: Assign values to variables , Reference functions and run their code , Execute statements.

The Satck: The Javascript interepter processes one line of code at a time. when a statement needs data from another function, it stack(or piles) the new function on top of the current tasks. 

Functions in JavaScript are said to have lexical scope. They are linked to the object they were defined within. So, for each execution context, the scope is the current execution context's variables object, plus the variables object for each parent execution context.In the interpreter, each execution context has its own variables object. It holds the variables, functions, and parameters available within it. Each execution context can also access its parent's variables object.

 If you understand scopes , functions,execution contexts along with stacks, you are more likely to find the error in your code as well as understand hoisting which lets you Call functions before they have been declared (if they were created using function declarations - not function expressions) , Assign a value to a variable that has not yet been declared

 If a JavaScript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for exception-handling code

Debugging is the process of finding errors. It involves a process of deduction. you have to look for the problem and be organized following these steps: First, should try to can narrow down the area where
the problem seems to be. In a long script, this is especially important.

1. Look at the error message, it tells you: The relevant script that caused the problem. The line number where it became a problem for the interpreter. (As you will see, the cause of the error may be earlier in a script; but this is the point at which the script could not continue.) The type of error (although the underlying cause of the error may be different).

2. Check how far the script is running. Use tools to write messages to the console to tell how far your script has executed. there are other console.log methods such as: 

- ` conso1e. info() ` can be used for general information
- ` console.warn() ` can be used for warnings
- ` console.error () ` can be used to hold errors
- If you want to write a set of related data to the console, you can use the ` console. group () ` method to group the messages together. You can then expand and contract the results.
- When you have finished writing out the results for the group, to indicate the end of the group the console ` .groupEnd () ` method is used.

3. Use breakpoints where things are going wrong. They let you pause execution and inspect the values
that are stored in variables.  

- You can pause the execution of a script on any line using breakpoints. Then you can check the values stored in variables at that point in time. 
- If you set multiple breakpoints, you can step through them one-by-one to see where values change and a problem might occur.
- You can indicate that a breakpoint should be triggered only if a condition that you specify is
met. The condition can use existing variables.
- You can create a breakpoint in your code using just the debugger keyword. When the developer tools are open, this will automatically create a breakpoint.
- You can also place the debugger keyword within a conditional statement so that it only triggers
the breakpoint if the condition is met. This is demonstrated in the code below.

Note: If you are stuck on an error, many programmers suggest that you try to describe the situation (talkingout loud) to another programmer. Explain what should be happening and where the error appears
to be happening. This seems to be an effective way of finding errors in all programming languages. (If
nobody else is available, try describing it to yourself.) 

Error objects can help you find where your mistakes are and browsers have tools to help you read them.

The console helps narrow down the area in which the error is located, so you can try to find the exact error.

JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error. If you know that you may get an error, you can handle
it gracefully using the try, catch, finally statements, try to use them to give your users helpful feedback. you also can generate your own errors before the interpreter creates them using ` throw new Error `

If you are working with data from a third party, you may come across problems such as:
- JSON that contains a formatting error
- Numeric data that occasionally has a nonnumeric value
- An error from a remote server
- A set of information with one missing value. 

Bad data might not cause an error in the script straight away, but it could cause a problem later on.
In such cases, it helps to report the problem straight away. It can be much harder to find the source of the problem if the data causes an error in a different part of the script.


Here are a selection of practical tips that you can try to use when debugging your scripts: 

1. ANOTHER BROWSER
2. Write numbers to the console so you can see which the items get logged. It shows how far your code runs before errors stop it.
3. Remove parts of code, and strip it down to the minimum you need. You can do this either by
removing the code altogether, or by just commenting it out using multi-line comments:
4. SEARCH such as Stackoverflow 
5. add it to a code
playground site (such as JSBin.com, JSFiddle. com, or Dabbl et. corn) and then post a link to it from the forum.
6. VALIDATION TOOLS