Node.js is a JavaScript tool that allows developers to write backend (server-side) programs in JavaScript. 
Node.js comes with a handful of built-in modules—small, independent programs—that help facilitate this purpose. Some of the core modules include:
* HTTP: a module that acts as a server
* File System: a module that reads and modifies files
* Path: a module for working with directory and file paths
* Assertion Testing: a module that checks code against prescribed constraints

Express, while not included with Node.js, is another module often used with it. 
Express runs between the server created by Node.js and the frontend pages of a web application. 
Express also handles an application's routing. Routing directs users to the correct page based on their interaction with the application.

While there are alternatives to using Express, its simplicity makes it a good place to begin when learning the interaction between a backend powered by Node.js and the frontend.

# Node Console
During the development process, is important to be able to check what’s going on in your code. Node is just a javascript environment. 
Like client side javascript, you can use the console to display useful debug information. On your local machine, you would see the console output in a terminal. 
On Glitch you can open the logs in the lower part of the screen. You can toggle the log panel with the button ‘Logs’ (top-left, under the app name).

To get started, just put the classic Hello World in the console. 
We recommend to keep the log panel open while working at these challenges. 
Reading the logs you can be aware of the nature of the errors that may occur.

# Start a Working Express Server
In the first two lines of the file myApp.js you can see how it’s easy to create an Express app object. This object has several methods, and we will learn many of them in these challenges. One fundamental method is app.listen(port). It tells your server to listen on a given port, putting it in running state. You can see it at the bottom of the file. It is inside comments because for testing reasons we need the app to be running in background. All the code that you may want to add goes between these two fundamental parts. Glitch stores the port number in the environemet variable process.env.PORT. Its value is 3000.

Let’s serve our first string! In Express, routes takes the following structure: app.METHOD(PATH, HANDLER). METHOD is an http method in lowercase. PATH is a relative path on the server (it can be a string, or even a regular expression). HANDLER is a function that Express calls when the route is matched.

Handlers take the form function(req, res) {...}, where req is the request object, and res is the response object. For example, the handler
```
function(req, res) {
  res.send('Response String');
}
```
will serve the string 'Response String'.

```javascript
app.get("/", function (req, res) {
  res.send("Hello Express");
});
```

## Serve a HTML file
We can respond with a file using the method res.sendFile(path).

You can put it inside the app.get('/', ...) route handler. Behind the scenes this method will set the appropriate headers to instruct your browser on how to handle the file you want to send, according to its type. Then it will read and send the file. This method needs an absolute file path. We recommend you to use the Node global variable __dirname to calculate the path.

e.g. absolutePath = __dirname + relativePath/file.ext.

Note: You can edit the solution of the previous challenge, or create a new one. If you create a new solution, keep in mind that Express evaluates the routes from top to bottom. It executes the handler for the first match. You have to comment out the preceding solution, or the server will keep responding with a string.

```javascript
app.get("/", function (req, res) {
  res.sendFile(__dirname + "/views/index.html")
});
```
