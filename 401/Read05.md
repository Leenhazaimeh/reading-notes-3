# Linked List : 
A data structure that contains nodes that points to the next node in the list.

Linked List Types: Singly & Doubly

- Nodes are the individual items inside a link list,  There are also ,  current , head , next nodes which they explain their selves by their name , node where you are at , first node in the list, and teh next node from the current accordingly ,we use next and current to loop over the list. 

Adding Nodes
If you want to add a node to a list before the Head node you can add it by following a procedure , create a function that calls a property newNode.next which will be equals to null since it doesn't exist yet , set it to node1 , change head value to be as newNode , Done. !

- exception : if you want to add it between two number , same procedure but you have to change the next value for the node before the newNode is added.

e.g : if we want to add the node 10 between the node 6 and 7 , follow the procedure above then make the node4.next = node 10