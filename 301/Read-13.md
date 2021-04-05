# Data:

- sending form data is easy, but securing an application can be tricky. 
- Once the form data has been validated on the client-side, it is okay to submit the form. 
- And, since we covered validation in the previous article, we're ready to submit! 

- We also look at some of the security concerns associated with sending form data.

**Prerequisites**

- Basic computer literacy, an understanding of HTML, and basic knowledge of HTTP and server-side programming.

**Objective:**

- To understand what happens when form data is submitted, including getting a basic idea of how data is processed on the server

**Client/server architecture**

- At it's most basic, the web uses a client/server architecture that can be summarized as follows. 

- The server answers the request using the same protocol.

**The action attribute**

- The action attribute defines where the data gets sent.
- If this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page.

**The method attribute**

- The method attribute defines how data is sent. 

- Just remember that a front-end developer is not the one who should define the security model of the data.It's possible to perform client-side form validation, but it won't be trusted by the server because it doesn't know what truly happens in the client.
**Security issues**

- Each time you send data to a server, you need to consider security. 

- HTML forms are by far the most common server attack vectors (places where attacks can occur). 

