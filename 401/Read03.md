# Reading and Writing Files in Python

- Files at their core are a bytes of data (binary of 0 and 1) in order to make the computer process them, files generally contain of 3 parts:
1. Header : Meta data about file 
2. File Data : file content and it depends on the type of the extension of the file
3. extension

- In python you can manipulate the files in your system and assign them to  variables, using open() method which is built in method in python , will always return an object file , after access that file then we can do process on its content , append to it , remove from it and much more ..

- The most common way of open a file is to read , read() method do this and it's the default when open a file, you also can write .write() , while using open as well , we can add another string arguments such as "w" , "r" , "wb" , "rb" , and its useful and let you write and read binary of the file.

- Note: There are some differences regarding files in OS distributions which can leads to some sequences when using same code on different OS , such as:  the character of ending the line that may lead to not iterate over lines properly , in windows /r/n , linux /n and in old mac /r.
-Note : It's always a good practice to handle the file closing because we can't guarantee safe closing always, either you do this inside a try,finally  statement or we can take advantage of with statement that defines a variable immediately and it will take care of closing the variable if we forgot to do it!

# Python Exceptions

- We can tell the definition of the exception simply by its name, its not an error by itself rather an exception , remember there are many error such as syntax error when improperly using the syntax language , and many errors , but what special about exception is that you can raise your exceptions which can be very useful at some cases, e.g of exceptions: DivisionByZero, etc..

-we can take advantage of this feature and raise our own exceptions if conditions met, for example to make sure we achieve sth , or if I don't want my program to proceed with a specific condition , we can use if,else then raise , or try , except to process while exception occurs.

Code Example:
`` 
    x = 10
    if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))
``

- Assertion exception: let your program throw an assertion exception if a condition is not met , we can use it to handle terminate our program by itself before it's actually done by rasing an assert exception, we used this alotin testing.

