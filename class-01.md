# HTML & CSS JON DUCKET 

## Introduction 
When you are accessing a web page from your browser which is a client that lets you see and browser this content, you should know that every device connected to internet has its own IP Addres by the ISP (Internet service provider). 

Every website published online is connected to a web server even by its own server or a hosted one that you should pay some fees for that. whenever you typed enter after you wrote the website or web page name, your browser firstly check your cache to see if there's anything included about it and that is a technique your browser make in order to have better performance and save sometime, so it doesn't have to render the content from the source each time you typed that web page or website name. 

if your browser didn't find anything in the cache or it needs an update, it connects to a DNS (Domain name system) which works as a librarian that gets you to the right web server by converting the domain name typed to an IP address then the connection begins as sending and receieving , so when the connection happens, the browser sends HTTP request for a required page which is usually index.html and the server responds with a message of Accepted/Error.. etc. and this requests continues to happen each time you click a link on that page. 

Remember that process happens in milli seconds each time you request a web page or typed a domain name between the browser and the web server, you can alo check these requests and responses in performance section in your browser when you check inspect at your developer tools. 



## Extra Markup

This section illustrates more about HTML versions and how to handle them. you should know that every programming or Markup language contininues to evolving and you most likely use the HTML5 which is the last version. but, sometimes you have to pay attention for that not all browsers supports last updates and version and your wesbite should be compatible for everyone to access, so if you expect to have some users that don't have updated browsers or use old browsers like internet explorer you should go an extra mile for let their browser identify your content ususally by adding a javascript line of code.

  

`

- Note that your HTML5 pages start with declaring <!Doctype html> tag.

in the head section we can include some extra info about our pages in a <meta> tag element that may include our set of character we'll use, language, description about the page, some extra info about the author and some keywords for search engines to be checked.

  

if you are using HTML5 you might encounter new tecniques and elements of structuring the web page such as: header/footer/article/section/nav/aside/iframe/figure/div/span and many more elements that have their own semantic meaning.

  

you should be able to differentiate between inline and block element and tell the browser how to handle a new element if it's dealt with it as an inline rather that bock.

  

` <header>
used mostly as the header of the page and contains <nav> & <ul> elements
`

` <footer>
the footer of the page or a section
`

`<article>
starting an independent piece of content
`

` <section>
connects a group of sections related to each other
`

` <Iframe>
used mostly if you want to display a complete window inside your page
`

` <figure>
to embed sth with a source in your page like a bunch of images/videos/graphs/digrams, usually with a <figcaption> that tells a decsription about that content
`

` <div>
connect group of elements with reated topic or purpose together along with ` <span> which is an inline element
`

Also , you should also keep an eye for classes and id attributes that tells more about your element tag and helps you start targeting them with CSS styles.

  

finally, remeber that code escape which is a resevred character in HTML that let you write more than and less than characters without using them for HTML purposes.
## Process & Design

  

When you are intending to build a website, there may be some non so technical process you will likely to follow in order to get your message in hands of your target audience and achieve a nice flow of your website. the first step is to imagine a sample of your target audience with all information you need like demographics, interests and behaviors. After that you have to specifiy the reason they are going to use your website and provide straightforward, clear and useful information to achieve an inspiring experience.

  

Once you do that, you will likely to do sth called site mapping that explains how overall structure of your web pages will look like usually in a heirachy method, then do a wireframe for every page in that heirachy which is a simple sketch for every page in order to let you imagine the final result and facilitate your writing code process.

  
  

## Structure

  

perhaps none of us didn't use Word docs processor before, remember that structure you were doing such as Heading 1 , heading 2 , paragraphs? your web page should be sth similar. Well-structured page will pay attention to headings, the most important heading should be the biggest (heading 1) and the sub-headings go inside with lower heading numbers heading 2 & 3,paragraph lay between them with their proper size and so on which is a commen sense design that will make your content easier to sink anyone's mind.

  

## HTML5 Layout

  

There might be some specifications or we can call *common use* for structuring web pages in HTML. they differ a little from each version of HTML, for example older versions of HTML used to use id attributes in header,footer,content.However, HTML5 which is the recent one help us alot doing this by just calling them as tags `<header>` , `<footer>` and so on ..

  

This example illustrates how HTML5 structures web pages.

`` 
	
	<header>

	<h1>This is a heading 1</h1>

	<nav>

	<ul>

	<li><a href="" class="current">home</a></li>
`
	<li><a href="">classes</a></li>

	<li><a href="">catering</a></li>

	<li><a href="">about</a></li>

	<li><a href="">contact</a></li>

	</ul>

	</nav>

	</header>
``
# JS Ducket 

## The ABC of programming

### A quick over view how computers work 

Computers are unlinke humans, I think humans are smarter but.. computers are more presice and the probability of computers making mistake might be a limit goes to zero while we may make a lot of mistakes as we may get distracted,confused and we also have feelings that might affect our logic. 

Computers are so logical and obedient, you just want to tell them what to do and they will do it exactly as you want, they work by instructions(programs). First of all, I think you have to know what you want the computer to for you then you can break this process into well-organized steps. Flowcharts and diagrams may help yoo doing this. Finally you have to convert these steps into syntax that computers understand which is in our case Javascript. Sometimes computers have to get some engines in order to convert a language syntax to a low-level langugae that the latter will then convert it into machine language which is binary. 

This is a quick brief on how we should interact with computers, so just be logical, precise,pay attention to details and get to know its language to communicate with it effectively!. 

### About Javascript

Javascript is a scripting language that mostly used in web to interact with web pages and web applications. Through Javascript we can turn static web site into a dynamic and interactive experience so we can make slides, animations,applications and alot of other things. it mostly used for front-end and it works for back-end as well. 

Another classifications of this language are procedural programming language which means it executes code line by line also something called OOP with basically treats anything in physical life as objects that have properites,methods and events.

every objects has his own properties, methods which lets you simply recall them by referring to the name of that property you related for the object and methods by follwing them with empty paranthesis().

Also there are events that you can tie your methods and actions to, it's just another way for telling the computer "hey this is just happened" then do whatever you want to do when they are triggered! 

Another thing you may also want to know when dealing with web world is the DOM (Document object mode) that structure the page in a set of groups as child, parent, siblings etc.. and facilitate dealing with the web page. 

### Javascript syntax

As we said before, javascript used mainly in web world. so it's used alot for interacting with content that it is HTML elements. using java script we can access some content in a web page,modify it, delete it or extracting something from it.

There are many ways for writing script: 

1. External scripts (in another files linked to HTML pages)
2. inside HTML Body (usually after the body tag or after content in body tag works also )
3. Inside HTML Head (used with some keywords to let scripts executed asyncronously for example )