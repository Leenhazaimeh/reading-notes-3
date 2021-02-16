## Layout

Using CSS There are several ways to control a position of an element which HTML & CSS treats it as a box referring to its type of block level or an inline. The

There are multiple possible values for position property: 
1. static which is the normal flow of the content 
2. relative which pulls out the element of its normal flow and lets you control its position using (top.bottom,left,top)  with a reference of the normal flow it should be on. 
3. absolute which pulls it out of its normal flow and lets you move it with a reference to its containing box.
4. Fixed which works as absolute but with a reference of browser window so the elements won't move while you are scrolling.


you can also control your elements using float of left and right, you may also clear any float from inside element if it's affected. whenever any overlapping occurs you can use index-z and give a higher value for the element you want to show on the top!


whenever you design a web page you should pay attention to screen sizes and make it responsive and not fixed, regarding css frameworks they have some pros and cons, they save you of repeated code but requires using classnames that only controls the presentation rather than descriping the content.

Using Grid property you can easily create you page into columns and rows design. 

you also should know that you can link to multiple stylesheets either inside the html page or using @import ( css relative path) inside the main css you are linking to.