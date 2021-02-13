
# Object literals

  

Object literal is one of other ways for creatinfg objects in javascript , objects are declared as variable put their keys and values inside a curly brackets.

  

This keys can be either properties or methods for that object.

  

	` var Car = {

	type: "BMW;

	weight: 4500;

	color: "black";

	inside : "panaroma";

	startEngine = function() {

	//code here

	}

	}

  

we can access peoperties by using (.) and the property name or using square brackets and the property name inside a quotation, so I can call color of the car by :

  

	Car.color

	Car.["color"]

  
  
  

second type usually used when weird symbol and characters property name is used usually when it's reversed by a server but the first way wil almost do the work,I also can change the value by assigning it to whatever I want , regardign methods they are accessed by usin their name followed by () paranthesis just like functions.

  
  

# DOM

  

The Document Object Model (DOM) specifies how browsers should create a model of an HTMLpage and how JavaScript can access and update the contents of a web page while it is in the browser window. it is stored in Browser memory and it consists of four main types of nodes.

- THE DOCUMENT NODE

- ELEMNTS NODE

- ATTRIBUTE NODES

- TEXT NODES

  

When you access any element, attribute, or text node, you navigate to it via the document node. It is the starting point for all visits to the DOM tree. To access the DOM tree, you start by looking for elements. Once you find the element you want, then you can access its text and attribute nodes if you

want to.

  

to select an element node or more, there are such ways like : ` document.querySelector `, ` document.querySelectorAll ` ,  ` document.getElementById ` ,  ` getElementsByClassNames ` and many more.. , some of them work for a single elemnt and others return nodelist. After that you can easily access and update using text nodes, work with HTML and access or update attribute values.

  

Using innerHTML property for example lets you Add content to the web page, remove content by setting it to an empty string or maybe you should take a look on working with attributes such as SetAttiribute, getAttibute, hasAttribute , removeAttribute.

  

this DOM sometimes peopele refers to it as API (Application Programming Interface) which is a software intermediary that allows two applications to talk to each other.