# HTML TABLES 

we can add tables to our HTML using ` <table> ` tag , it's structured by row , each raw started with ` <tr> ` , inside each raw we include ` <td> ` which is table data. Also, using colspan & rowspan attributes we can make them span by specifying the number of cols or rows we want to streth the data to. 

if the table were long we can split it into ` <thead> , <tbody> , <tfoot> ` 

# Functions, Objects & Methods 

An object is a series of variables (which are called peoperties) and functions (which are called methods) that represent something from the world around you. 

We can make objects using constructor rather than literal by using ` new Object() `which is part of the javascript language then add keys and assign them to values using object name followed by (.) then the peoperty name or the method , after that we can also update these values anytime.

In fact we can go further and creating many objects using a template we create by a function that take also parameters , inside it and with help of (this) we assign the values to the properties which will be the same as the parameters we pass to. then we daclare whatever variable name we want and using (new) keyword with the name of the object followed by the arguments which will be the values for the properties and they will make a new object automatically! such a very powerful tool that facilitate the process. 

Note : The name of a constructor function usually begins with a capital letter (unlike other functions, which tend to begin with a lowercase character).

There are 3 types of bult-in objects: 
1. BROWSER OBJECT MODEL helps you work with the browser properties and functions. 
2. DOCUMENT OBJECT MODEL helps you work with a DOM tree
3. GLOBAL JAVASCRIPT OBJECTS such as for: String, numbers,date,math.

when it comes to arrays , they are objects as well but the key is their index. so they are special object that are used to create complex data sets along with the normal objects and they both can include each other. 