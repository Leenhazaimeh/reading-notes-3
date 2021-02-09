## Links 

There are many ways of declaring links in your web page depends on where you want to link to: 

1. External links (uses href attibute with the absolute url path )
2. Internal links (uses href along with the relative path in your project, yiu should also pay attention to directory heirachy) 
for example: if you're in the same level of the page you want link to it will look like this href="contact.html", if it's child it will be as "page/index.html" & if you want to go back in level towards root you use inside the href attrubite "../../index.html" .

3. Internal links to specific section in a page or another page (usually by referring to an id attribute using # and its name) 
for example: href="contact.html/#phone_number" 
Note : remember that those sections should have the id attribute inside their html.

Target attribiute with a value of _blank can be used to open a link in a new tab.

## Layout

Using CSS There are several ways to control a position of an element which HTML & CSS treats it as a box referring to its type of block level or an inline. The

There are multiple possible values for position property: 
1. static which is the normal flow of the content 
2. relative which pulls out the element of its normal flow and lets you control its position using (top.bottom,left,top)  with a reference of the normal flow it should be on. 
3. absolute which pulls it out of its normal flow and lets you move it with a reference to its containing box.
4. Fixed which works as absolute but with a reference of browser window so the elements won't move while you are scrolling.


you can also control your elements using float of left and right, you also can clear any float from inside element if it's affected. whenever any overlapping occurs you can use index-z and give a higher value for the element you want to show on the top!


whenever you design a web page you should pay attention to screen sizes and make it responsive and not fixed, regarding css frameworks they have some pros and cons, they save you of repeated code but requires using classnames that only controls the presentation rather than descriping the content.

Using Grid property you can easily create you page into columns and rows design. 

you also should know that you can link to multiple stylesheets either inside the html page or using @import ( css relative path) inside the main css you are linking to.

## Function 

Functions let you group a series of statements together to perform a
specific task. there are many ways for declaring functions, sometimes it depends on their type as well. if it's a normal function you should recall it inorder to use it.

function usually used for return values either if it's single or multiple using arrays. and it's done with return and this statement should be the last one in its code block. 

Types of functions: 
- Normal function 
- Anynymous functions (usually used for varable declaration expression and can assign to a variable, it doesn't have a name)
- immdeiately invoked functons (executed the moment the browser encouters them and wrapped withing paranthesis)

Good to know that function takes parameters and can pass any argument to them if you already put the expected paremeters when declaring as (index,a) rather than leave it empty. 

## Pair prgramming 

it's just a very powerful techniuqe during learning code, it combines roles of a driver who executes everything and a narrator who captures the big picture. it has alot of benifits such as a more collaborative environment, very good efficiency expected, it also allow i=us to learn from each other and discuss problems so it improves problem sloving & it definitely will enhace the communication skills and that will make a difference in interviews and in work environments. 