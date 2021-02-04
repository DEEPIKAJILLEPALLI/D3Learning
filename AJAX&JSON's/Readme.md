# AJAX
* The term AJAX originated as an acronym for **Asynchronous JavaScript And XML**. 
* It refers to a group of technologies that make asynchronous requests to a server to transfer data, then load any returned data into the page. 
* An asynchronous process has a couple key properties. The browser does not stop loading a page to wait for the server's response. 
  * Also, the browser inserts updated data into part of the page without having to refresh the entire page.

> User experience benefits from asynchronous processes in several ways. 
* Pages load faster since the browser isn't waiting for the server to respond in the middle of a page render. 
* Requests and transfers happen in the background, without interrupting what the user is doing.
*  When the browser receives new data, only the necessary area of the page refreshes. These qualities especially enhance the user experience for single page applications.

> The *data transferred between the browser and server* is often in a format called **JavaScript Object Notation (JSON)**. JSON resembles JavaScript object literal syntax, except that it's transferred as a string.Once received, it can be converted into an object and used in a script.
* However, JSON transmitted by APIs are sent as bytes, and your application receives it as a string.
*  These can be converted into JavaScript objects, but they are not JavaScript objects by default. 
* The **JSON.parse** method parses the string and constructs the JavaScript object described by it.