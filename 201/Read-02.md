## Text

In order to give your web page a meaningful content you have to follow structure rules in HTML by using markup elements which they divided into structural and semantic ones. 

the structural is for structing content like heading,subheading ..etc.
the semantic which provides extra information about the tag like <b> , <em> , <i> ,<br> , <hr> <s> , <sup> , <sub> , <strong> , <blockquote> , <q> , <abbr> , <cite> , <dfn> , <ins> , <del>.


## Introducing CSS

CSS stands for cascading style sheets. it's a way for styling your HTML content simply by calling the element we want to apply the style on it by sth called selectors then make a declaration with a property and a value for it.

Examples of selectors: 
- Tag name 
- class name 
- id 
- + 
- ~

your CSS code will look sth like this: 


``

	h1 {

	color:white;

	padding:20px;

	}

``
There are multiple ways of adding css styles to a web page: 
1. Inline (style attribute inside HTML element 'rarely used')
2. Internal (style tag inside head of the HTML 'used when you want to add styles to a web page that is different than others)
3. External (linking to a css file using link element in the head 'recommended and mostly used since it has many benifits such as: you don't have to modify each web page indivisually you simply can link every web page to the same css files & it helps also with performance since you don't have to add code to your HTML for each page to not download each css seperately.')


### Colors in CSS
We don't doubt that colors add life to everything, your web page should also have colors. 

Many ways of declaring colors by:
1. name 
2. rgb or rgba which is with opacity (can take values up to 255 , 0-1 for a)
3. HEX #00ffee where each two sequent numbers stands for rgb. 
4. HSLA which is hue,saturation,brightness and opacity (0-360,percentage,percentage,0-1)


## Basic JavaScript Instructions

the script is some lines of instructions you tell the computer to execute. 

Each meaningful line of code in javascript (instruction or step) can be called statement and each statement should be ended with semicolon(;) for a cleaner code purposes. Statement can be included in block codes usually between curly brackets. 

Note: Javascript is case sensitive. 

a variable is as a container for a data, and data type can be number, string, boolean. 

you usually declaring variable by using var prefix , you can aslo use let & const. then assign a value for than variable using (=) and tis line of code called expression. There are also many rules you should follow when you name a varibale. 

regarding data types : for numbers you can use arithmetic operators in declaring variable and assigning them to values, for string you should include them between quotation marks, and boolean should be true or false. 

Arrays : works as a container for many variables, so rathen than declaring many variables with many data types you can include them in one array and recalling their values by their index, and it's 0 based index. 



### Operators and comparison 

Operator is a tool that helps you doing some processes, there are three types of operators: 
1. Arithmitic operators like + ,- , /, * , % , ** 
2. Logical operators like && , || , ! 
3. Comparison operators ==, === , != , !===, >= , < and many more. 

Note: (+) works with string as concatenation. and if you try to do any arithmetic operatior for strings it will return NaN. 


### logical operators 

&& stands for "and", the condition cannot be satisfied untill all expression have the same boolean value. 
|| stands for "or" , one expression is enough to satisfy the condition. 
! stands for "not", reverse the boolean value of the expression to the opposite. 

## Switch

Switch statement is another way of writing conditional statements by simply call a switch with an argument as : switch (level) , then inside curly brackets you start mentioning the cases you expect to have and what to do if that happens liek : Case 'One': // code block then break; , in the last you will include default case which will happen if none of the cases above trigger. 

it will loook sth like this:



	switch(expression) {

	case x:

	// code block

	break;

	case y:

	// code block

	break;

	default:

	// code block

	}

