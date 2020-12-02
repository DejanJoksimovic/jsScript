Web, js, basics:
* http:
Hypertext Transfer Protocol (HTTP) is an application-layer protocol for transmitting hypermedia documents, such as HTML. It was designed for communication between web browsers and web servers, but it can also be used for other purposes. HTTP follows a classical client-server model, with a client opening a connection to make a request, then waiting until it receives a response. HTTP is a stateless protocol, meaning that the server does not keep any data (state) between two requests. Though often based on a TCP/IP layer, it can be used on any reliable transport layer; that is, a protocol that doesn't lose messages silently, such as UDP.
* https:
HTTPS (HTTP Secure) is an adaptation of the Hypertext Transfer Protocol (HTTP) for secure communication over a computer network.
* difference between https and http:
HTTPS URLs begin with "https://" and use port 443 by default, whereas HTTP URLs begin with "http://" and use port 80 by default. HTTP is not encrypted and is vulnerable to man-in-the-middle attacks.
* man in the middle attack:
In cryptography and computer security, a man-in-the-middle attack (MITM) is an attack where the attacker secretly relays and possibly alters the communication between two parties who believe they are directly communicating with each other.
* TCP (Transmission Control Protocol) 
is a standard that defines how to establish and maintain a network conversation via which application programs can exchange data
* Response codes types
Successful (200 ok, 201 created…), Client error (400 bad request, 401 unauthorized, 403 forbidden, 404 not found…), Server Error(500 internal error, 501 not implemented…), Informational(100 continue…), Redirection(300 multiple choice…)
* http methods:
GET Should only retrieve data. Sends info via url.
POST Is used to submit an entity to the specified resource.
HEAD Same request like GET but without expecting response body.
DELETE Deletes the specified resource.
* Html and xhtml differences
Both are languages in which web page is written. Html is markup language based and xhtml is xml based. Xhtml is derived from html to match xml standards. Hence xhtml is stricted.
* Rest
Representational State Transfer (REST) is an architectural style that defines a set of constraints and properties based on HTTP.
Constraints:
Uniform Interface - Resource-Based
Stateless
Cacheable
Client-Server
Layered System
Code on Demand (optional)
* Html5 additions: header - footer elements, async attribute, video and audio elements
* Html5 advantages: cleaner code, video and audio support, simple doctype declaration which works in all major browsers, mobile platform support, support for legacy browsers, 
* Json over xml use:
The lightweight approach of JSON can make significant improvements in RESTful APIs working with complex systems. The XML software parsing process can take a long time. One reason for this problem is the DOM manipulation libraries that require more memory to handle large XML files.
The response depends on standard that is used.
* DOCTYPE tells Web browsers what version of HTML your page is using. If the doctype is missing, browser will ignore certain features that browser doesn’t understand (example html 5 footer, header, nav…)
* ajax:
Asynchronous JavaScript + XML. using a number of existing technologies together, including HTML or XHTML, Cascading Style Sheets, JavaScript, The Document Object Model, XML, XSLT, and most importantly the XMLHttpRequest object.
When these technologies are combined in the Ajax model, web applications are able to make quick, incremental updates to the user interface without reloading the entire browser page. Although X in Ajax stands for XML, JSON is used more than XML nowadays because of its many advantages such as being lighter and a part of JavaScript. Both JSON and XML are used for packaging information in Ajax model.
You can send get, post, put and delete requests using ajax. Response could be Json, binary etc.
* XMLHttpRequest has holds statuses (0 request not initialized, 1 established connection, 2 request received, 3 processing request and 4 request finished.
* Ajax request example: 
```js
const http_request = new XMLHttpRequest();
http_request.onreadystatechange = () => (http_request.readyState === 4) && console.log(JSON.parse(http_request.responseText));
http_request.open("GET", "http://www.tutorialspoint.com/json/data.json", true);
http_request.send();
```
* example of downloading within browser:
```js
const xhr = new XMLHttpRequest(); // (A)
xhr.open('GET', 'http://example.com/textfile.txt'); // (B)
xhr.onload = () => { // (C)
  if (xhr.status == 200) {
    processData(xhr.responseText);
  } else {
    assert.fail(new Error(xhr.statusText));
  }
};
xhr.onerror = () => { // (D)
  assert.fail(new Error('Network error'));
};
xhr.send(); // (E)

function processData(str) {
  assert.equal(str, 'Content of textfile.txt\n');
}
```
* On open status set to 1, on send status 2, after receiving response status changed to 4.
* XMLHttpRequest object is a browser level api. It is used to update part of the page without reloading. It handles CORS policy. 
* hoisting
The JavaScript engine treats all variable declarations using “var” as if they are declared at the top of a functional scope (if declared inside a function) or global scope (if declared outside of a function) regardless of where the actual declaration occurs. This essentially is “hoisting”
* closure
The binding which defines the scope of execution. Function declared in a function is a Closure. Inner function can access the parent function variables.
* var and let diff:
The scope of a variable defined with var is function scope or declared outside any function, global. The scope of a variable defined with let is block scope. For example: var declared in a function is available outside of a function. Let declared in a function is not available outside the function. Const also has a block scope.
* Js advantages: client side execution, testing js in console of browser, support major browsers, easy syntax. If we want to limit scope of var, we can use IIFE:
```js
(function() {var a})();
```
Since var is function scope, it will be available only within the function itself.
* Js page redirection 
```js
window.location(url)
```
* Functions are first class objects (can be sent as parameters and can be returned from another function)
* dom:
The Document Object Model (DOM) connects web pages to scripts or programming languages and he represents a document with a logical tree.
* Dom methods
getElementById, removeChild
* xml:
eXtensible Markup Language (XML) is a generic markup language, meta-language. Is not predefined. The primary purpose of the language is the sharing of data across different systems, such as the Internet. XML is realized as a tree.
* json:
Is a syntax for serializing objects, arrays, numbers, string and null. Based on javascript. JavaScript Object Notation
* json and xml diff:
The fundamental difference is that XML is a markup language, whereas JSON is a way of representing objects.
extension (js, json), trailing comma not allowed in json, in js key doesn’t have to be double quoted.
* Idemopotent,  the side-effects of N > 0 identical requests is the same as for a single request
* jsonP
When cross domain request is to be made, use jsonp (better alternative is CORS) JSONP is really a simple trick to overcome the XMLHttpRequest same domain policy. (As you know one cannot send AJAX (XMLHttpRequest) request to a different domain.) So - instead of using XMLHttpRequest we have to use script HTML tags, the ones you usually use to load js files, in order for js to get data from another domain. When using jsonP callback is sent as a parameter. JsonP will receive callback and it will return callbackFun([result])
* Session manager
The session manager creates HTTP sessions and manages the life cycles of HTTP sessions that are associated with the application.
* Doctype
In HTML, the doctype is the required
```html
<!DOCTYPE html> 
```
preamble found at the top of all documents. Its sole purpose is to prevent a browser from switching into so-called “quirks mode” when rendering a document; that is, the 
```html
<!DOCTYPE html>
```
doctype ensures that the browser makes a best-effort attempt at following the relevant specifications, rather than using a different rendering mode that is incompatible with some specifications.
* Semantic
In programing, Semantics refers to the meaning of a piece of code — for example "what effect does running that line of JavaScript have?", or "what purpose or role does that HTML element have" (rather than "what does it look like?".)
* Inline and block elements:
A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).
An inline element does not start on a new line and only takes up as much width as necessary.
* Html form:
The HTML <form> element represents a document section that contains interactive controls for submitting information to a web server.
* css:
Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML.
* CSS Selectors
In CSS, selectors are used to target the HTML elements on our web pages that we want to style.
```css
.a.b selects with both a and b
.a .b selects b where it is decendent of a
.a > .b selects b where it is direct decendent of a
.a, .b selects a or b
```
* CSS Selectors types:
Simple selectors: type, class, id
Attribute selectors: based on attribute values
Pseudo classes: elements that exist in certain state (hovered by mouse, check box that is currently disabled-enabled, element that is the first child..)
Pseudo elements: Match part of the content that is in the certain position in relation to the element.
Combinators: self explanatory
The render tree is sort of like the DOM tree, but doesn't match it exactly. The render tree knows about styles, so if you're hiding a div with display: none, it won't be represented in the render tree.
Multiple selectors: selectors separated by commas.
* CSS cascade: is a mechanism which controls which rule wins
* Specificity is basically a measure of how specific a selector is — how many elements it could match. Id selectors have high specificity. Only way to defeat specificity is !important
Source order is important
* Inheretance: Some attributes are inhereted(font-familiy, color), and some are not(margin, background-image, border). Inheretance could be overwritten with keyword (inherit)
* The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.
* Float property determines if element should be placed left, right of center (inherit)
* Display property: none (not visible), inline, block, inline-block
* visibility: hidden means that unlike display: none, the tag is not visible, but space is allocated for it on the page. The tag is rendered, it just isn't seen on the page.
* Z index determines where will element be in horizontal space, with z index (and with other elements that doesn't have z-index) css stacks is formed
* @media css query is used when a condition should be satisfied in order that rule is applied
* CSS Measurement units: px, %, mm, cm...
* CSS image sprites: An image sprite is a collection of images put into a single image.
A web page with many images can take a long time to load and generates multiple server requests. Using image sprites will reduce the number of server requests and save bandwidth.
* After rendering tree in html, reflow and repaint could be executed. They are usually expensive.(hiding, animation, moving element...)
* Pre-processors, with their advanced features, helped to achieve writing reusable, maintainable and extensible codes in CSS. Sass and LESS are both very powerful CSS extensions. You can think of them as more of a programming language designed to make CSS more maintainable, theme able, and extendable. Both Sass and LESS are backward compatible so you can easily convert your existing CSS files just by renaming the .css file extension to .less or .scss, respectively. LESS is JavaScript based and Sass is Ruby based.
* Design Patterns
Is a general repeatable solution to a commonly occurring problem in software design. 
    * SINGLETON A class of which only a single instance can exist.
    * FACTORY METHOD Creates an instance of several derived classes.
    * PROTOTYPE A fully initialized instance to be copied or cloned.
    * DECORATOR Add responsibilities to objects dynamically.
    * ...
* js function:
Is an basic element in js. Is an object.
* object oriented languages:
inheritance, polymorphism, encapsulation
* js is not an object oriented language
Only inheritance that js supports is Prototypal inheritance. Js is interpreted language. Interpreted languages are not compiled and interpreter (browser) executes them directly.
* reserved words cannot be used to declare a variable, but they can be used as a property of an object
* function or { are always interpreted as statements, only if they are wrapped with (), they are interpreted as an expression statement (expression as a statement)
* after return statement, new line is forbiden in order to prevent accidentally return undesired value
* shadow: inner block x shadow outer x
```js
const x = 1;
assert.equal(x, 1);
{
  const x = 2;
  assert.equal(x, 2);
}
assert.equal(x, 1);
```
* global object can be accessed:
```js
globalObject
```
* scope
The current context of execution.
* Difference between == and ===
With == values are being compared with their values, but not types. With === values are being compared with values and types.
* Imutabillity
Immutable value, after it has been created, it can never change.
* Cookies
An HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to the user's web browser. The browser may store it and send it back with the next request to the same server. Typically, it's used to tell if two requests came from the same browser.
* Js cookie access
Document.cookie
* Cookie, session storage, local storage difference: 
    * LocalStorage: no expiration date, clears only with js or  clear browser cache
    * SessionStorage: stores data only for one session. Data is never transfered to server
    * Cookie: stores data that has to be sent to server. Only cookie is for server side reading as well as for client side. Size less then 4kb
* script async and defer
```html
<script> // embed or reference executable code
<script async> // default false, the executable code will be executed synchronously
<script defer> // code will be executed after the document is parsed
```
* html properties vs attributes
```html
<input type="checkbox" checked=true/>

$('input').prop('checked'); // returns true
$('input').attr('checked'); // returns "checked"

```
* html data- attributes: store additional data on certain html elements
```html
<article
  id="electric-cars"
  data-columns="3"
  data-index-number="12314"
  data-parent="cars">
...
</article>
```
```js
const article = document.querySelector('#electric-cars');
 
article.dataset.columns // "3"
article.dataset.indexNumber // "12314"
article.dataset.parent // "cars"
```
* Scalable Vector Graphics (SVG) is an XML-based vector image format for two-dimensional graphics with support for interactivity and animation
* html head is not rendered in page
* The CSS Reset stylesheet is a basic template to wipe out all built-in styling for HTML elements.
* The Normalize.css stylesheet also removes browser inconsistencies for HTML elements, but instead of removing everything like CSS Reset, normalize.css will preserve some useful defaults
* Native objects are those objects supplied by JavaScript. Examples of these are String, Number, Array, Image, Date, Math, etc.
* Host objects are objects that are supplied to JavaScript by the browser environment. Examples of these are window, document, forms, etc.
* Js var starts with
$, _, and letters.
* Js modules
JavaScript code modules let multiple privileged JavaScript scopes share code. Example of the module is any code that we imported in out current code.
* This js
ES5 bind and ES6 call and apply methods are forwarding this, and by that change the context of function. In strict mode this inside the function will be undefined, in non-strict mode, this will be window or other global object. This in arrow functions represents a global object.
* Promise
The Promise object represents the eventual completion (or failure) of an asynchronous operation, and its resulting value. Promise.all([promise1, promise2, promise3]).then(function(values) {... is a method which is used to call multiple parallel promises. If any of the promises fail in its execution, promise all fails.
* MVC pattern
Model View Controller (MVC) is a software architecture pattern, commonly used to implement user interfaces.
The model defines what data the app should contain
The view defines how the app's data should be displayed
The controller contains logic that updates the model and/or view in response to input from the users of the app
Model updates view, view sends input from user to controller, controller manipulates model and sometimes directly view.
* Source control
Management of changes to documents. A.k.a. version control. 
* Jira
Project tracking software
* TFS 
Version control and project tracking software
* Git
Open source version control system.
* Git hub
Is a web-based hosting service for version control using git
* Javascript functional library: Ramda
* Javascript immutable library: immutable.js
* Javascript selectors: Reselect
* Javascript expressions and statements, An expression produces a value, an example of statement is if statement. If statement is expected, expression could be passed, but not the other way around.
* Hashtag is used as an Anchor in url
* Difference between y.x and y[x]. Second expression is evaluating x before accessing the property
* Elements in array are stored as array properties, using numbers as property names, since .Number cannot be used, we use [number]. Array.length is the same as array[“length”]
* Properties that contain functions are called methods
* Object.keys property lists all properties of an object (if the properties (keys) are strings)
* if the properties are symbols, use Reflect.onwKeys
* Reflect is similiar object as it is Math object that contains built in methods, similar to Object but with some specific differences (like ownKeys..)
* Object.assign copies all properties from one object to another
* Arrays are just a kind of objects specialized for storing sequences of things
* Difference between fun(a) and a.fun(). Second call has this keyword default and it uses this parameters
* Generally speaking, a function is a "subprogram" that can be called by code external (or internal in the case of recursion) to the function. Like the program itself, a function is composed of a sequence of statements called the function body. Values can be passed to a function, and the function will return a value. In JavaScript, functions are first-class objects, because they can have properties and methods just like any other object. What distinguishes them from other objects is that functions can be called. In brief, they are Function objects.
* Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.
* Apply, call , bind: Use .bind() when you want that function to later be called with a certain context, useful in events. Use .call() or .apply() when you want to invoke the function immediately, and modify the context.
* Apply, call and bind are not working with arrow function
* Call and Apply cannot override bind
* When it comes to inheritance, JavaScript only has one construct: objects. Each object has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in this prototype chain.
* We can now use the new operator to create an instance of doSomething() based on this prototype.
* When a function is created in JavaScript, JavaScript engine adds a prototype property to the function. This prototype property is an object (called as prototype object) which has a constructor property by default. Constructor property points back to the function on which prototype object is a property. We can access the function’s prototype property using the syntax functionName.prototype.
* Event propagation: the way to describe order of events in web browser (two kinds: to child and to parent). Stop propagation: event.stopPropagation, event.preventDefault.
* A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
* The ready event occurs after the HTML document has been loaded, while the onload event occurs later, when all content (e.g. images) also has been loaded. The onload event is a standard event in the DOM, while the ready event is specific to jQuery. The purpose of the ready event is that it should occur as early as possible after the document has loaded, so that code that adds functionality to the elements in the page doesn't have to wait for all content to load.
* An event in JavaScript is defined as “things that happen to HTML elements,” and there are a a lot of them. Change, click, mouseover, mouseout, keydown, load. If element doesn’t exist when page is loaded a eventListener problem occur. event.target is a reference to an object that dispatched the event. 
```js
//Event Delegation
function toggleDone (event) {
  if (!event.target.matches(‘input’)) return
  console.log(event.target)
  //We now have the correct input - we can manipulate the node here
}
```
* event delegation: adding event listener to parrent will propagate 
* adding event listener to element will add event listener to all the children (event delagation) 
* process of delegation execution is event bubbling
* difference between target and currentTarget, target is the thing that is clicked, and currentTarget is where you attached eventListener (these two can be different because delegation for example)
* 
* ES6 modules: Named exports, Default exports, Imports are hoisted
* ES6 new functionalities: constants, arrow functions, parameter default values, string interpolation, property shorthand ({x, y} instead of {x:x, y:y}), destructuring (var { op, lhs, rhs } = getASTNode()), class
* DRY – Don’t Repeat Yourself
* KISS – Keep It Simple Stupid
* YAGNI – You Aren’t Gonna Need It
* S – Single Responsibility Principle
* O – Open-Closed Principle
* L – Liskov Substitution Principle
* I – Interface Segregation Principle
* D – Dependency Inversion Principle
* Browserify lets you require('modules') in the browser by bundling up all of your dependencies
* Webpack is an open-source JavaScript module bundler. Its main purpose is to bundle JavaScript files for usage in a browser, yet it is also capable of transforming, bundling, or packaging just about any resource or asset
* RequireJS is a JavaScript file and module loader
* Jenkins is an open source automation server written in Java. Jenkins helps to automate the non-human part of the software development process, with continuous integration and facilitating technical aspects of continuous delivery
* Web sites are made of lots of things — frameworks, libraries, assets, and utilities. Bower manages all these things for you
* Gulp is a javascript task runner that lets you automate tasks like: refreshing browser when save a file, quickly running tests, running code analisys, less-sass to css compilation…
* Unit tests - In computer programming, unit testing is a software testing method by which individual units of source code.
* Integration test complete tests, after unit testing
* Jsx is a syntax extension for javascript, written to be used with React. JSX is compiled to javascript.
* The instanceof operator tests whether the prototype property of a constructor appears anywhere in the prototype chain of an object
* Length of function foo.length
* Function always return undefined if not specific return
* Functions compose from right to left (data flow)
* !!param will transform param in to Boolean value
* Side effect is any unpredictable result (random function, changing variable out of function scope and of course asynchronous response. Program cannot be written without side effects.)
* Pure function doesn’t have side effects. Pure function has referential transparency(if function is to be replaced with its return value, the program behavior would not change).
* For big calculations we can use cache inside of functions and in that way they are pure functions
* Value immutability programs only use values that cannot be changed. (create new values for state of a program)
* Primitive values number, string, Boolean are already immutable (2 = 2.5 // invalid)
* Strings in JS are not arrays. They are array-like objects. You can access element like it is an array, but you cannot change it.
* We use pure functions to achieve immutability
* If we declare array as a constant, we will be able to change it’s content. (const x = [2]; x[0] = 3; //ok)
* Object.freeze() can be used to turn mutable object/array/function to immutable(top level only). 
* Web services exchange data from a server to a client, using an XML format to send requests
* The basic web services platform is XML + HTTP. All the standard web services work using the following components −
a.	SOAP (Simple Object Access Protocol)(to transfer a message)
b.	UDDI (Universal Description, Discovery and Integration)
c.	WSDL (Web Services Description Language) (to describe the availability of device)
d.	XML (to tag the data)
* To achieve immutability we don’t need to copy the entire structure every time, just the previous version.
```js
var x = Object.freeze( [ 2, 3, [4, 5] ] );

// not allowed:
x[0] = 42;

// oops, still allowed:
x[2][0] = 42;
```
* With closure and objects we can achieve the same thing
* Isomorphic, two things are similar in structure but not the same. Two things are isomorphic if you could map from a to b and go back with inverse mapping. Objects and Closures are isomorphic.
* We could use closure to keep track of events of keypresses (this is just an example)
```js
function trackEvent(evt,keypresses = () => []) {
    return function newKeypresses() {
        return [ ...keypresses(), evt ];
    };
}

var keypresses = trackEvent( newEvent1 );

keypresses = trackEvent( newEvent2, keypresses );
```
* Binary recursion – the function calls itself twice
* Memoization, a way for our function to remember (cache) the results
* Mutual recursion – functions calling each other
* Function js programing termin ‘Functor’ is a value that has a utility for using an operator function on that value (each value). (map)
* Filtering can be inclusionary or exclusionary. (keeping or throwing out)
* Secure Sockets Layer (SSL), are cryptographic protocols designed to provide communications security over a computer network
* SSL (and its successor, TLS) is a protocol that operates directly on top of TCP.
* Ssl operates directly on top of tcp protocol.
* When using ssl correctly attacker can only see the ip, approximately amount of data and it can terminate connection. Both sides will know that communication is terminated by third party.
* After building tcp connection, ssl handshake is started. Client send number of specifications. (version of ssl, compression method to use…) After this is done server sends certificate. Having verified the certificate, key Is exchanged. From now on, server and client can compute the key for symmetric encryption. Server verifies that message authentification code is correct and send message that can be correctly decripted.
* Count how many times the function has been called: put inside a function console.count()
* Count how many times has function being called with specific argument console.countl(param)
* Console.table(array) will have a nice print (this is. Working with object also) (to name each value you can pass array of two arrays in which first represents keys and the other one values)
* Use console.group() and console.groupEnd() to organize logging if needed
* RxJs library which is used for handling asynchronous calls using observable squences.  
* Push and pull systems: In pull systems Consumer determines when it receives data from Producer (js functions). In push systems Producer determines when to send data to Consumer (js promises).
* Observable is Producer of multiple values and it is pushing them into Observers (Consumers)
* Generator and Function difference, function returns singular value and generator returns none to infinite potentially.
* Functions, generators, observables – lazy, promises not (f,g,o will not execute unless called)
* Observables are synchronous
* Observable can return multiple values over time, functions can return one value, one time.
* New keyword in js:
    * Creates new object (everything is object in js)
    * It sets prototype
    * It sets this
    * It executes constructor
    * It returns newly created object, or reference to object
* process from when user enters url until page loads
    * extract ip adress from ulr (browser cache, os cache, dns cache, dns data)
    * browser opens tcp connection sends http(s) request
    * server handles request and sends the response
    * browser parse response and render html
* getting data from server
    * Client pull — client asking server for updates at certain regular intervals
    * Server push — server is proactively pushing updates to the client (reverse of client pull)
    * Short polling is an AJAX-based timer that calls at fixed delays whereas Long polling is based on Comet (i.e server will send data to the client when the server event happens with no delay).
    * web sockets is persistent connection between client and server
    * server send event - is mechanism that allows the server to asynchrounously push the data to the client once the client-server connection is esablished. Server decides to send data when new data is available.
* headers (req, resp)
    * expires - date/time after response is condsidered stale
    * date - when message originated
    * age - time in seconds object has been in proxy cache
    * if-modified-since - server will return response only if requested data has been modified after given date
    * DNT - Do Not Track - does user prefer privacy
    * cache-control - speficy caching mechanisms in req and resp
    * transfer-encoding - form of encoding for payload body
    * e-tag - identifier for specific version of resource
    * x-frame-options -  should browser be allowed to render page
* Prefetching allows a browser to silently fetch the necessary resources needed to display content that a user might access in the near future.
* Rxjs pipeable operator (function) takes observables as an input and returns another observable (a pure operation) (subscribing to output observable will also subscribe to input observable
* How to check if object contain property: hasOwnProperty (will return true only if property exist in object itself, not the chain)
* Difference between argument and a parameter (argument is a value passed to a function, parameter is a value that function expects upon execution)
* Function is called a method when is stored in object
* Functions that are not bound to an object are bound to global object
* Js constructor has to be capitalize
* Arguments array has only .length property
* Methods to prototypes can be added to use them in js in general on the project
* Transpiler is different from compiler. It turns code into another code. Compiler turns code into machine code that is understandable. 
* Node.js is asynchronous, event driven Javascript runtime. Js app can be run using node.js. We can use js as server side language.
* Npm is a part of node.js . It is used to install third party packages. Node package manager
* Sass less advantages against css, nested syntax, can define variables, math functions. (var declaration with @)
* Minification, is the process of removing all unnecessary characters from the source codes that are there for readability reasons. This process is used to optimize builds and code size. Uglify js ass a part of node (npm)
* Priority of css selectors is done by specificity. The more specific the selector is it is ‘stronger’.
* Strict mode makes several changes to semantics:
    *   Silent errors throw errors (changing object after freeze, this in function is undefined instead of window)
    * Some optimizations so could run faster
    *   Prohibits syntax for next releases
* Object.freeze(obj). Obj cannot be changed.
* Self invoking function (function() {}())
* Promise.any method is similar to Promise.race but the promise returned by this method does not execute the catch block as soon as any of the promises gets rejected. Instead, it waits until any of the promises resolves. If none of the promises is resolved, catch block will get executed. If any of the promises have resolved first, then block will be executed.
* xpath is query language for xml
* meta tag robot: "noindex", don't index page while web site is in development
* in the html form, every control should have 'name' attribute which is serve the purpose to map params for submit.
* content tag is used for displaying on google search
* image tag in html5 doesn't need to close
* mailto:[mail.com]
* a with name attribute but without href attribute is and anchor
* Build process is an automated sequence of tasks that runs on each push/release.
* build process includes:
    * clean install
    * linter
    * test
    * build
        * transpile (babel, typescript, flow)
        * preprocess (sass, less)
        * uglify (minify)
        * bundle (webpack)
        * push (git)
        * deployment (optional)
* the build tasks execution can be done with CLI (npm)
* (+) operator - converts both values to primitive values (string or number, and does addition)
* Object.is(a, b), is even more strict then ===
* >= and <= are strict
* ?? operator is used when only null or undefined needs to be checked: a ?? b (if a i null or undefined)
* The comma operator (,) evaluates each of its operands (from left to right) and returns the value of the last operand. 
```js
x = (x++, x);
console.log(x);
// expected output: 2
x = (2, 3);
console.log(x);
// expected output: 3
```
It is commonly used in for loop
* JSON doesn't support undefined, only null
* a in b, check if b.a
REACT, REDUX:
* React components and props
Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.
* Redux principals
Single source of truth - the state of your whole application is stored in an object tree within a single store.
State is read-only
Changes are made with pure functions
* React 
Is a declarative, efficient, and flexible JavaScript library for building user interfaces.
* Redux
Redux is a predictable state container for JavaScript apps. Based upon flux (unidirectional data flow) and elm arhitecture(The core idea is that your code is built around a Model of your application state, a way to update your model, and a way to view your model).
* React data flow (unidirectional data flow)
All data in our applications flow in a single direction. In React it flows down the tree from parent to child.
* Virtual dom
The Virtual DOM is an abstraction of the HTML DOM.
* React element
A ReactElement is a light, stateless, immutable, virtual representation of a DOM Element. ReactElements lives in the virtual DOM.
* Thunk
Redux Thunk middleware allows you to write action creators that return a function instead of an action. The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met.
* React component methods
shouldComponentUpdate(), render(),componentDidUpdate()
* ReactDOM is a javascript library containing react specific methods. All the methods deal with the DOM.
* ReactDOM.render() renders JSX.
* JSX substitute for class is className. This is because class is reserved name in js and JSX is interpreted to js
* Events in react are written in camelCase. Html events are written in lowercase.
* If statement is not possible in JSX expression
* Keys should be declared in lists in react. If they are not defined, the order could be wrong when rendering.
* Class names should be written capitalized
* Logic should be written in render method React.
* React if statement can be used before return statement
* This in React refers to instance of the class. Actually it refers to object on which this’s enclosing method (render() )
* Form action decides redirection for submit
* React props is an object
* This.props.children returns single element if there is single element in between react component. For example (<RC>child</RC>) If there are multiple it will return array of elements
* Default props React, even if they are not given as parameters they are defined by default with: SomeComponent.defaultProps = { someProp = “example” }
* This.setState cannot be called inside render method because right after setState the render function is called. It would create infinite loop
* Redux normalize state principals:
* Each type of data gets its own "table" in the state.
* Each "data table" should store the individual items in an object, with the IDs of the items as keys and the items themselves as the values.
* Any references to individual items should be done by storing the item's ID.
* Arrays of IDs should be used to indicate ordering.
* js is single threaded
* event loop
    * setTimeout is provided by the browser, js is calling the function which invokes js function after given time (it pushes callback on taks queue, event loop puts first thing on the stack from task queue if stack is empty)
    * setTimeout with zero time is used to delay callback until stack is cleared
    * ajax request lives in a browser as web api. When it completes, callback is pushed in to the queue, it is picked up by the event loop and when stack is empty callback will execute
    * to define async forEach (which is synchrounous) use setTimeout with delay time 0 each time callback is called
    * Microtasks and Macrotasks: setTimeout, onClick are Macrotasks and all tasks are executed sequentally. Microtask queue is processed after Marcotasks (Promise)
    * event loop (microtasks and macrotasks)
        * Check if there is any task available in the macrotasks queue.
        * If so and this task is running, wait until it is completed before going to the next step. If not, go directly to step 3.
        * Then run all the microtasks that are in the microtask queue.
        * If we add new microtasks during the execution of the microtasks, they are also executed.
    * event loop executions tasks
    * task sources add tasks
    * a task is finished when it reaches return keyword
    
* IIFE imediatelly invoked function expression
```js
function a() {}(); // not good
const foo = function(){}(); // good
(function () {})(); // good
```
* undeclared variable is different from undefined (browser gives an error)
* when use const, varible has to be initialized
* type of undeclared and undefined will return 'undefined'
* type of null is an object - bug in js
* async functions return AsyncFunction object. These functions operate in a separate order then the rest of the code via the event loop, returning implicit Promise as its result. An async function can contain await expression that pauses the execution to wait for the passed promise resolution, then resumes execution.
* use strict is mandatory when using es6
* use const in regex
```js
const regex = 'test';
var re = new RegExp(regex,"g");
someStr.match(re);
```
* You can use store inside a function like this:
```js
import store from 'blaBla/store';
// store is just a:
// return createStore(blaBla...
// ...
  const {
    something,
  } = store.getState();
```
* All primitive values are immutable!
* you cannot change the chars in an array like this:
```js
str[1] = 'a';
```
because strings are primitive values
Also we cannot set property to a number for example
Also we cannot change:
```js
let a = 'test';
a.b = 3;
```
This is a bug in js:
```js
console.log(typeof(null));
```
famous number problem
```js
console.log(0.1 + 0.2 === 0.3); // false
console.log(0.1 + 0.2 === 0.30000000000000004); // true
```
As we move from 0 in either direction, we start losing precision for numbers.
* Infinity and Nan are also numbers
* two different codes:
```js
let banana = function() {}
let result = banana
// will point to the same function in memory
```
```js
let banana = 1
let result = banana
banana = 2;
// will point to 2 different values
// banana is 2
// result is 1
```
* equality in js
```js
typeof NaN // 'number'
NaN === NaN // false - special case
0 === -0 // true - special case
-0 === 0 // true - special case
{} === {} // false
2 === 2 // true
```
* Further calculations with NaN will give you NaN again
* to check if it is NaN
```js
Number.isNaN(val)
Object.is(val, NaN)
val !== val // since the only value for which this is applicable is NaN
```
* if divided with zero
```js
5 / 0
// Infinitity
```
* number is Infinity
```js
Number.isFinite(x) === false;
```
* ceil, floor and round
```js
// ceil smallest
Math.floor(2.9); // 2
// floor largest
Math.ceil(2.9) // 3
// .5 rounded up
Math.round(2.5) // 3
```
* converting to string
```js
String(x); // recomended
'' + x;
x.toString(); // does not work for undefined and null
String(['a', ['b']]); // 'a,b' it will hide some details
```
* Stringifying functions, returns their source code
```js
const a = () => {};
String(a); // "() => {}"
```
* Symbols
```js
// each value of symbol is unique
const mySymbol = Symbol('test');
// can be used when unique prop keys are needed (even if some of them are the same)
const obj = {
    [Symbol('test')]: 'test',
    [Symbol('test')]: 'test1',
};
// if we want to differentiate two similar constants:
const xStatus = Symbol('red');
const yStatus = Symbol('red');
// xStatus !== yStatus
```
* Symbols work with explicit conversion mostly
```js
Boolean(sym) // ok
!sym // ok
Number(sym) // ok
sym * 2 // Type error, similar is for String and toString
```
* throw exception
```js
// one by one throw exits the nested constructs until it encounters a try statement. Execution continues in the coresponding catch statement
```
* finally block executes before try statement ends
```js
() => {
    try {
      throw new Error();
    } finally {
      finallyWasExecuted = true;
    }
    // finally will be executed
```
* import * - import all
* default export cannot export const since it can define multiple values:
```js
const a = 1, b = 2;
```
* 'default' cannot be a variable name, but it can be a export or a property name
* reserved names are allowed to use as property names
* when we use imports, we cannot change the variable exported, but connection is live, meaning that if there is a function that will change exported variable and is exported also, variable can be changed using mentioned function.
* import(x) returns a promise
* undefined and null can be spread inside an object
```js
{...undefined, ...null} // {}
// and also numbers
{...123} // also {}
```
* spread can be used for shallow copying object. If any of the properties values is object, the value will not be shallow copied.
* spread can be used for default data:
```js
const providedData = { data1: 'c', data3: 'd' };
const allData = {data1: 'a', data2: 'b', ...providedData};
```
* we can use '?' to check if we can safely execution part of the code on the right side
```js
const a = { b: 1 };
a?.c?.d // no error, undefined
a?.b // 1
```
* '?' checks for null or undefined
* in operator to check if there is a prop inside an object
```js
const obj = { test: 1 };
'test' in obj // true
```
* delete obj.a will delete a property of object obj
* Object.fromEntries() is doing reverse Object.entries()
* toString function is used to determine how to convert to string, for numbers, valueOf function is used
* Object.freeze makes object immutable (not object in properties of an object)
* non inhereted properties are called own properties
* iterable has next, value and done attr. When iteration is finished, done is true, add
* if you set element length to smaller number then current, you are removing elements
* string is itarable
```js
[...'abc'] === [ 'a', 'b', 'c' ] // numbers are not
```
* you can spread iterable to get an array
```js
const arr = [1,2,3];
// arr.keys() returns iterable
[...arr.keys()]; // [0,1,2]
```
* you can add additional member of an array like this:
```js
const a = [1,2];
a.test = 1;
// result
// [1, 2, test: 1]
// equals:
// 0: 1
// 1: 2
// test: 1
// length: 2
// __proto__ ...
```
* a way to check if something is an array:
```js
Array.isArray(something);
```
* array like objects
```js
{length: 2, 0: 'a', 1: 'b'};
```
* remove first elem of an array:
```js
const arr1 = ['a', 'b', 'c'];
const [, ...arr2] = arr1;
```
* flatMap can be used for filtering and map at the same time
* js Maps allow use of functions, objects and other types as object keys. Object only allow strings and Symbols. Also Maps are iterable, objects are not
* structures that has limited number of memebers use length, others use size
* swap values:
```js
let x = 'a';
let y = 'b';
[x,y] = [y,x]; // swap
```
* generator function example:
```js
function* genFunc1() {
  yield 'a';
  yield 'b';
}
const iterable = genFunc1();
[...iterable] === ['a', 'b'];
```
* the way of using generator functions:
```js
let location = 0;
function* genFunc2() {
  location = 1; yield 'a';
  location = 2; yield 'b';
  location = 3;
}
const iter = genFunc2();
location === 0;
iter.next() === {value: 'a', done: false};
location === 1;
iter.next() === {value: 'b', done: false};
location === 2;
iter.next() === {value: undefined, done: true};
```
* await pauses the current async function and returns from it. Once the awaited result is ready, the execution of the function continues where it left off.
* Many of the user interface mechanisms of browsers also run in the JavaScript process (as tasks). Therefore, long-running JavaScript code can block the user interface.



JS FUNCTIONAL PATTERNS
```js
1.	Order parameter of function

function foo( {x,y} = {} ) {
    console.log( x, y );
}

foo( {
    y: 3
} );

2.	named arguments (if you want to achieve specific naming of arguments)

 function foo( {x,y} = {} ) {
    console.log( x, y );
}

foo( {
    y: 3
} ); 
3.	Assign multiple values from function:
function foo() {
    var retValue1 = 11;
    var retValue2 = 31;
    return [ retValue1, retValue2 ];
}
var [ x, y ] = foo();
4.	No points
function output(txt) {
 console.log( txt );
   }

function printIf( predicate, msg ) {
    if (predicate( msg )) {
        output( msg );
    }
}

function isShortEnough(str) {
    return str.length <= 5;
}

var msg1 = "Hello";
var msg2 = msg1 + " World";

printIf( isShortEnough, msg1 );         // Hello
printIf( isShortEnough, msg2 );

function isLongEnough(str) {
    return !isShortEnough( str );
}

printIf( isLongEnough, msg1 );
printIf( isLongEnough, msg2 );

function not(predicate) {
    return function negated(...args){
        return !predicate( ...args );
    };
}

var isLongEnough = not( isShortEnough );

printIf( isLongEnough, msg2 ); 

5.	Compose
function compose(...fns) {
    return function composed(result){
        // copy the array of functions
        var list = [...fns];

        while (list.length > 0) {
            // take the last function off the end of the list
            // and execute it
            result = list.pop()( result );
        }

        return result;
    };
}
function skipShortWords(words) {
    var filteredWords = [];

    for (let word of words) {
        if (word.length > 4) {
            filteredWords.push( word );
        }
    }

    return filteredWords;
}
var text = "To compose two functions together, pass the \
output of the first function call as the input of the \
second function call.";

var biggerWords = compose( skipShortWords, unique, words );

var wordsUsed = biggerWords( text );
6.	Abstraction
function saveComment(txt) {
    if (txt != "") {
        comments[comments.length] = txt;
    }
}

function trackEvent(evt) {
    if (evt.name !== undefined) {
        events[evt.name] = evt;
    }
}

// abstraction:

function storeData(store,location,value) {
    store[location] = value;
}

function saveComment(txt) {
    if (txt != "") {
        storeData( comments, comments.length, txt );
    }
}

function trackEvent(evt) {
    if (evt.name !== undefined) {
        storeData( events, evt.name, evt );
    }
}

7.	Pure functions with closure
function unary(fn) {
    return function onlyOneArg(arg){
        return fn( arg );
    };
}

New in js:

Array.flat

var nums = [1, [2, [3, [4, 5]]]];
console.log( nums.flat() ); // [1, 2, [3, [4,5]]]
console.log( nums.flat(2) ); // [1, 2, 3, [4,5]]
console.log( nums.flat(Infinity) ); // [1, 2, 3, 4, 5]

Array.flatMap

var nums = [1, 2, 3];
var squares = nums.map( n => [ n, n*n ] )console.log( squares ); // [[1,1],[2,4],[3,9]]
console.log( squares.flat() ); // [1, 1, 2, 4, 3, 9]

var nums = [1, 2, 3];
var makeSquare = n => [ n, n*n ];console.log( nums.flatMap( makeSquare ) ); // [1, 1, 2, 4, 3, 9]


Object.fromEntries

var entries = [["x", 1],["y", 2],["z", 3]];
var obj = Object.fromEntries( entries );console.log( obj ); // {x: 1, y: 2, z: 3}

globalThis

Promise.race([...promises]) returns a promise which resolves as soon as any of the input promises resolves and rejects as soon as any of the promises rejects.

Promise.allSettled method takes an array of promises and resolves once all of the promises have either resolved or rejected. Hence, promise returned by this method does not require catch callback as it will always resolve. The then callback receives the status and value of each promise in the order of their appearance.

var p1 = () => new Promise(
  (resolve, reject) => setTimeout( () => resolve( 'val1' ), 2000 )
);
 
var p2 = () => new Promise(
  (resolve, reject) => setTimeout( () => resolve( 'val2' ), 2000 )
); 
 
var p3 = () => new Promise(
  (resolve, reject) => setTimeout( () => reject( 'err3' ), 2000 )
);var p = Promise.allSettled( [p1(), p2(), p3()] ).then(
  ( values ) => console.log( values )
);// Output
[ {status: "fulfilled", value: "val1"}
  {status: "fulfilled", value: "val2"}
  {status: "rejected", value: "err3"}
]
```

# JS Chanlenges:
```js
const twoSum = function(nums, target) {
    return nums.reduce((acc, curr, index) => {
        const candidate = nums.slice(index + 1).findIndex(elem => elem + curr === target);
        if (candidate !== -1) {
            acc.push(index, candidate + index + 1);
        }
        return acc;
    }, []);
};
/*
twoSum([2,0,7,11,15], 9)
result: [0,2]
*/


const reverse = function(x) {
 const value = parseInt(x.toString().split('').reverse().join(''));
 switch(true) {
  case value > 2**31 - 1:
    return 0;           
  case x < 0:
    return -1 * value;
  default:
    return value
  }
};
/*
reverse(321)
result: 123
note: if reversed overflows [−2**32,  2**31 − 1], should return 0
this can be used for isPalindrome (x === reverse(x))
*/

const romanToInt = function(s) {
  return s.split('').reduce((acc, curr, index, arr) => {
    switch(true) {
      case curr === 'I' && ['V', 'X'].includes(arr[index + 1]):
      case curr === 'X' && ['L', 'C'].includes(arr[index + 1]):
      case curr === 'C' && ['D', 'M'].includes(arr[index + 1]):
          return { ...acc, previous: curr };
          default:
            return { num: getNum(acc, curr), previous: null };
    }
  }, { num: 0, previous: null }).num;
};

const getNum = (acc, curr) => {
  const { num, previous } = acc;
  const sum = num + romanNumerals[curr];
  return previous ? sum - romanNumerals[previous] : sum;
}
  
const romanNumerals = {
  I: 1,
  V: 5,
  X: 10,
  L: 50,
  C: 100,
  D: 500,
  M: 1000,
};
/*
romanToInt('IX')
result: 9
*/

const longestCommonPrefix = function(strs) {
    if (!strs.length) {
        return '';
    }
    const [first, ...rest] = strs;
    const shortestLength = rest.reduce((acc, curr) => {
        return curr.length < acc.length ? curr : acc;
    }, first);
    return shortestLength.split('').reduce((acc, curr, index) => {
        if (!acc.contains) {
            return acc;
        }
        const contains = strs.every(str => str[index] === curr);
        return contains ? { prefix: acc.prefix + curr, contains: true } : { ...acc, contains: false };
    }, { prefix: '', contains: true }).prefix;
};
/*
longestCommonPrefix(["aca","cba"]);
result ''
longestCommonPrefix(["flower","flow","flight"]);
result 'fl'
longestCommonPrefix([]);
result ''
*/

const isValidParentheses = function(s) {
    if (!s) return true;
    const res = s.split('').reduce((acc, curr) => {
        switch(true) {
            case ['(', '{', '['].includes(curr):
                return { ...acc, soFar:  [ ...acc.soFar, curr ] }
            case [')', '}', ']'].includes(curr):
                const oldSoFar = acc.soFar;
                const appropriate = oldSoFar[oldSoFar.length - 1] === closedOposite[curr];
                const newAcc = appropriate ? { ...acc, soFar: oldSoFar.slice(0, oldSoFar.length - 1) }  :  { ...acc, eliminator: true };
                return newAcc;
        default:
            return true;
        }
    }, { soFar: [], eliminator: false });
    return !res.eliminator && !res.soFar.length;
}

const closedOposite = {
  '}': '{',
  ')': '(',
  ']': '[',
};
/*
isValidParentheses('()'); // true
isValidParentheses('({})'); // true
isValidParentheses('([)]'); // false
*/

const strStr = function(haystack, needle) {
    if (needle === '') return 0;
    return haystack.split('').findIndex((char, indexF, array) => {
        return needle.split('').reduce((acc, curr, indexR) => {
            return acc && array[indexF + indexR] === curr;
        }, true);
    });
};

/*
// finds first index
strStr('hello', 'll'); // 2
strStr('aaa', 'bb'); // 0
*/

const searchInsert = function(nums, target) {
    const index = nums.findIndex(num => {
        const equal = num === target;
        const larger = num > target;
        return equal || larger;
    });
    return index === -1 ? nums.length : index;
};

/*
searchInsert([1,3,5,6], 5) // 2
searchInsert([1,3,5,6], 2) // 1
search([1,3,5,6], 7) // 4
*/

// with looking into solutions
const maxSubArraySum = nums => {
   return nums.reduce((acc, curr) => {
       const prev = Math.max(acc.prev + curr, curr);
        return {
            prev,
            max: Math.max(acc.max, prev),
        };
    }, { prev: -Number.MAX_VALUE, max: -Number.MAX_VALUE }).max;
  }

/*
maxSubArray([-2,1,-3,4,-1,2,1,-5,4]) // 6
*/

const lengthOfLastWord = function(s) {
    if (!s) {
        return 0;
    }
    const arr = s.split(' ').reverse();
    const candidate = arr.find(elem => elem.length);
    return candidate ? candidate.length : 0;
};
/*
lengthOfLastWord("Hello World") // 5
*/

const plusOne = function(digits) {
    const digitsReversed = digits.reverse();
    return digitsReversed.reduce((acc, curr, index, arr) => {
        const newDigit = curr + acc.add;
        if (newDigit !== 10) {
            return { digits: [...acc.digits, newDigit], add: 0 };
        }
        if (arr.length === index + 1) {
            return { digits: [...acc.digits, 0, 1] };
        }
        return { digits: [...acc.digits, 0], add: 1 };
    }, { digits: [], add: 1}).digits.reverse();
};
/*
    plusOne([1,2,3]) // [1,2,4]
    plusOne([9,9]) // [1,0,0]
*/

const mySqrt = function(x, sqrt = 1) {
    const candidate = sqrt * sqrt;
    if (candidate > x) return sqrt - 1;
    return mySqrt(x, sqrt + 1);
};

/*
    mySqrt(8) // 2
    mySqrt(9) // 3
*/

const isSameTree = (p, q) => {
    if (!p && !q) return true;
    if (!p || !q || p.val !== q.val) return false;
    return isSameTree(p.left, q.left) && isSameTree(p.right, q.right);
};
/*
    isSameTree([1,2,3], [1,2,3]) // true
    isSameTree([1,2,null], [1,2,3]) // false
*/
```


