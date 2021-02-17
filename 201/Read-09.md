# Forms

Forms in HTML lets you collect information from users, ` <form> ` used as a container for the whole form along with ` <input> ` inside , input take many attributes such as: type which defines the type of your input, value that take the value with the name to the server, name,placeholder etc..

some examples of values to the type attribute , 

- text 
- password 
- submit
- search
- email 
- url 
- file 
- radip 
- checkbox
- drop-down
- date 
and many more .. 

there are also ` <textarea> ` & ` <select> `


# Lists, Tables & Forms

you should know that most people wouldn't like to fill forms so you have to style them,make them easier for the user by making the form controls vertically and add more interaction. 

there are several CSS properties that are specifically used to control the appearance of lists, tables, and forms. also ,List markers can be given different appearances using the list-style-type and list-style image properties.

Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent.

## JS EVENTS

When you browse the web, your browser registers different types of events. It's the browser's way of saying, "Hey, this just happened." Your script can then respond to these events.

Scripts often respond to these events by updating the content of the web page (via the Document Object Model) which makes the page feel more interactive.

There are many events that happen in the browser, we can classify them to:
1. UI Events: load, error, scroll .. 
2. Keyboard Events: keypress, keyup , keydown .. 
3. MOUSE EVENTS: clock, mouseover,mouseout .. 
 
 Other Events: 

 - Focus Events
 - Form Events
 - Mutation Events

 Steps for letting an event trigger a JS code: 

 1. Select t he element node(s) you want the script to respond to.
 2. Indicate which event on the selected node(s) will trigger the response. (binding)
 3. State the code you want to run when the event occurs. ( anamed of anonymous function)

 THREE WAYS TO BIND AN EVENT TO AN ELEMENT: 
 1. HTML EVENT HANDLERS ( this is a bad practice so don't use )
 2. TRADITIONAL DOM EVENT HANDLERS ( can assign events to only one function)
 3. DOM LEVEL 2 EVENT LISTENERS ( the newest and best way since it can let you assign events with more than one function at a time)
 

 Note: the order in which events are fired is called event flows it starts from the inside out, you can place event handlers on a containing element and use the event object's target property to find which of its children the event happened on because if you want to trigger events on alot of button.cells tables,al long list, this will use alot of memory and slow down performance.  