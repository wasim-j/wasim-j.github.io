React is a great tool to render the User Interface (UI) of modern web applications.

React is a JavaScript library designed to make it easier to build complex user interfaces. React does this in a few ways:
* React allows HTML to render from a JavaScript file.
* React breaks a website's parts into Components that can then be combined to build pages.
* React Components can pass data to each other as properties

React uses a virtual Document Object Model. 

Instead of changing the DOM directly, React makes a simplified copy of the DOM (the virtual DOM) when the page loads. 
This allows React to make changes to elements on the page without re-rendering the entire page. 
This can improve the responsiveness and functionality of single-page applications.

# JSX
While not part of the React library and not required, JSX is often paired with React. 
JSX is a preprocessor for JavaScript written in a syntax akin to XML that results in more readable code.

React uses a syntax extension of JavaScript called JSX that allows you to write HTML directly within JavaScript. This has several benefits. 
It lets you use the full programmatic power of JavaScript within HTML, and helps to keep your code readable. 
For the most part, JSX is similar to the HTML that you have already learned, however there are a few key differences that will be covered throughout these challenges.

For instance, because JSX is a syntactic extension of JavaScript, you can actually write JavaScript directly within JSX. 
To do this, you simply include the code you want to be treated as JavaScript within curly braces: { 'this is treated as JavaScript code' }. 
Keep this in mind, since it's used in several future challenges.

However, because JSX is not valid JavaScript, JSX code must be compiled into JavaScript. The transpiler Babel is a popular tool for this process. 

## Single Element Return
One important thing to know about nested JSX is that it must return a single element. 
This one parent element would wrap all of the other levels of nested elements. 
For instance, several JSX elements written as siblings with no parent wrapper element will not transpile. Here's an example:

```jsx
//Valid JSX:
<div><p>Paragraph One</p><p>Paragraph Two</p><p>Paragraph Three</p></div>

//Invalid JSX:
<p>Paragraph One</p><p>Paragraph Two</p><p>Paragraph Three</p>
```

Note: When rendering multiple elements like this, you can wrap them all in parentheses, but it's not strictly required. 
Also notice this challenge uses a div tag to wrap all the child elements within a single parent element. If you remove the div, the JSX will no longer transpile. 
Keep this in mind, since it will also apply when you return JSX elements in React components.

## Commenting
To put comments inside JSX, you use the syntax {/* */} to wrap around the comment tex

## HTML Class in JSX (class is className)
One key difference in JSX is that you can no longer use the word class to define HTML classes. This is because class is a reserved word in JavaScript. 
Instead, JSX uses className.

In fact, the naming convention for all HTML attributes and event references in JSX become camelCase. 
For example, a click event in JSX is onClick, instead of onclick. Likewise, onchange becomes onChange. 
While this is a subtle difference, it is an important one to keep in mind moving forward.

## Self-Closing JSX Tags
In HTML, almost all tags have both an opening and closing tag: <div></div>; the closing tag always has a forward slash before the tag name that you are closing. 
However, there are special instances in HTML called “self-closing tags”, or tags that don’t require both an opening and closing tag before another tag can start. 
For example the line-break tag can be written as <br> or as <br />, but should never be written as <br></br>, since it doesn't contain any content.

In JSX, the rules are a little different. Any JSX element can be written with a self-closing tag, and every element must be closed. 
The line-break tag, for example, must always be written as <br /> in order to be valid JSX that can be transpiled. 
A <div>, on the other hand, can be written as <div /> or <div></div>. 
The difference is that in the first syntax version there is no way to include anything in the <div />.

## Styling JSX elements
If you import styles from a stylesheet, it isn't much different at all. You apply a class to your JSX element using the className attribute, and apply styles to the class in your stylesheet. 
Another option is to apply inline styles, which are very common in ReactJS development.

You apply inline styles to JSX elements similar to how you do it in HTML, but with a few JSX differences. Here's an example of an inline style in HTML:
```jsx		
<div style="color: yellow; font-size: 16px">Mellow Yellow</div>
```
JSX elements use the style attribute, but because of the way JSX is transpiled, you can't set the value to a string. Instead, you set it equal to a JavaScript object. Here's an example:
```jsx		
<div style={{color: "yellow", fontSize: 16}}>Mellow Yellow</div>
```

### Camel Case
First, the names of certain CSS style properties use camel case. For example, the last challenge set the size of the font with fontSize instead of font-size. 
Hyphenated words like font-size are invalid syntax for JavaScript object properties, so React uses camel case. 
As a rule, any hyphenated style properties are written using camel case in JSX.

All property value length units (like height, width, and fontSize) are assumed to be in px unless otherwise specified. 
If you want to use em, for example, you wrap the value and the units in quotes, like {fontSize: "4em"}. 
Other than the length values that default to px, all other property values should be wrapped in quotes.

# ReactDOM
With React, we can render this JSX directly to the HTML DOM using React's rendering API known as ReactDOM.

ReactDOM offers a simple method to render React elements to the DOM which looks like this: ReactDOM.render(componentToRender, targetNode).
* The first argument is the React element or component that you want to render.
* The second argument is the DOM node that you want to render the component within.

As you would expect, ReactDOM.render() must be called after the JSX element declarations, just like how you must declare variables before using them.

# Creating Components
Components are the core of React. Everything in React is a component and here you will learn how to create one. 
There are two ways to create a React component.

## JS Function
The first way is to use a JavaScript function. 
	
Defining a component in this way creates a stateless functional component. The concept of state in an application will be covered in later challenges. 
For now, think of a stateless component as one that can receive data and render it, but does not manage or track changes to that data. (We'll cover the second way to create a React component in the next challenge.)

To create a component with a function, you simply write a JavaScript function that returns either JSX or null. 
One important thing to note is that React requires your function name to begin with a capital letter. 

Here's an example of a stateless functional component that assigns an HTML class in JSX:
```jsx
// After being transpiled, the <div> will have a CSS class of 'customClass'
const DemoComponent = function() {
  	return (
    		<div className='customClass' />
  	);
};
```
Because a JSX component represents HTML, you could put several components together to create a more complex HTML page. 
This is one of the key advantages of the component architecture React provides. It allows you to compose your UI from many separate, isolated components. 
This makes it easier to build and maintain complex user interfaces.

Note: The text is considered a child of the div element, so you will not be able to use a self-closing tag.

## ES6 class syntax
The other way to define a React component is with the ES6 class syntax. In the following example, Kitten extends React.Component:
```jsx
class Kitten extends React.Component {
  constructor(props) {
    	super(props);
  }

  render() {
    	return (
    			<h1>Hi</h1>
    	);
  }
}
```
This creates an ES6 class Kitten which extends the React.Component class. 

So the Kitten class now has access to many useful React features, such as local state and lifecycle hooks. 
Don't worry if you aren't familiar with these terms yet, they will be covered in greater detail in later challenges.

Also notice the Kitten class has a constructor defined within it that calls super(). 
It uses super() to call the constructor of the parent class, in this case React.Component. 
The constructor is a special method used during the initialization of objects that are created with the class keyword. 
	
It is best practice to call a component's constructor with super, and pass props to both. 
This makes sure the component is initialized properly. For now, know that it is standard for this code to be included.

# Component Composition
Now we will look at how we can compose multiple React components together. 
Imagine you are building an App and have created three components, a Navbar, Dashboard, and Footer. 
To compose these components together, you could create an App parent component which renders each of these three components as children. 
To render a component as a child in a React component, you include the component name written as a custom HTML tag in the JSX. 
For example, in the render method you could write:
```jsx
return (
 <App>
  <Navbar />
  <Dashboard />
  <Footer />
 </App>
)
```

When React encounters a custom HTML tag that references another component (a component name wrapped in < /> like in this example), it renders the markup for that component in the location of the tag. 
This should illustrate the parent/child relationship between the App component and the Navbar, Dashboard, and Footer.

Component composition is one of React's powerful features. 
When you work with React, it is important to start thinking about your user interface in terms of components like the App example in the last challenge. 
You break down your UI into its basic building blocks, and those pieces become the components. 

This helps to separate the code responsible for the UI from the code responsible for handling your application logic. 
It can greatly simplify the development and maintenance of complex projects.

As the challenges continue to use more complex compositions with React components and JSX, there is one important point to note. 
Rendering ES6 style class components within other components is no different than rendering the simple components you used in the last few challenges. 
You can render JSX elements, stateless functional components, and ES6 class components within other components.

# Props
With this foundation, it's time to look at another feature very common in React: props. In React, you can pass props, or properties, to child components. 
Say you have an App component which renders a child component called Welcome that is a stateless functional component. You can pass Welcome a user property by writing:
```jsx
<App>
  <Welcome user='Mark' />
</App>
```

You use custom HTML attributes that React provides support for to pass the property user to the component Welcome. 
Since Welcome is a stateless functional component, it has access to this value like so:
```jsx
const Welcome = (props) => <h1>Hello, {props.user}!</h1>
```

It is standard to call this value props and when dealing with stateless functional components, you basically consider it as an argument to a function which returns JSX. 
You can access the value of the argument in the function body. With class components, you will see this is a little different. 

The way to pass an array to a child component is a little different than the process for passing a string. 
Both data types use the HTML-like attribute syntax, but you wrap a string value in quotes (<ChildComponent myProp="stringData" />), and you treat an array value as JavaScript. 
Since you are composing this code within a JSX element, it must be wrapped by curly braces (<ChildComponent myProp={arrayData} />).

## Default Props
React also has an option to set default props. 
You can assign default props to a component as a property on the component itself and React assigns the default prop if necessary. 

This allows you to specify what a prop value should be if no value is explicitly provided. 
For example, if you declare MyComponent.defaultProps = { location: 'San Francisco' }, you have defined a location prop that's set to the string San Francisco, unless you specify otherwise. 

React assigns default props if props are undefined, but if you pass null as the value for a prop, it will remain null.

### Override Default Props
The ability to set default props is a useful feature in React. 
The way to override the default props is to explicitly set the prop values for a component.

## PropTypes
React provides useful type-checking features to verify that components receive props of the correct type. 
For example, your application makes an API call to retrieve data that you expect to be in an array, which is then passed to a component as a prop. 
You can set propTypes on your component to require the data to be of type array. This will throw a useful warning when the data is of any other type.

It's considered a best practice to set propTypes when you know the type of a prop ahead of time. 
You can define a propTypes property for a component in the same way you defined defaultProps. 
Doing this will check that props of a given key are present with a given type. Here's an example to require the type function for a prop called handleClick:
```jsx
MyComponent.propTypes = { handleClick: React.PropTypes.func.isRequired }
```

In the example above, the React.PropTypes.func part checks that handleClick is a function. 
Adding isRequired tells React that handleClick is a required property for that component. You will see a warning if that prop isn't provided. 

Also notice that func represents function. Among the seven JavaScript primitive types, function and boolean (written as bool) are the only two that use unusual spelling. 
	
In addition to the primitive types, there are other types available. For example, you can check that a prop is a React element. 
Please refer to the documentation for all of the options.

## Access Props Using this.props
The last several challenges covered the basic ways to pass props to child components. 
But what if the child component that you're passing a prop to is an ES6 class component, rather than a stateless functional component? 
The ES6 class component uses a slightly different convention to access props.

Anytime you refer to a class component within itself, you use the this keyword. 
To access props within a class component, you preface the code that you use to access it with this. 
For example, if an ES6 class component has a prop called data, you write {this.props.data} in JSX.

# Summary of Componenet Types
A __stateless functional__ component is any function you write which accepts props and returns JSX.

A __stateless component__, on the other hand, is a class that extends React.Component, but does not use internal state (covered in the next challenge). 

A __stateful component__ is any component that does maintain its own internal state. You may see stateful components referred to simply as components or React components.

A common pattern is to try to minimize statefulness and to create stateless functional components wherever possible. 
This helps contain your state management to a specific area of your application. 
In turn, this improves development and maintenance of your app by making it easier to follow how changes to state affect its behavior.

# State
One of the most important topics in React is state. State consists of any data your application needs to know about, that can change over time. 
You want your apps to respond to state changes and present an updated UI when necessary. 
React offers a nice solution for the state management of modern web applications.

State is one of the most powerful features of components in React. 
It allows you to track important data in your app and render a UI in response to changes in this data. If your data changes, your UI will change. 
React uses what is called a virtual DOM, to keep track of changes behind the scenes. 
When state data updates, it triggers a re-render of the components using that data - including child components that received the data as a prop. 
React updates the actual DOM, but only where necessary. This means you don't have to worry about changing the DOM. You simply declare what the UI should look like.

Note that if you make a component stateful, no other components are aware of its state. 
Its state is completely encapsulated, or local to that component, unless you pass state data to a child component as props. 
This notion of encapsulated state is very important because it allows you to write certain logic, then have that logic contained and isolated in one place in your code.

## Creating State
You create state in a React component by declaring a state property on the component class in its constructor. 
This initializes the component with state when it is created. The state property must be set to a JavaScript object. Declaring it looks like this:
```jsx
this.state = {	// describe your state here}
```
You have access to the state object throughout the life of your component. You can update it, render it in your UI, and pass it as props to child components. 
The state object can be as complex or as simple as you need it to be. 
Note that you must create a class component by extending React.Component in order to create state like this.

## Render State in the UI
Once you define a component's initial state, you can display any part of it in the UI that is rendered. 
If a component is stateful, it will always have access to the data in state in its render() method. You can access the data with this.state.
If you want to access a state value within the return of the render method, you have to enclose the value in curly braces.

### Alternative Way to Render State in the UI
Another way to access state in a component. In the render() method, before the return statement, you can write JavaScript directly. 

For example, you could declare functions, access data from state or props, perform computations on this data, and so on. 
Then, you can assign any data to variables, which you have access to in the return statement.

## Setting State
There is also a way to change the component's state. React provides a method for updating component state called setState. 
You call the setState method within your component class like so: this.setState(), passing in an object with key-value pairs. 
The keys are your state properties and the values are the updated state data. 
	
For instance, if we were storing a username in state and wanted to update it, it would look like this:
```jsx
this.setState({username: 'Lewis'});
```

React expects you to never modify state directly, instead always use this.setState() when state changes occur. 
Also, you should note that React may batch multiple state updates in order to improve performance. 
What this means is that state updates through the setState method can be asynchronous. 
There is an alternative syntax for the setState method which provides a way around this problem. This is rarely needed but it's good to keep it in mind!

## Bind 'this' to a Class Method
In addition to setting and updating state, you can also define methods for your component class. 

A class method typically needs to use the this keyword so it can access properties on the class (such as state and props) inside the scope of the method. 
There are a few ways to allow your class methods to access this.

One common way is to explicitly bind this in the constructor so this becomes bound to the class methods when the component is initialized. 

You may have noticed the last challenge used this.click = this.click.bind(this) for its click method in the constructor. 
Then, when you call a function like this.setState() within your class method, this refers to the class and will not be undefined.

### Bind 'this' with an ES6 Arrow Function
There is another way to bind this when writing methods in React component classes. A useful, concise way is to use an ES6 arrow function. 
It does not assign its own value for this, but instead adopts the value of this from the context surrounding the function when it is written. 
In other words, an arrow function binds this automatically from its surrounding context.

The use of an arrow function as a class property like this is technically still an experimental feature of JavaScript (ES7 property initializers) but can be enabled through pre-processing. 
It's very useful because of its conciseness, but keep in mind that it is not part of the official language yet. 
Using this syntax means you can define a class method as an arrow function and not have to explicitly bind this in the constructor.

## Pass State as Props to Child Components
You saw a lot of examples that passed props to child JSX elements and child React components in previous challenges. 
You may be wondering where those props come from. 
A common pattern is to have a stateful component containing the state important to your app, that then renders child components. 
You want these components to have access to some pieces of that state, which are passed in as props.

For example, maybe you have an App component that renders a Navbar, among other components. 
In your App, you have state that contains a lot of user information, but the Navbar only needs access to the user's username so it can display it. 
You pass that piece of state to the Navbar component as a prop.

This pattern illustrates some important paradigms in React. The first is unidirectional data flow. 
State flows in one direction down the tree of your application's components, from the stateful parent component to child components. 
The child components only receive the state data they need. 
The second is that complex stateful apps can be broken down into just a few, or maybe a single, stateful component. 
The rest of your components simply receive state from the parent as props, and render a UI from that state. 
It begins to create a separation where state management is handled in one part of code and UI rendering in another. 
This principle of separating state logic from UI logic is one of React's key principles. 
When it's used correctly, it makes the design of complex, stateful applications much easier to manage.

### Pass a Callback as Props
You can pass state as props to child components, but you're not limited to passing data. 
You can also pass handler functions or any method that's defined on a React component to a child component. 
This is how you allow child components to interact with their parent components. You pass methods to a child just like a regular prop. 
It's assigned a name and you have access to that method name under this.props in the child component.

# Lifecycle Methods
React components have several special methods that provide opportunities to perform actions at specific points in the lifecycle of a component. 
These are called lifecycle methods, or lifecycle hooks, and allow you to catch components at certain points in time. 
This can be before they are rendered, before they update, before they receive props, before they unmount, and so on. 
Here is a list of some of the main lifecycle methods: 
* componentWillMount(), 
* componentDidMount(), 
* componentWillReceiveProps(), 
* shouldComponentUpdate(), 
* componentWillUpdate(), 
* componentDidUpdate(), 
* componentWillUnmount()

## componentDidMount
Most web developers, at some point, need to call an API endpoint to retrieve data. 
If you're working with React, it's important to know where to perform this action.

The best practice with React is to place API calls or any calls to your server in the lifecycle method componentDidMount(). 
This method is called after a component is mounted to the DOM. Any calls to setState() here will trigger a re-rendering of your component. 
When you call an API in this method, and set your state with the data that the API returns, it will automatically trigger an update once you receive the data.

### Add Event Listeners
The componentDidMount() method is also the best place to attach any event listeners you need to add for specific functionality. 
React provides a synthetic event system which wraps the native event system present in browsers. 
This means that the synthetic event system behaves exactly the same regardless of the user's browser - even if the native events may behave differently between different browsers.

You've already been using some of these synthetic event handlers such as onClick(). 
React's synthetic event system is great to use for most interactions you'll manage on DOM elements. 
However, if you want to attach an event handler to the document or window objects, you have to do this directly.

## componentWillReceiveProps
Another lifecycle method is componentWillReceiveProps() which is called whenever a component is receiving new props. 
This method receives the new props as an argument, which is usually written as nextProps. 
You can use this argument and compare with this.props and perform actions before the component updates. 
For example, you may call setState() locally before the update is processed.

Another method is componentDidUpdate(), and is called immediately after a component re-renders. 
Note that rendering and mounting are considered different things in the component lifecycle. 
When a page first loads, all components are mounted and this is where methods like componentWillMount() and componentDidMount() are called. 
After this, as state changes, components re-render themselves. The next challenge covers this in more detail.

## shouldComponentUpdate
So far, if any component receives new state or new props, it re-renders itself and all its children. This is usually okay. 
But React provides a lifecycle method you can call when child components receive new state or props, and declare specifically if the components should update or not. 
The method is shouldComponentUpdate(), and it takes nextProps and nextState as parameters.

This method is a useful way to optimize performance. 
For example, the default behavior is that your component re-renders when it receives new props, even if the props haven't changed. 

You can use shouldComponentUpdate() to prevent this by comparing the props. 
The method must return a boolean value that tells React whether or not to update the component. 
You can compare the current props (this.props) to the next props (nextProps) to determine if you need to update or not, and return true or false accordingly.

# Advanced JS in React Render Method
In previous challenges, you learned how to inject JavaScript code into JSX code using curly braces, { }, for tasks like accessing props, passing props, accessing state, inserting comments into your code, and most recently, styling your components. 
These are all common use cases to put JavaScript in JSX, but they aren't the only way that you can utilize JavaScript code in your React components.

You can also write JavaScript directly in your render methods, before the return statement, without inserting it inside of curly braces. 
This is because it is not yet within the JSX code. 
When you want to use a variable later in the JSX code inside the return statement, you place the variable name inside curly braces.

## Render with an If/Else Condition
Another application of using JavaScript to control your rendered view is to tie the elements that are rendered to a condition. 
When the condition is true, one view renders, when it's false, it's a different view. 
You can do this with a standard if/else statement in the render() method of a React component.

### Use && for a More Concise Conditional
The if/else statements worked in the last challenge, but there's a more concise way to achieve the same result. 
Imagine that you are tracking several conditions in a component and you want different elements to render depending on each of these conditions. 
If you write a lot of else if statements to return slightly different UIs, you may repeat code which leaves room for error. 

Instead, you can use the && logical operator to perform conditional logic in a more concise way. 
This is possible because you want to check if a condition is true, and if it is, return some markup. 
Here's an example: {condition && <p>markup</p>}

If the condition is true, the markup will be returned. If the condition is false, the operation will immediately return false after evaluating the condition and return nothing. 
You can include these statements directly in your JSX and string multiple conditions together by writing && after each one. 
This allows you to handle more complex conditional logic in your render() method without repeating a lot of code.

### Use a Ternary Expression for Conditional Rendering
Before moving on to dynamic rendering techniques, there's one last way to use built-in JavaScript conditionals to render what you want: the ternary operator. 
The ternary operator is often utilized as a shortcut for if/else statements in JavaScript. They're not quite as robust as traditional if/else statements, but they are very popular among React developers. 
One reason for this is because of how JSX is compiled, if/else statements can't be inserted directly into JSX code. 
You might have noticed this a couple challenges ago — when an if/else statement was required, it was always outside the return statement. 

Ternary expressions can be an excellent alternative if you want to implement conditional logic within your JSX. 
Recall that a ternary operator has three parts, but you can combine several ternary expressions together. Here's the basic syntax:
condition ? expressionIfTrue : expressionIfFalse

## Return null to Prevent Rendering
There are situations when you may not want to render a child element. React won't render a component if that component's render() method returns null. 

This is useful when you don't want to render components based on conditional logic.

## Render Conditionally from Props
So far, you've seen how to use if/else, &&, null and the ternary operator (condition ? expressionIfTrue : expressionIfFalse) to make conditional decisions about what to render and when. 
However, there's one important topic left to discuss that lets you combine any or all of these concepts with another powerful React feature: props. 

Using props to conditionally render code is very common with React developers — that is, they use the value of a given prop to automatically make decisions about what to render.
In this challenge, you'll set up a child component to make rendering decisions based on props. 
You'll also use the ternary operator, but you can see how several of the other concepts that were covered in the last few challenges might be just as useful in this context.

## Use Array.map() to Dynamically Render Elements
Conditional rendering is useful, but you may need your components to render an unknown number of elements. 
Often in reactive programming, a programmer has no way to know what the state of an application is until runtime, because so much depends on a user's interaction with that program. 
Programmers need to write their code to correctly handle that unknown state ahead of time. Using Array.map() in React illustrates this concept.

For example, you create a simple "To Do List" app. As the programmer, you have no way of knowing how many items a user might have on their list. 
You need to set up your component to dynamically render the correct number of list elements long before someone using the program decides that today is laundry day. 

### Give Sibling Elements a Unique Key Attribute
When you create an array of elements, each one needs a key attribute set to a unique value. 
React uses these keys to keep track of which items are added, changed, or removed. 
This helps make the re-rendering process more efficient when the list is modified in any way. 
Note that keys only need to be unique between sibling elements, they don't need to be globally unique in your application.

## Use Array.filter() to Dynamically Filter an Array
The map array method is a powerful tool that you will use often when working with React. 
Another method related to map is filter, which filters the contents of an array based on a condition, then returns a new array. 

For example, if you have an array of users that all have a property online which can be set to true or false, you can filter only those users that are online by writing:
let onlineUsers = users.filter(user => user.online);

# Render React to the Server
So far, you have been rendering React components on the client. Normally, this is what you will always do. However, there are some use cases where it makes sense to render a React component on the server. 
Since React is a JavaScript view library and you can run JavaScript on the server with Node, this is possible. 
In fact, React provides a renderToString() method you can use for this purpose.

There are two key reasons why rendering on the server may be used in a real world app. 
First, without doing this, your React apps would consist of a relatively empty HTML file and a large bundle of JavaScript when it's initially loaded to the browser. 
This may not be ideal for search engines that are trying to index the content of your pages so people can find you. 
If you render the initial HTML markup on the server and send this to the client, the initial page load contains all of the page's markup which can be crawled by search engines. 
Second, this creates a faster initial page load experience because the rendered HTML is smaller than the JavaScript code of the entire app. 
React will still be able to recognize your app and manage it after the initial load.

