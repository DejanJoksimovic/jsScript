# Web:
## http:
Hypertext Transfer Protocol (HTTP) is an application-layer protocol for transmitting hypermedia documents, such as HTML. It was designed for communication between web browsers and web servers, but it can also be used for other purposes. HTTP follows a classical client-server model, with a client opening a connection to make a request, then waiting until it receives a response. HTTP is a stateless protocol, meaning that the server does not keep any data (state) between two requests. Though often based on a TCP/IP layer, it can be used on any reliable transport layer; that is, a protocol that doesn't lose messages silently, such as UDP.
## https:
HTTPS (HTTP Secure) is an adaptation of the Hypertext Transfer Protocol (HTTP) for secure communication over a computer network.
## difference between https and http:
HTTPS URLs begin with "https://" and use port 443 by  default, whereas HTTP URLs begin with "http://" and use port 80 by default. HTTP is not encrypted and is vulnerable to man-in-the-middle attacks.
## man in the middle attack:
In cryptography and computer security, a man-in-the-middle attack (MITM) is an attack where the attacker secretly relays and possibly alters the communication between two parties who believe they are directly communicating with each other.
## TCP (Transmission Control Protocol)
is a standard that defines how to establish and maintain a network conversation via which application programs can exchange data
## Response codes types
Successful (200 ok, 201 created…), Client error (400 bad request, 401 unauthorized, 403 forbidden, 404 not found…), Server Error(500 internal error, 501 not implemented…), Informational(100 continue…), Redirection(300 multiple choice…)
## http methods:
GET Should only retrieve data. Sends info via url.
POST Is used to submit an entity to the specified resource.
HEAD Same request like GET but without expecting response body.
DELETE Deletes the specified resource.
## Html and xhtml differences
Both are languages in which web page is written. Html is markup language based and xhtml is xml based. Xhtml is derived from html to match xml standards. Hence xhtml is stricted.
## GraphQL
a query language for APIs
## Rest
Representational State Transfer (REST) is an architectural style that defines a set of constraints and properties based on HTTP.
### REST Constraints:
Uniform Interface - Resource-Based
Stateless
Cacheable
Client-Server
Layered System
Code on Demand (optional)
## Html5 additions:
header - footer elements, async attribute, video and audio elements
## Html5 advantages:
cleaner code, video and audio support, simple doctype declaration which works in all major browsers, mobile platform support, support for legacy browsers, 
## Json over xml use:
The lightweight approach of JSON can make significant improvements in RESTful APIs working with complex systems. The XML software parsing process can take a long time. One reason for this problem is the DOM manipulation libraries that require more memory to handle large XML files.
The response depends on standard that is used.
## Doctype
tells Web browsers what version of HTML your page is using. If the doctype is missing, browser will ignore certain features that browser doesn’t understand (example html 5 footer, header, nav…)
In HTML, the doctype is the required
```html
<!DOCTYPE html> 
```
preamble found at the top of all documents. Its sole purpose is to prevent a browser from switching into so-called “quirks mode” when rendering a document; that is, the 
```html
<!DOCTYPE html>
```
doctype ensures that the browser makes a best-effort attempt at following the relevant specifications, rather than using a different rendering mode that is incompatible with some specifications.

## ajax:
Asynchronous JavaScript + XML. using a number of existing technologies together, including HTML or XHTML, Cascading Style Sheets, JavaScript, The Document Object Model, XML, XSLT, and most importantly the XMLHttpRequest object.
When these technologies are combined in the Ajax model, web applications are able to make quick, incremental updates to the user interface without reloading the entire browser page. Although X in Ajax stands for XML, JSON is used more than XML nowadays because of its many advantages such as being lighter and a part of JavaScript. Both JSON and XML are used for packaging information in Ajax model.
You can send get, post, put and delete requests using ajax. Response could be Json, binary etc.
## XMLHttpRequest
has holds statuses (0 request not initialized, 1 established connection, 2 request received, 3 processing request and 4 request finished.
## Ajax request example: 
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
On open status set to 1, on send status 2, after receiving response status changed to 4.
## XMLHttpRequest object
is a browser level api. It is used to update part of the page without reloading. It handles CORS policy.
## dom:
The Document Object Model (DOM) connects web pages to scripts or programming languages and he represents a document with a logical tree.
## Dom methods
getElementById, removeChild
## xml:
eXtensible Markup Language (XML) is a generic markup language, meta-language. Is not predefined. The primary purpose of the language is the sharing of data across different systems, such as the Internet. XML is realized as a tree.
## json:
Is a syntax for serializing objects, arrays, numbers, string and null. Based on javascript. JavaScript Object Notation
## json and xml diff:
The fundamental difference is that XML is a markup language, whereas JSON is a way of representing objects.
extension (js, json), trailing comma not allowed in json, in js key doesn’t have to be double quoted.

## jsonP
When cross domain request is to be made, use jsonp (better alternative is CORS) JSONP is really a simple trick to overcome the XMLHttpRequest same domain policy. (As you know one cannot send AJAX (XMLHttpRequest) request to a different domain.) So - instead of using XMLHttpRequest we have to use script HTML tags, the ones you usually use to load js files, in order for js to get data from another domain. When using jsonP callback is sent as a parameter. JsonP will receive callback and it will return callbackFun([result])
## Session manager
The session manager creates HTTP sessions and manages the life cycles of HTTP sessions that are associated with the application.
## Semantic
In programing, Semantics refers to the meaning of a piece of code — for example "what effect does running that line of JavaScript have?", or "what purpose or role does that HTML element have" (rather than "what does it look like?".)
```html
<footer>
<header>
<nav>
<section>
...
```
## Html form:
The HTML <form> element represents a document section that contains interactive controls for submitting information to a web server.
Form can be submitted with submit() using js
## Cookie, session storage, local storage difference: 
### LocalStorage:
no expiration date, clears only with js or  clear browser cache
### SessionStorage:
stores data only for one session. Data is never transfered to server
### Cookie:
stores data that has to be sent to server. Only cookie is for server side reading as well as for client side. Size less then 4kb
## script async and defer
```html
<script> // embed or reference executable code
<script async> // default false, the executable code will be executed synchronously
<script defer> // code will be executed after the document is parsed
```
## html properties vs attributes
```html
<input type="checkbox" checked=true/>

$('input').prop('checked'); // returns true
$('input').attr('checked'); // returns "checked"

```
## html data- attributes:
store additional data on certain html elements
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
## Scalable Vector Graphics (SVG)
is an XML-based vector image format for two-dimensional graphics with support for interactivity and animation
## html head
is not rendered in page
## Hashtag
is used as an Anchor in url
## The ready event occurs
after the HTML document has been loaded, while the onload event occurs later, when all content (e.g. images) also has been loaded. The onload event is a standard event in the DOM, while the ready event is specific to jQuery. The purpose of the ready event is that it should occur as early as possible after the document has loaded, so that code that adds functionality to the elements in the page doesn't have to wait for all content to load. ready is similar to onDocumentReady
## Web services exchange data from a server to a client, using an XML format to send requests
## The basic web services
platform is XML + HTTP. All the standard web services work using the following components −
a.	SOAP (Simple Object Access Protocol)(to transfer a message)
b.	UDDI (Universal Description, Discovery and Integration)
c.	WSDL (Web Services Description Language) (to describe the availability of device)
d.	XML (to tag the data)
## process from when user enters url until page loads
  * extract ip adress from ulr (browser cache, os cache, dns cache, dns data)
  * browser opens tcp connection sends http(s) request
  * server handles request and sends the response
  * browser parse response and render html
## getting data from server
  * Client pull — client asking server for updates at certain regular intervals
  * Server push — server is proactively pushing updates to the client (revers of client pull)
  * Short polling is an AJAX-based timer that calls at fixed delays whereas Lon polling is based on Comet (i.e server will send data to the client when th server event happens with no delay).
  * web sockets is persistent connection between client and server
  * server send event - is mechanism that allows the server to asynchrounousl push the data to the client once the client-server connection is esablished  Server decides to send data when new data is available.
## headers (req, resp)
  * expires - date/time after response is condsidered stale
  * date - when message originated
  * age - time in seconds object has been in proxy cache
  * if-modified-since - server will return response only if requested data ha been modified after given date
  * DNT - Do Not Track - does user prefer privacy
  * cache-control - speficy caching mechanisms in req and resp
  * transfer-encoding - form of encoding for payload body
  * e-tag - identifier for specific version of resource
  * x-frame-options -  should browser be allowed to render page
## Prefetching
allows a browser to silently fetch the necessary resources needed to display content that a user might access in the near future.
## xpath
is query language for xml
## meta tag robot
"noindex", don't index page while web site is in development
## in the html form, every control should have 'name' attribute which is serve the purpose to map params for submit.
## content tag is used for displaying on google search
## image tag in html5 doesn't need to close
## mailto:[mail.com]
## a with name attribute but without href attribute is and anchor
## viewState vs sessionState
* 'ViewState' is specific to a page in a session.
* 'SessionState' is specific to user specific data that can be accessed across all pages in the web application.
## window.postMessage
* method safely enables cross-origin communication between window objects
```js
postMessage(message, targetOrigin)
// message - data to send
// targetOrigin '*' should be avoided, will be available to all window objects
```
* window can listen to these messages:
```js
window.addEventListener("message", (event) => {
  if (event.origin !== "http://example.org:8080")
    return;

  // …
}, false);
```
## IndexedDB
is a database that is built into a browser
## headless browser
Web browser without a graphical user interface













# CSS:

## adaptive vs responsive css design:
A responsive design can change its layout and appearance based on the screen size of the device it's accessed on, from a large desktop computer to a small mobile phone. An adaptive design requires the creation of a different layout for each device the website will be accessed on

## Inline and block elements:
A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).
An inline element does not start on a new line and only takes up as much width as necessary.
## CSS:
Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML.
## CSS Selectors
In CSS, selectors are used to target the HTML elements on our web pages that we want to style.
```css
.a.b selects with both a and b
.a .b selects b where it is decendent of a
.a > .b selects b where it is direct decendent of a
.a, .b selects a or b
```
## Units
- vh: 1% of the viewport's height
- vw: 1% of the viewport's width
- pt: somewhat larger then px
- in: inches
- cm: cm
- mm: mm
- em: font size of parrent
- rem: font size of root element
## Bubling
When an event happens on an element, it first runs the handlers on it, then on its parent, then all the way up on other ancestors.

## CSS Selectors types:
- Simple selectors: type, class, id
- Attribute selectors: based on attribute values
- Pseudo classes: elements that exist in certain state (hovered by mouse, check box that is currently disabled-enabled, element that is the first child..)
- Pseudo elements: Match part of the content that is in the certain position in relation to the element. 
```css
.example :is(h2, h4, :hover) {
  color: red;
}
/* is selector can have invalid parameter and it will ignore it */
/* is have higher specificity then some selectors */
:where(h2, h4, :hover)
/* where works very similar, but has zero specificity */
.example:has(img) {
  background: blue;
}
/* has selector selects .example element if element has an image*/
```
- Combinators: self explanatory
- The render tree is sort of like the DOM tree, but doesn't match it exactly. The render tree knows about styles, so if you're hiding a div with display: none, it won't be represented in the render tree.
- Multiple selectors: selectors separated by commas.
## position
- static: The top, right, bottom, left, and z-index properties have no effect
- relative: Offset relative to itself based on the values of top, right, bottom, and left
- absolute:  No space is created for the element in the page layout. Its final position is determined by the values of top, right, bottom, and left.
- fixed:  No space is created for the element in the page layout. The element is positioned relative to its initial containing block, which is the viewport in the case of visual media. Its final position is determined by the values of top, right, bottom, and left.
- sticky: Offset relative to its nearest scrolling ancestor and containing block (nearest block-level ancestor), including table-related elements, based on the values of top, right, bottom, and left. The offset does not affect the position of any other elements.
## CSS cascade: is a mechanism which controls which rule wins
## Specificity
is basically a measure of how specific a selector is — how many elements it could match. Id selectors have high specificity. Only way to defeat specificity is !important
Source order is important
## Inheretance:
Some attributes are inhereted(font-familiy, color), and some are not(margin, background-image, border). Inheretance could be overwritten with keyword (inherit)
## The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.
## Float property
determines if element should be placed left, right of center (inherit)
## Display property:
none (not visible), inline, block, inline-block
## visibility:
hidden means that unlike display: none, the tag is not visible, but space is allocated for it on the page. The tag is rendered, it just isn't seen on the page.
## Z index
determines where will element be in horizontal space, with z index (and with other elements that doesn't have z-index) css stacks is formed
## @media css query
is used when a condition should be satisfied in order that rule is applied
## CSS image sprites
An image sprite is a collection of images put into a single image.
## CSS Measurement units
px, %, mm, cm...
A web page with many images can take a long time to load and generates multiple server requests. Using image sprites will reduce the number of server requests and save bandwidth.
## After rendering tree in html, reflow and repaint could be executed.
They are usually expensive.(hiding, animation, moving element...)
## Pre-processors
with their advanced features, helped to achieve writing reusable, maintainable and extensible codes in CSS. Sass and LESS are both very powerful CSS extensions. You can think of them as more of a programming language designed to make CSS more maintainable, theme able, and extendable. Both Sass and LESS are backward compatible so you can easily convert your existing CSS files just by renaming the .css file extension to .less or .scss, respectively. LESS is JavaScript based and Sass is Ruby based.
## The CSS Reset stylesheet
is a basic template to wipe out all built-in styling for HTML elements.
## The Normalize.css
stylesheet also removes browser inconsistencies for HTML elements, but instead of removing everything like CSS Reset, normalize.css will preserve some useful defaults
## Sass less
advantages against css, nested syntax, can define variables, math functions. (var declaration with @)
## + selector
b element that directly follow element a
```css
a + b
```
## ~ selector
all b elements that follow element a
```css
a ~ b
```
## first:child selector
first p element
```css
  p:first-child;
```
## only-child selector
element for which parents are p
```css
  p:only-child;
```
## last-child selector
last child
```css
  p:last-child;
```
## nth-child selector
second child
```css
  p:nth-child(2);
```
## nth-last-child selector
second last child
```css
  p:nth-last-child(2);
```
## first-of-type selector
self explanatory
```css
  p:first-of-type;
```
## nth-of-type selector
self explanatory
```css
  p:nth-of-type;
```
## nth-of-type(An+B) selector
self explanatory (different combinations)
```css
  p:nth-of-type(An+B);
```
## last-of-type selector
self explanatory
```css
  p:last-of-type;
```
## empty selector
selects elements that don't have any other elements inside
```css
  p:empty;
```
## not selector
self explanatory
```css
  p:not(X);

```
## attribute selector
selects elements with type
```css
[type]
a[type]
[type="someType"]
[type^="startsWith"]
[type$="endsWith"]
[type*="contains"]
```


## Flexbox
justify content align items horizontally
```css
a {
  display: flex;
  justify-content: flex-end;
}
```
align-items align items vertically
```css
a {
  display: flex;
  align-items: flex-start;
}
```
flex-direction changes direction
```css
a {
  display: flex;
  flex-direction: row;
}
```
order
```css
a {
  display: flex;
  order: 1
}
```
align-self is the same as align-items for single elem
```css
a {
align-self: flex-end
}
```
flex-wrap spread items
```css
a {
  display: flex;
flex-wrap: wrap
}
```
flex-flow is combination of flex-direction and flex-wrap
align-content to align multiple lines
## Grid
grid-column-start - grid-column-end (fill the grid columns)
grid-column
grid-row
grid-area (column + row)
grid-template
## CSS import and link
two common ways to add external css to html










# General:
## Difference between functional and object oriented programming
Object oriented programming is focusing on 'how system' looks using interfaces and classes as entities, while functional principle is focusing on functional use of the system (something like that :) )
## Memory leak
A memory leak is the gradual deterioration of system performance that occurs over time as the result of the fragmentation of a computer's RAM due to poorly designed or programmed applications that fail to free up memory segments when they are no longer needed.
## Event driven arhitecture
- publisher send events that are immutable and it doesn't care if events are handled or not
- broker keeps records of all events
- subscribers subscribe to broker and can choose to handle certain events
## Design Patterns
Is a general repeatable solution to a commonly occurring problem in software design. 
    * SINGLETON A class of which only a single instance can exist.
    * OBSERVER An object called subject maintains the list of dependents, called observers and notifies them automatically of any state changes.
    * FACADE is trying to hide underlying complexity, allowing you to work with api.
    * FACTORY METHOD Creates an instance of several derived classes.
    * PROTOTYPE A fully initialized instance to be copied or cloned.
    * DECORATOR Add responsibilities to objects dynamically.
    * ...
## SOLID principles
* Single Responsibility - Each module should be responsible to one, and only one, actor (actor - user - stakeholder - module)
* Open-Closed - should be open for extension, but closed for modification
* Liskov Substitution - build software systems from interchangeable parts
* Interface Segregation - avoid depending on things that they don’t use
* Dependency injection - enables you to replace dependencies without changing the class that uses them
## object oriented languages:
inheritance, polymorphism, encapsulation
## Cookies
An HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to the user's web browser. The browser may store it and send it back with the next request to the same server. Typically, it's used to tell if two requests came from the same browser.
## MVC pattern
Model View Controller (MVC) is a software architecture pattern, commonly used to implement user interfaces.
The model defines what data the app should contain
The view defines how the app's data should be displayed
The controller contains logic that updates the model and/or view in response to input from the users of the app
Model updates view, view sends input from user to controller, controller manipulates model and sometimes directly view.
## Source control
Management of changes to documents. A.k.a. version control. 
## Jira
Project tracking software
## TFS 
Version control and project tracking software
## Git
Open source version control system.
## Git hub
Is a web-based hosting service for version control using git
## Jenkins
is an open source automation server written in Java. Jenkins helps to automate the non-human part of the software development process, with continuous integration and facilitating technical aspects of continuous delivery
## Jenkins Blue Ocean
Blue Ocean is Jenkins interface
## Jenkins pipeline tips
- keep your groovy language syntax as simple as possible (just execute shell scripts)
- use plugins whenever you can
- avoid using non-serializable objects (use plugins, then it shouldn't matter)
## Bower
Web sites are made of lots of things — frameworks, libraries, assets, and utilities. Bower manages all these things for you
## Gulp
is a javascript task runner that lets you automate tasks like: refreshing browser when save a file, quickly running tests, running code analisys, less-sass to css compilation…
## Unit tests
In computer programming, unit testing is a software testing method by which individual units of source code.
## Integration test
complete tests, after unit testing
## Secure Sockets Layer (SSL)
are cryptographic protocols designed to provide communications security over a computer network
## SSL
(and its successor, TLS) is a protocol that operates directly on top of TCP.
* Ssl operates directly on top of tcp protocol.
* When using ssl correctly attacker can only see the ip, approximately amount of data and it can terminate connection. Both sides will know that communication is terminated by third party.
* After building tcp connection, ssl handshake is started. Client send number of specifications. (version of ssl, compression method to use…) After this is done server sends certificate. Having verified the certificate, key Is exchanged. From now on, server and client can compute the key for symmetric encryption. Server verifies that message authentification code is correct and send message that can be correctly decripted.
## CDN stands for Content Delivery Network.
CDNs deliver cached, static content from a network of servers across the globe.
## monorepo
A monorepo (mono repository) is a single repository that stores all of your code and assets for every project. It is not a good idea to use git with monorepo, it gets really complex to use.
## monolith repo
A monolith repo is usually referred to single project repo.

## Node JS is not multithreaded but imitates this

## husky adds pre commit
```bash
npx husky add .husky/pre-commit "npm test"
git add .husky/pre-commit
git commit -m "Keep calm and commit"
# `npm test` will run
```
## ramda
set of useful js functions (functional approach) https://ramdajs.com/docs/#add
## A CSS Injection vulnerability
involves the ability to inject arbitrary CSS code in the context of a trusted web site which is rendered inside a victim's browser
## Polyfilling
Taking the definition of a newer feature and producing code that offers equivalent behavior, but is able to run in older JS environments.
## Transpiling
Using a tool that converts your newer code into older code equivalents
## NVMRC
- add .nvmrc to root of your project
- content: v18.12.1
- nvm use command will change to nvm version specified
## Service worker 
Service workers essentially act as proxy servers that sit between web applications, the browser, and the network (when available). They are intended, among other things, to enable the creation of effective offline experiences, intercept network requests and take appropriate action based on whether the network is available, and update assets residing on the server.








# Testing:
## Loosely coupled
Modules should be as independent as possible from other modules, so that changes to module don’t heavily impact other modules.
## Highly cohesive
We want to design components that are self-contained: independent, and with a single, well-defined purpose
## Test doubles:
- fake: Fakes are objects that have working implementations
- stub: Stubs are objects that return predefined values 
- spy: Spy is a test double that records the invocations of its methods
- mock: Mocks are combinations of stubs and spies
## jest custom report
Create custom-reporter.js
```js
class CustomReporter {
    constructor(globalConfig, options) {
      this._globalConfig = globalConfig;
      this._options = options;
    }
  
    onRunComplete(contexts, results) {
      console.log('KRENUO')
      if (results.numFailedTests > 0) {
        console.log('Failed Files:');
        results.testResults.forEach(testResult => {
          if (testResult.numFailingTests > 0) {
            console.log(11111, testResult)
            console.log(testResult.testFilePath);
          }
        });
      }
    }
  }
  
  module.exports = CustomReporter;
```
in jest.config:
```json
  // Use this configuration option to add custom reporters to Jest
  reporters: ["default", "<rootDir>/src/custom-reporter.js"],
```







# Build process:
## Transpiler is different from compiler.
It turns code into another code. Compiler turns code into machine code that is understandable. Example: from es6 to es5
## Package managers
are tools that allow you to manage dependencies in your project. (yarn and npm, both of them are clients for npm package registry)
## Node.js
is asynchronous, event driven Javascript runtime. Js app can be run using node.js. We can use js as server side language.
## Npm
is a part of node.js . It is used to install third party packages. Node package manager
## Minification
is the process of removing all unnecessary characters from the source codes that are there for readability reasons. This process is used to optimize builds and code size. Uglify js ass a part of node (npm)
## Build process
is an automated sequence of tasks that runs on each push/release.
## build process includes:
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
## the build tasks execution can be done with CLI (npm)
## Difference between tilde(~) and caret(^)
1.0.2
* 1 - major
* 0 - minor
* 2 - patch
### ~
For the specified minor version, ~ will match the most recent patch version.
### ^
For the specified major version, ^ will match the most recent minor version.













# JS:
### &&=, ||=
```js
if (x) {
  x = y
}
// the same thing as 
x &&= y
```
## Loop invariant
A loop invariant is some predicate (condition) that holds for every iteration of the loop
```js
int j = 9;
for(int i=0; i<10; i++)  
j--;
```
In this example it is true (for every iteration) that i + j == 9.
A weaker invariant that is also true is that i >= 0 && i <= 10.
One may get confused between the loop invariant, and the loop conditional ( the condition which controls termination of the loop ).
The loop invariant must be true:
before the loop starts
before each iteration of the loop
after the loop terminates
( although it can temporarily be false during the body of the loop )
## deep clone
- spread will only create new ref for first level
- simplest way: 
```js
JSON.parse(JSON.stringify(x))
```
## check if
- Array (Array.isArray(something) or something.constructor === Array)
- Boolean, Number, String (typeof something === 'boolean')
- Function (something && {}.toString.call(something) === '[object Function]') TRICKY
- Object (typeof something === 'object' && something !== null && !Array.isArray(something))
## classes
- Class is a function under the hood. typeof class is function (it is the same as its constructor)
- Object.getOwnPropertyNames of __proto__ will list all methods and constructor (not from parent class)
- Object.getOwnPropertyNames of class instance will list all public fields (also from parent class)
- Classes are not just syntatic sugar (though very similar behavour can be acheived with functions) IsClassConstructor is set true on classes
- classes always works in strict mode
- classes (as functions) are first class citizens
- if we use getter and/or setter we use those like they are functions but they are invoked with "= something", not "(something)"
- we can calculate method name with [expression]
- methods can handle 'this' more secure (if we call the class method from setTimeout 'this' wont be lost) if we use arrow function
- expression that evaluates to class can be used after extends keyword
- we can access extended class via super key word. Constructor has to call extended class constructor or there will be an error
- arrow functions cannot be accessed via super
- it is not mandatory to ovveride extended class constructor
- super works thanks to HOMEOBJECT that knows how to resolve parent class
- static functions are accesible from class directly (Test.staticMethod()) without creating an instance of class
- 'this' in classes is equal to class itself
- 'this' for static method is calculated via the “object before dot” rule
- all inheretance is possible because of prototypes
- protected props should be used within the class and subclasses
- convention is to use underscore to mark this is protected (since protected doesn't exist in js as a language)
- private props can only be used within the class, in js there is accepted proposal to use # as a var prefix to make variable private
- if we want to have read only prop, we simply not implement setter
- Built in classes are extendible also, such as Array, String ...
- if we extend built in class, and method returns new array for example, it will return extended array
- Built in classes don't inherite static methods (Array and Date extend object, not static methods from object)
- someClassObject instanceOf class // true, also checks inhereted classes
-  mixin is a tehnique in which we create an object with certain methods/props that we want to use accross multiple clasess and then use Object.assign(someClass, object) to add all props/methods to someClass
```js
Object.assign(SomeClass.prototype, mentionedObject)
```
- The Object.assign() static method copies all enumerable own properties from one or more source objects to a target object. It returns the modified target object.
- Example of all:
```js
class original {
    constructor(country) {
        this.surname = 'Petrovic'
        this.country = country
    }
    get getCountry() {
        return this.country;
    }
    set setCountry(value) {
        this.country = value;
    }
    stucanje() {
        console.log('stucanje1')
    }
}

class klasa extends original {
    #name
    constructor(country) {
        super(country)
        this.#name = 'test123';
        this.test = 123
    }
    get ['get'+'Name1']() {
        return this.#name;
    }
    set setName(value) {
        this.#name = value
        super.setCountry = 'Srbija'
    }
    stucanje() {
        console.log(this)
        super.stucanje()
    }
    static hellou(b) {
        console.log(this)
        console.log("hellou ", b.getName1)
    }
}
const b = new klasa('BIH');

```
## Javascript engine
* v8 for Chrome and Opera
* SpiderMonkey for Firefox
## hoisting
The JavaScript engine treats all variable declarations using “var” as if they are declared at the top of a functional scope (if declared inside a function) or global scope (if declared outside of a function) regardless of where the actual declaration occurs. This essentially is “hoisting”
A function declaration has "hoisting"
```js
a;
console.log(a)
// Uncaught ReferenceError: a is not defined

console.log(a)
var a;
// undefined

a = 1;
console.log(a)
var a;
// 1

console.log(a)
a = 1;
var a;
// undefined
```
Functions are hoisted before variables.
```js
foo();
var foo;
function foo() {
	console.log( 1 );
}
foo = function() {
	console.log( 2 );
};
// 1 will be logged
```
## closure
The binding which defines the scope of execution. Function declared in a function is a Closure. Inner function can access the parent function variables.
## compound operator
Compound Assignment examples: -=, *=, and += are compound operators that combine a math operation with assignment
## strict mode
You can opt in to strict mode for an individual function, or an entire file, depending on where you put the strict mode pragma.
```js
use strict
```
## var and let diff:
The scope of a variable defined with var is function scope or if declared outside any function, global. The scope of a variable defined with let is block scope. For example: var declared in a function is available above it's declaration but not out of a function. Let declared in a function is not available outside the function and before it's declaration. Const also has a block scope. Hoisting is only tied to var. Let cannot be redclared.
## refences and values
```js
var y = 234;
var z = y
y = 23;
console.log(z);  // Returns 234

var obj = { name: "Vivek", surname: "Bisht" };
var obj2 = obj;
obj1.name = "Akki";
console.log(obj2);
// Returns {name:"Akki", surname:"Bisht"
```
## Js advantages:
client side execution, testing js in console of browser, support major browsers, easy syntax. If we want to limit scope of var, we can use IIFE:
```js
(function() {var a})();
```
Since var is function scope, it will be available only within the function itself.
## Js page redirection 
```js
window.location(url)
```
## Functions
are first class objects (can be sent as parameters and can be returned from another function)
## Idemopotent
the side-effects of N > 0 identical requests is the same as for a single request

## js function:
Is an basic element in js. Is an object.
## js is not an object oriented language
Only inheritance that js supports is Prototypal inheritance. Js is interpreted language. Interpreted languages are not compiled and interpreter (browser) executes them directly.
## reserved words
cannot be used to declare a variable, but they can be used as a property of an object
## function
or { are always interpreted as statements, only if they are wrapped with (), they are interpreted as an expression statement (expression as a statement)
## after return statement
new line is forbiden in order to prevent accidentally return undesired value
## shadow
inner block x shadow outer x
```js
const x = 1;
assert.equal(x, 1);
{
  const x = 2;
  assert.equal(x, 2);
}
assert.equal(x, 1);
```
## global object
can be accessed:
```js
globalObject
```
## scope
The current context of execution.
## scopes:
* Global
* Function
* Block (let and const)
## Difference between == and ===
With == values are being compared with their values, but not types. With === values are being compared with values and types.
## Imutabillity
Immutable value, after it has been created, it can never change.
## Js cookie access
Document.cookie
## Native objects
are those objects supplied by JavaScript. Examples of these are String, Number, Array, Image, Date, Math, etc.
## Host objects
are objects that are supplied to JavaScript by the browser environment. Examples of these are window, document, forms, etc.
## Js var starts with
- $, _, and letters.
## Js modules
JavaScript code modules let multiple privileged JavaScript scopes share code. Example of the module is any code that we imported in out current code.
## This js
ES5 bind and ES6 call and apply methods are forwarding this, and by that change the context of function. In strict mode this inside the function will be undefined, in non-strict mode, this will be window or other global object. This in arrow functions represents a global object.
The value of “this” keyword will always depend on the object that is invoking the function. Arrow functions don't have this of their own. Apply, call and bind will not work.
The this keyword inside an arrow function, does not refer to the object calling it. It rather inherits its value from the parent scope which is the window object in this case
## Promise
The Promise object represents the eventual completion (or failure) of an asynchronous operation, and its resulting value. Promise.all([promise1, promise2, promise3]).then(function(values) {... is a method which is used to call multiple parallel promises. If any of the promises fail in its execution, promise all fails.
## async functions return AsyncFunction object.
These functions operate in a separate order then the rest of the code via the event loop, returning implicit Promise as its result. An async function can contain await expression that pauses the execution to wait for the passed promise resolution, then resumes execution.
```js
async function f() {
  const promise = new Promise((resolve, _reject) => {
    setTimeout(() => resolve("done!"), 1000)
  });
  const result = await promise; // wait until the promise resolves (*) and return result 'from' promise
  alert(result); // "done!"
}
f();
```
## await pauses the current async function and returns from it.
Once the awaited result is ready, the execution of the function continues where it left off.
## Many of the user interface mechanisms of browsers also run in the JavaScript process (as tasks). Therefore, long-running JavaScript code can block the user interface.
## Promise can be in 3 states:
pending, and one of two settled states: fulfilled and rejected.
## Promise resolve returns fullfilled or rejected status
## Promise reject, rejects it with given error
## then receives return value from promise on which mentioned then is called
## .catch .then can be chained in the order, once catch is executed, then will continue since catch returns a promise
## if promise returns a promise in return, next chained promise will receive .then result of that promise as input
## .then executes async calls sequentially
## Promises handle both asynchronous errors (via rejections) and synchronous errors
## util.promisify()
is a utility function that converts a callback-based function f into a Promise-based one
```js
import * as fs from 'fs';
import {promisify} from 'util';

const readFileAsync = promisify(fs.readFile); // (A)

readFileAsync('some-file.txt', {encoding: 'utf8'})
  .then(text => {
    assert.equal(text, 'The content of some-file.txt\n');
  })
  .catch(err => {
    assert.fail(err);
  });
```
* fetch:
```js
// fetch can be alternative for axios, but axios has some features implemented very simply
// if result code is 400 it will use then
fetch('http://example.com/textfile.txt')
  .then(response => response.text())
  .then(text => {
    assert.equal(text, 'Content of textfile.txt\n');
  });
```
## axios, graphql
use axios for rest, qraphql appollo for rest and graphql
## promise combinators:
  * race
  * all
  * allSettled
  * ...
## promise primitive:
  * resolve
  * reject
## promise.race
can be used to set a timeout for your promise. For example: the 'second' promise can be resolved after some period of time (timeout) using the setTimeout function. There for in promise.race, if the promise with timeout finish first, second one will not finish.

## Promise.race([...promises])
returns a promise which resolves as soon as any of the input promises resolves and rejects as soon as any of the promises rejects.

## Promise.any([...promises])
rejects a promise only if all promises are rejected, otherwise it resolves

## Promise.allSettled method
takes an array of promises and resolves once all of the promises have either resolved or rejected. Hence, promise returned by this method does not require catch callback as it will always resolve. The then callback receives the status and value of each promise in the order of their appearance.
```js
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
## good promise practise:
```js
// bad practise: this will return promise that is not yet finished
promise.then(r => r);
return promise;
// good practise:
return promise.then(r => r);

//bad practise:
.then(r => {
    return someFun()
    .then(r1 => r1);
});
.then(r => someFun())
.then(r1 => r1);
```
* async functions
```js
async function someFun() => {
try {
    const resp1 = await someReq(); // async
    const resp2 = await resp1.someReq1(); // async
    return resp2; // sync
  }
  catch(e) {
    return e;
  }
};
```
## Promise.any
method is similar to Promise.race but the promise returned by this method does not execute the catch block as soon as any of the promises gets rejected. Instead, it waits until any of the promises resolves. If none of the promises is resolved, catch block will get executed. If any of the promises have resolved first, then block will be executed.
## Javascript functional library: Ramda
* Javascript immutable library: immutable.js
## Javascript selectors: Reselect, specificly design library to work with redux
## Javascript expressions and statements
An expression produces a value, an example of statement is if statement. If statement is expected, expression could be passed, but not the other way around.
## Difference between y.x and y[x]
Second expression is evaluating x before accessing the property
## Elements in array
are stored as array properties, using numbers as property names, since .Number cannot be used, we use [number]. Array.length is the same as array[“length”]
## Methods:
Properties that contain functions are called methods
## Object.keys
property lists all properties of an object (if the properties (keys) are strings)
## ownKeys
if the properties are symbols, use Reflect.ownKeys
## Reflect
is similiar object as it is Math object that contains built in methods, similar to Object but with some specific differences (like ownKeys..)
## Object.assign
copies all properties from one object to another
## Arrays
are just a kind of objects specialized for storing sequences of things
## Difference between fun(a) and a.fun()
Second call has this keyword default and it uses this parameters
## functions
generally speaking, a function is a "subprogram" that can be called by code external (or internal in the case of recursion) to the function. Like the program itself, a function is composed of a sequence of statements called the function body. Values can be passed to a function, and the function will return a value. In JavaScript, functions are first-class objects, because they can have properties and methods just like any other object. What distinguishes them from other objects is that functions can be called. In brief, they are Function objects.
## Higher order functions
Functions that operate on other functions either by taking them as arguments or by returning them, are called higher-order functions.
## Apply, call , bind:
Use .bind() when you want that function to later be called with a certain context, useful in events. Use .call() or .apply() when you want to invoke the function immediately, and modify the context.
## Apply, call and bind
are not working with arrow function
## Call and Apply
cannot override bind
## When it comes to inheritance
JavaScript only has one construct: objects. Each object has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in this prototype chain.
* We can now use the new operator to create an instance of doSomething() based on this prototype.
* When a function is created in JavaScript, JavaScript engine adds a prototype property to the function. This prototype property is an object (called as prototype object) which has a constructor property by default. Constructor property points back to the function on which prototype object is a property. We can access the function’s prototype property using the syntax functionName.prototype.
## Event propagation
the way to describe order of events in web browser (two kinds: to child and to parent). Stop propagation: event.stopPropagation, event.preventDefault.
3 phases:
- Capturing phase – the event goes down to the element.
- Target phase – the event reached the target element.
- Bubbling phase – the event bubbles up from the element.
## A callback function
is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
## An event in JavaScript
is defined as “things that happen to HTML elements,” and there are a a lot of them. Change, click, mouseover, mouseout, keydown, load. If element doesn’t exist when page is loaded a eventListener problem occur. event.target is a reference to an object that dispatched the event. 
```js
//Event Delegation
function toggleDone (event) {
  if (!event.target.matches(‘input’)) return
  console.log(event.target)
  //We now have the correct input - we can manipulate the node here
}
```
## event delegation
adding event listener to parrent will propagate 
## adding event listener
to element will add event listener to all the children (event delagation) 
```js
someElement.addEventListener("mouseup", handleMouseUp); // third param - options
```
## process of delegation execution is event bubbling
## difference between target and currentTarget
target is the thing that is clicked, and currentTarget is where you attached eventListener (these two can be different because delegation for example)
## ES6 modules
Named exports, Default exports, Imports are hoisted
## ES6 new functionalities
* constants
* arrow functions
* parameter default values
* string interpolation
* property shorthand ({x, y} instead of {x:x, y:y})
* destructuring (var { op, lhs, rhs } = getASTNode()), class
## Browserify
lets you require('modules') in the browser by bundling up all of your dependencies
## A JavaScript compiler
takes JavaScript code, transforms it and returns JavaScript code in a different format. (example: babel)
## Bundlers
take JavaScript and CSS code written as separate modules (often hundreds of them), and combine them together into a few files better optimized for the browsers. (webpack)
## Webpack
is an open-source JavaScript module bundler. Its main purpose is to bundle JavaScript files for usage in a browser, yet it is also capable of transforming, bundling, or packaging just about any resource or asset. At its core, webpack is a static module bundler for modern JavaScript applications. When webpack processes your application, it internally builds a dependency graph from one or more entry points and then combines every module your project needs into one or more bundles, which are static assets to serve your content from.
## RequireJS is a JavaScript file and module loader
## The instanceof operator
tests whether the prototype property of a constructor appears anywhere in the prototype chain of an object
## Length of function
foo.length
## Function always return undefined if not specific return
## Functions compose from right to left (data flow)
## !!param will transform param in to Boolean value
## Side effect
is any unpredictable result (random function, changing variable out of function scope and of course asynchronous response. Program cannot be written without side effects.)
## Pure function
doesn’t have side effects. Pure function has referential transparency(if function is to be replaced with its return value, the program behavior would not change).
* For big calculations we can use cache inside of functions and in that way they are pure functions
* Value immutability
programs only use values that cannot be changed. (create new values for state of a program)
* Primitive values number, string, Boolean are already immutable (2 = 2.5 // invalid)
## Strings
in JS are not arrays. They are array-like objects. You can access element like it is an array, but you cannot change it.
## We use pure functions to achieve immutability
## If we declare array as a constant, we will be able to change it’s content. (const x = [2]; x[0] = 3; //ok)
## Object.freeze()
can be used to turn mutable object/array/function to immutable(top level only). 
## To achieve immutability
we don’t need to copy the entire structure every time, just the previous version.
```js
var x = Object.freeze( [ 2, 3, [4, 5] ] );

// not allowed:
x[0] = 42;

// oops, still allowed:
x[2][0] = 42;
```
## With closure and objects we can achieve the same thing
## Isomorphic
two things are similar in structure but not the same. Two things are isomorphic if you could map from a to b and go back with inverse mapping. Objects and Closures are isomorphic.
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
## tail optimization for recursion
```js
// standard recursion
const recursive = (n) => {
  if (n === 0) return "a dream";
  let dreams = recursive(n - 1);
  return dreams + " within a dream";
}
// tail recursive (should be less stack heavy)
const tailRecursive = (n) => {
  const helper = (n, dreams) => {
    if (n === 0) return dreams;
    return helper(n-1, dreams+" within a dream");
  }
  return helper(n);
}
```
## Binary recursion
the function calls itself twice within implmentation
## Memoization
a way for our function to remember (cache) the results
## Mutual recursion
functions calling each other
## Function js programing termin ‘Functor’
is a value that has a utility for using an operator function on that value (each value). (map)
## Filtering
can be inclusionary or exclusionary. (keeping or throwing out)
## Count how many times the function has been called
put inside a function console.count()
## Count how many times has function being called with specific argument console
countl(param)
## Console.table(array)
will have a nice print (this is. Working with object also) (to name each value you can pass array of two arrays in which first represents keys and the other one values)
## Use console.group() and console.groupEnd()
to organize logging if needed
## New keyword in js:
  * Creates new object (everything is object in js)
  * It sets prototype
  * It sets this
  * It executes constructor
  * It returns newly created object, or reference to object
## How to check if object contain property:
hasOwnProperty (will return true only if property exist in object itself, not the chain)
## Difference between argument and a parameter
(argument is a value passed to a function, parameter is a value that function expects upon execution)
## Function is called a method when is stored in object
## Functions that are not bound to an object are bound to global object
## Js constructor has to be capitalized
## Arguments array has only .length property
## Methods to prototypes can be added to use them in js in general on the project
## Strict mode
makes several changes to semantics:
  * Silent errors throw errors (changing object after freeze, this in functio is undefined instead of window)
  * Some optimizations so could run faster
  * Prohibits syntax for next releases
Chrome console is not in strict mode
```js
// strict mode inside chrome console
(function()
{
    'use strict';
    // write code
}());
```
## Object.freeze(obj).
First level of object property cannot be changed.
## Self invoking function
(function() {}()) IIF (imidiatelly invoked function)
## IIFE imediatelly invoked function expression
```js
function a() {}(); // not good
const foo = function(){}(); // good
(function () {})(); // good
```
## (+) operator
converts both values to primitive values (string or number, and does addition)
## Object.is(a, b)
is even more strict then ===
## >= and <= are strict
## < and >
will convert operands to number:
```js
true < 2 // true
true > 1 // false, true is converted to 1
```
## ?? operator is used
when only null or undefined needs to be checked: a ?? b (if a i null or undefined)
## The comma operator (,)
evaluates each of its operands (from left to right) and returns the value of the last operand. 
```js
x = (x++, x);
console.log(x);
// expected output: 2
x = (2, 3);
console.log(x);
// expected output: 3
```
It is commonly used in for loop
## of operator
can be used for "for" loop
```js
// standard
for(let i = 0;i<10;i++>) { }
// using operator "of"
for(let number of [1,2,3]) {}
// since string is iterable, we can do something like this
for(let char of "Dejan") {}
```
## how to make param mandatory
```js
mandatory = () => {
  throw new Error('Missing parameter!');
}

foo = (bar = mandatory()) => {}
```
## ~~ is the same as Math.floor()
```js
Math.floor(4.9) === 4  //true
~~4.9 === 4  //true
```
## ** is the same as Math.pow()
```js
Math.pow(2,3); // 8
2**3 // 8
```
## JSON doesn't support undefined, only null
## a in b, check if b.a
## js is single threaded
## event loop
  * setTimeout is provided by the browser, js is calling the function which invokes js function after given time (it pushes callback on taks queue, eventloop puts first thing on the stack from task queue if stack is empty)
  * setTimeout with zero time is used to delay callback until stack is cleared
  * ajax request lives in a browser as web api. When it completes, callback is pushed in to the queue, it is picked up by the event loop and when stack isempty callback will execute
  * to define async forEach (which is synchrounous) use setTimeout with delaytime 0 each time callback is called
  * Microtasks and Macrotasks: setTimeout, onClick are Macrotasks and all tasks are executed sequentally. Microtask queue is processed after Macrotasks.
  * mircotasks for asynchronous elements, macrotasks for synchrounous
  * Microtasks come solely from our code. (execution of Promises then, catch, finally)
  * event loop (microtasks and macrotasks)
    * Check if there is any task available in the macrotasks queue.
    * If so and this task is running, wait until it is completed before gointo the next step. If not, go directly to step 3.
    * Then run all the microtasks that are in the microtask queue.
    * If we add new microtasks during the execution of the microtasks, theare also executed.
  * event loop executions tasks
  * task sources add tasks
  * a task is finished when it reaches return keyword
  * rendering never happens while engine is executing a task
  * Immediately after every macrotask, the engine executes all tasks from microtask queue, prior to running any other macrotasks or rendering or anything else.
  ```js
  setTimeout(() => alert("timeout"));

Promise.resolve()
  .then(() => alert("promise"));

alert("code");
What’s going to be the order here?

code shows first, because it’s a regular synchronous call.
promise shows second, because .then passes through the microtask queue, and runs after the current code.
timeout shows last, because it’s a macrotask.
  ```
* event loop alg:
  * Dequeue and run the oldest task from the macrotask queue (e.g. “script”).
  * Execute all microtasks:
  * While the microtask queue is not empty:
  * Dequeue and run the oldest microtask.
  * Render changes if any.
  * If the macrotask queue is empty, wait till a macrotask appears.
  * Go to step 1.

## undeclared variable is different from undefined (browser gives an error)
## when use const, varible has to be initialized
## type of undeclared and undefined will return 'undefined'
## type of null is an object - bug in js
## use strict is mandatory when using es6
## use const in regex
```js
const regex = 'test';
var re = new RegExp(regex,"g");
someStr.match(re);
```
## All primitive values are immutable!
## you cannot change the chars in an array like this:
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
## Infinity and Nan are also numbers
## Number writting 
```js
1_000_000
// is equal to:
1000000
```
## two different codes:
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
## equality in js
```js
typeof NaN // 'number'
NaN === NaN // false - special case
0 === -0 // true - special case
-0 === 0 // true - special case
{} === {} // false
2 === 2 // true
```
## Further calculations with NaN will give you NaN again
## to check if it is NaN
```js
Number.isNaN(val)
Object.is(val, NaN)
val !== val // since the only value for which this is applicable is NaN
```
## if divided with zero
```js
5 / 0
// Infinitity
```
## number is Infinity
```js
Number.isFinite(x) === false;
```
## ceil, floor and round
```js
// ceil smallest
Math.floor(2.9); // 2
// floor largest
Math.ceil(2.9) // 3
// .5 rounded up
Math.round(2.5) // 3
```
## converting to string
```js
String(x); // recomended
'' + x;
x.toString(); // does not work for undefined and null
String(['a', ['b']]); // 'a,b' it will hide some details
```
## convert to number
```js
parseInt(string, base)
+x
-x
```
## check if Object
```js
(a !== null) && (a.constructor === Object)
```
## Stringifying functions, returns their source code
```js
const a = () => {};
String(a); // "() => {}"
```
## Symbols
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
## Symbols work with explicit conversion mostly
```js
Boolean(sym) // ok
!sym // ok
Number(sym) // ok
sym * 2 // Type error, similar is for String and toString
```
## throw exception
```js
// one by one throw exits the nested constructs until it encounters a try statement. Execution continues in the coresponding catch statement
```
## finally block executes before try statement ends
```js
() => {
    try {
      throw new Error();
    } finally {
      finallyWasExecuted = true;
    }
    // finally will be executed
```
## import * - import all
## dynamic import
```js
const loadSomeComponent = () => import('.../something');
loadSomeComponent();
```
## default export cannot export const since it can define multiple values:
```js
const a = 1, b = 2;
```
## 'default'
cannot be a variable name, but it can be a export or a property name
## reserved names
are allowed to use as property names
## when we use imports, we cannot change the variable exported, but connection is live, meaning that if there is a function that will change exported variable and is exported also, variable can be changed using mentioned function.
## import(x) returns a promise
## undefined and null can be spread inside an object
```js
{...undefined, ...null} // {}
// and also numbers
{...123} // also {}
```
## spread can be used
for shallow copying object. If any of the properties values is object, the value will not be shallow copied.
## spread can be used for default data:
```js
const providedData = { data1: 'c', data3: 'd' };
const allData = {data1: 'a', data2: 'b', ...providedData};
```
## we can use '?' to check if we can safely execution part of the code on the right side
```js
const a = { b: 1 };
a?.c?.d // no error, undefined
a?.b // 1
```
## '?' checks for null or undefined
## in operator to check if there is a prop inside an object
```js
const obj = { test: 1 };
'test' in obj // true
```
## delete obj.a will delete a property of object obj
## Object.fromEntries() is doing reverse Object.entries()
```js
// Object.fromEntries

var entries = [["x", 1],["y", 2],["z", 3]];
var obj = Object.fromEntries( entries );console.log( obj ); // {x: 1, y: 2, z: 3}
```
## freeze certain prop of an object
```js
const a = { x: 1 }

    Object.defineProperty(a, 'x', { writable: false });
    a.y = 2;
    Object.getOwnPropertyDescriptor(a, 'x');
    // {
    //   configurable: true,
    //   enumerable: true,
    //   value: "1",
    //   writable: true,
    // }

    Object.defineProperty(a, 'y', {
value:"",
});
// {
// configurable: false,
// enumerable: false,
// value: "",
// writable: false,
// }
```
## toString function is used
to determine how to convert to string, for numbers, valueOf function is used
## Object.freeze makes object immutable (not object in properties of an object)
## non inhereted properties are called own properties
## iterable has next, value and done attr.
When iteration is finished, done is true, add
## if you set element length to smaller number then current, you are removing elements
## string is itarable
```js
[...'abc'] === [ 'a', 'b', 'c' ] // numbers are not
```
## you can spread iterable to get an array
```js
const arr = [1,2,3];
// arr.keys() returns iterable
[...arr.keys()]; // [0,1,2]
```
## you can add additional member of an array like this:
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
## a way to check if something is an array:
```js
Array.isArray(something);
// or
something.constructor === Array
something instanceof Array
!!something.length
```
## array like objects
```js
{length: 2, 0: 'a', 1: 'b'};
```
## remove first elem of an array:
```js
const arr1 = ['a', 'b', 'c'];
const [, ...arr2] = arr1;
```
## flatMap
can be used for filtering and map at the same time
```js
<!-- Array.flat -->

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
```
## js Maps
allow use of functions, objects and other types as object keys. Object only allow strings and Symbols. Also Maps are iterable, objects are not
## structures that has limited number of memebers use length, others use size
## swap values:
```js
let x = 'a';
let y = 'b';
[x,y] = [y,x]; // swap
```
## generator function example:
```js
function* genFunc1() {
  yield 'a';
  yield 'b';
}
const iterable = genFunc1();
[...iterable] === ['a', 'b'];
```
## the way of using generator functions:
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
## JSON.parse(text, reviver?)
does not parse regex values. For this reviver param must be used
## Date js does not support time zones.
## code splitting
Lazy load just the things that are currently needed for app. import supports code splitting. With Code splitting, the bundle can be split to smaller chunks where the most important chunk can be loaded first and then every other secondary one lazily loaded.
## negative infinity
if we divide negative number with zero
## File read
* using a webpage and active x objects
* some js extensions
## get os
```js
window.navigator.platform
```
## pop-up boxes
* alert
* confirm
* prompt
## void operator
void operator evaluates expression and returns undefined
```js
void(2 == '2') // return undefined
```
## blur
removes focus from an element
## errors in js
* Build process errors
* run time errors
## encode and decode url
decodeURI() and encodeURI()
## MutationObserver
is a built-in object that observes a DOM element and fires a callback when it detects a change
## Range object
```js
let range = new Range();
setStart(node, offset)
setEnd(node, offset)
```
## Check if variable is declared
```js
typeof a !== "undefined"
```
## boxing wrappers:
str.length or str.toUpperCase() can be used because primitive types such as string or number get wrapped by boxing wrappers which allows use of methods (examples mentioned)
## web worker:
A separate instance of js engine allowing task parallelism. Workers share resources via postMessage API
## Thenable:
Any object (or function) with a then(..) function on it is assumed to be a thenable. Any place where the Promise mechanisms can accept and adopt the state of a genuine promise, they can also handle a thenable.
## function name:
```js
function def1() {
  let a = 5;
}
def1.name = 'def1'
var abc = function def() {
  let a = 5;
}
abc.name // def
var abc1 = function () {
  let a = 5;
}
abc1.name // abc1
```
## Lexical scope
When we access a variable from a child scope to the parent scope, this is known as being available in the “lexical” scope.














# REACT:
## React
is javascript library for building user interfaces.
## Jsx
is a syntax extension for javascript, written to be used with React. JSX is compiled to javascript.
## JSX is syntactic sugar for React.createElement()
## ReactDOM.render() renders JSX.
## JSX substitute for class is className.
This is because class is reserved name in js and JSX is interpreted to js
## Rendering of component is triggered:
- When parent component is rendered (React doesn't care about changing props, this is simply a consequence, unless you use useMemo and useCallback)
- When state of component changes
- When subscriptions are triggered (subscriptions on redux and React context)
## Never create a function that returns a component inside React component
Create it outside of component. Reconciliation will always create a new reference to this component and rerender all children if function is created inside
## Use key for component even if this is not a part of the list
If we use key like this, component will unMount and mount on any change, this can be useful
## You can use CONDITIONAL setState inside render method
## Events in react are written in camelCase.
Html events are written in lowercase.
## If statement is not possible in JSX expression
## React DOM 'escapes' any values in JSX to prevent cross-site-scripting attacks.
## Babel compiles jsx and es6
## React.createElement() creates an object:
```jsx
// simplified
const element = {
  type: 'h1',
  props: {
    className: 'greeting',
    children: 'Hello, world!'
  }
};
// for:
const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
);
```
## components are made of elements
## elements are immutable
## elements represents ui in a single point in time
## React element
A ReactElement is a light, stateless, immutable, virtual representation of a DOM Element. ReactElements lives in the virtual DOM.
## React components and props
Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.
## React components need to be specified with Capital letter in order for JSX to differentiate html and React Components
## Class names should be written capitalized
## All React components must be pure functions
## setState, the first level of 
## React data flow (unidirectional data flow) (top-down)
All data in our applications flow in a single direction. In React it flows down the tree from parent to child.
## React use syntetic events
that are similar to native events
## inside jsx we should use constant functions, not anonimous.
If this callback is passed through props, it can produce unecessary renders.
## id is not recomended for keys
for plural entities in React. It can mess up the performance, since React is using keys to identifies list members. If id's are changed during this time it can create confusion.
## rule of thumb: use keys inside map (individial member, doesn't need a key)
## passed key will not be available in props
## React component methods
shouldComponentUpdate(), render(),componentDidUpdate()
## This.props.children
returns single element if there is single element in between react component. For example (<RC>child</RC>) If there are multiple it will return array of elements
## you can pass Componenets as props unrelated to props.children
## This.setState
cannot be called inside render method because right after setState the render function is called. It would create infinite loop
## Decomposition, not inheretance!
## Virtual dom
The Virtual DOM is an abstraction of the HTML DOM.
## ReactDOM is a javascript library containing react specific methods.
All the methods deal with the DOM.
## Logic should be written in render method React.
## This in React refers to instance of the class.
Actually it refers to object on which this’s enclosing method (render() )
## React props is an object
## Default props React
even if they are not given as parameters they are defined by default with: SomeComponent.defaultProps = { someProp = “example” }
## we can control focus in React using ref
## React supports using ref as callback
```js
<div
  ref={(el) => {
    if (!el) return;
    console.log(el.getBoundingClientRect().width);
  }}
>
  Something
</div>
```
## React guarantees that refs are set before componentDidMount or componentDidUpdate hooks.
## React.lazy combined with Suspense component
can be used for lazy loading components. React.lazy currently only supports default exports. It seems that in the meantime React.lazy started to support dynamic imports. This is done through code spliting behind the hood.
```js
React.lazy(() => import('...'));
```
```jsx
<Suspense fallback={<Spinner>}>
  <ComponentX>
</Suspense>
```
## Component that is subscribed to context will read from closest Provider in ancestry
```js
const MyContext = React.createContext(defaultValue); // when provider cannot be found, use default value
<MyContext.Provider value={/* some value */}>
```
All consumers that are descendants of a Provider will re-render when Provider value prop changes.
```js
<MyContext.Consumer>
  {value => /* render something based on the context value */}
</MyContext.Consumer>
```
## Context can be updated from nested component.
Callback can be put in the context
## We could consume multiple contexts
component is wrapped with provider and all of this is wrapped in another provider:
```js
<FirstContext.Provider value={firstSomething}>
  <SecondContext.Provider value={secondSomething}>
    <SomeComponent />
  </SecondContext.Provider>
</FirstContext.Provider>
```
And inside component:
```js
<FirstContext.Consumer>
  {firstSomething => (
    <SecondContext.Consumer>
      {secondSomething => (
        <SomeOtherComponent firstSomething={firstSomething} secondSomething={secondSomething} />
      )}
    </SecondContext.Consumer>
  )}
</FirstContext.Consumer>
```
## Contexts compare context with using the Object.is
so if any prop is changed, components will be rerendered, so we need to think about value carefully, not to get unecessary re-renders
## ErrorBoundary component
can be use as a 'catch' for components. (only for class components). Errors that were not caught by any error boundary will result in unmounting of the whole React component tree
## React.forwardRef
can be used to use created ref (React.createRef) for more DOM manipulation
## Fragment doesn't add extra nodes to DOM
## Fragment doesn't support keys, but explicit React.Fragment does:
```js
<React.Fragment key={item.id}>
```
## key is the only attribute that can be passed to Fragment
## Higher order component
is a code pattern for React. It is a function that takes component and returns new component. This pattern is used for reusing logic. It is a pure function with no side effects
```js
const NewComponent = higherOrderFunction(OldComponent, (data) => doSomethingWithData(data));
// ...
const higherOrderFunction = (WrappedComponent, callback) => {
    return class extends React.Component {
        constructor(props) {
            super(props);
            // use callback function in any function
        }
        //...
    }
}
```
## Redux's 'connect' is a higher order component that returns higher order component
## Higher order component is parametrized container component.
## don't use higher order function inside render
on each render, new component will be created.
## React can be integrated with other libraries
## React must be in scope if using jsx
## JSX type can be a capitalized variable but not expression:
```jsx
return <components[props.storyType] someProp={props.someProp} /> // wrong
// right
const SpecificComponent = components[props.someType];
return <SpecificComponent someProp={props.someProp} />;
```
## Statements (if, for...) cannot be used in JSX, expressions can and should be used
## JSX between tags, can be string (whitespaces and blank lines will be removed). Expressions can be children
## Booleans, null and undefined are ignored in JSX (false and true)
## Virtualize long lists libraries:
react-window, react-virtualized
## if some rerendering (even if it is only a small part of dom), takes a lot of time, we can use shouldComponentUpdate lifecycle function shouldComponentUpdate and return true or false depending on what situation we know for sure that component should or shouldn't be updated.
## React portal
is a way to render children outside DOM hierarchy of parrent component. Typical use case is for dialogs.
## Profiler api
can be used to measure how often react app is rendered and the 'cost' of it. We can optimize parts that are 'slow'
## React alghorytm for comparing old and new elements is called reconciliation
If the root element has different types, it will remount everything, if not, only updates changed attributes
## when you add keys, react is doing compare using keys for order of elements. Without keys, if you change order, it will rerender everything, since it is in the new order. Do not use indexes as keys since indexes can change during time
## Arrays of IDs should be used to indicate ordering.
## ref in React. node can be reached with myRef.current
## ref updates happen before componentDidMount or componentDidUpdate lifecycle methods.
## 'render prop'
refers to a technique for sharing code between React components using a prop whose value is a render function. (React Router uses 'render prop' technique)
```js
// here:
render() {
  return (
    <SomeComponent render={data => (
      <OtherComponent {...this.props} data={date} />
    )}/>
  );
}
// and inside SomeComponent:
render() {
  return (
    <>
    {this.props.render(this.state)}
    </>
  );
}
```
## React.StrictMode
can show warnings and perform checks for its children
## React.Proptypes provides typecheck
## controlled components
data is handled by state. Uncontrolled components - data is handled by DOM
## React.isValidElement
returns true if it is a valid react element
## Custom hooks
should be used for reusing state logic between two different components. States are completelly different.
```js
const useWindowSize = () => {
  const [windowSize, setWindowSize] = useState({
    width: undefined,
    height: undefined,
  });
  
  useEffect(() => {
    function handleResize() {
      setWindowSize({
        width: window.innerWidth,
        height: window.innerHeight,
      });
    }
    window.addEventListener('resize', handleResize);
    handleResize();
    return () => window.removeEventListener('resize', handleResize);
  }, []);
  
  return windowSize;
}
// and then in component
const windowSize = useWindowSize()
// use it inside jsx if needed
```
## First DOM is update and then effects are run
## useEffect is asynchronous, most of the hooks are
## useEffect executes after the render
every effect will use state from that corresponding cycle
- use functions inside useEffect if possible
- if above is not possible, extract functions out of you component or wrap those with use callback (in this case, functions will need to be a part of dependency array of useEffect)
## a way to cancel request inside effect (avoid having race condition from previous request)
```js
function Article({ id }) {
  const [article, setArticle] = useState(null);
 
  useEffect(() => {
    let didCancel = false;
 
    async function fetchData() {
      const article = await API.fetchArticle(id);
      if (!didCancel) {
        setArticle(article);
      }
    }
 
    fetchData();
 
    return () => {
      didCancel = true;
    };
  }, [id]);
 
  // ...
}
```
## effect clean up happens after every render
## always use hooks at the top level
## useReducer lets us use reducer to handle local state of the component
```js
const [state, dispatch] = useReducer(stateReducer, []);
```
useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks
## setState (class components)
merge state objects. useState doesn't
## if initial state is expensive, useState can receive a function that will eventually initiate state.
```js
useState(getComplexComputation())  // wrong
useState(() => getComplexComputation()) // right
```
## useLayoutEffect
fires before render method, useEffect fires after render method (not recomended unless useEffect causes issues)
## useContext
```js
const something = useContext(MyContext);
```
## useMemo and useCallback help optimize with memoization
can be used with or without params for complex calculations
```js
const memoizedResult = useMemo(() => {
  return expensiveFunction(propA, propB);
}, [propA, propB]);
// components itself can be memoized
// const list = useMemo(() => <CountriesList countries={countries} />, [
//     countries
//   ]);
```
## React.memo
```js
export function Movie({ title, releaseDate }) {
  return (
    <div>
      <div>Movie title: {title}</div>
      <div>Release date: {releaseDate}</div>
    </div>
  );
}
export const MemoizedMovie = React.memo(Movie);
// First render - MemoizedMovie IS INVOKED.
<MemoizedMovie 
  title="Heat" 
  releaseDate="December 15, 1995" 
/>
// Second render - MemoizedMovie IS NOT INVOKED.
<MemoizedMovie
  title="Heat" 
  releaseDate="December 15, 1995" 
/>
```
## useDebugValue can be use when inspecting hooks for easier debugging
## it is recomended to separate state into multiple useState hooks for easier state update (setState doesn't merge objects by definition)
## we can useReducer and provide dispatch to child component instead of passing some callback
## mockComponent()
using with tests, self explanatory
## isElement()
returns true if it is React Element
## isElementOfType()
if it is React element with specific componentClass type
## ReactTestUtils.Simulate.click(node) - self explanatory
## Test Renderer - used without depending on dom (only plain js objects)
## React Testing Library - works with dom nodes, not with react components. RTL works WITH Jest (not mandatory).

## different state managers:
  * Redux
  * mobix
  * vuex (for Vue.js)
## namespace
group of desired functions, variables under a unique name. It is used for modularity
## use async callback inside useEffect
```js
useEffect(() => {
  (async () => {
    // body
  })();
}, [someEntity])
```
## react doesn't sanitize href
## The only difference between the fragment and <> is that <> doesn't support key
## key represent an element identity for React
We can use key to tell React that it should unmount component if needed. In the example bellow we are using a key as an element identity so it will be unmounted if x changes, potentially. Otherwize, component1 will not be unmounted, it will only change the prop from smth to dummy.
```jsx
{x === 'smth' ?
  <componentX key="first" smth={smth} />
  : <componentX key="second" dummy={dummy}>}
```
## React 19:
- useActionState
- useFormStatus
- useOptimistic
- use api
- ssr
- ref as a prop














# REDUX:
## Redux
is a pattern and library for managing and updating application state, using events called "actions"
## Redux
Redux is a predictable state container for JavaScript apps. Based upon flux (unidirectional data flow) and elm arhitecture(The core idea is that your code is built around a Model of your application state, a way to update your model, and a way to view your model).
* An action is a plain JavaScript object that has a type field. You can think of an action as an event that describes something that happened in the application.
```js
const addTodoAction = {
  type: 'todos/todoAdded',
  payload: 'Buy milk'
}
```
## An action creator
is a function that creates and returns an action object. We typically use these so we don't have to write the action object by hand every time
```js
const addTodo = text => {
  return {
    type: 'todos/todoAdded',
    payload: text
  }
}
```
## A reducer
is a pure function that receives the current state and an action object, decides how to update the state if necessary, and returns the new state
## The current Redux application state lives in an object called the store.
## Dispatch
The Redux store has a method called dispatch. The only way to update the state is to call store.dispatch() and pass in an action object. We typically call action creators to dispatch the right action.
```js
store.dispatch(addTodo('new todo'))
```
## Selectors
are functions that know how to extract specific pieces of information from a store state value
```js
const selectCounterValue = state => state.value
const currentValue = selectCounterValue(store.getState())
```
## A thunk
is a specific kind of Redux function that can contain asynchronous logic.
```js
export const incrementAsync = amount => (dispatch, getState) => {
  console.log('state ', getState());
  setTimeout(() => {
    dispatch(incrementByAmount(amount))
  }, 1000)
}
```
## Thunk can be used the same way action creator is used.
```js
store.dispatch(incrementAsync(5))
```
## Thunks can be used only if middleware is added to redux store
## Redux principals
  ### Single source of truth
  the state of your whole application is stored in an object tree within a single store.
  ### State
  is read-only
  ### Changes are made with pure functions
## You can normalize complex state in order to do 'nicer' calculations
## Redux normalize state principals:
  * Each type of data gets its own "table" in the state.
  * Each "data table" should store the individual items in an object, with the IDs of the items as keys and the items themselves as the values.
  * Any references to individual items should be done by storing the item's ID.
### State or Actions values must be serilizable
### Only one redux Store per app
### more then one child reducer can 'respond' to single action dispatched
## You can use store inside a function like this:
```js
import store from 'blaBla/store';
// store is just a:
// return createStore(blaBla...
// ...
  const {
    something,
  } = store.getState();
```
## add redux tools
``` js
const store = createStore(
    connectRouter(history)(App),
    compose(
        applyMiddleware(
            ...middleware
        ),
        window.__REDUX_DEVTOOLS_EXTENSION__ ? window.__REDUX_DEVTOOLS_EXTENSION__() : f => f
    )
);
```










# RxJs:
## RxJs library
which is used for handling asynchronous calls using observable squences.  
## Push and pull systems
In pull systems Consumer determines when it receives data from Producer (js functions). In push systems Producer determines when to send data to Consumer (js promises).
## Observable
is Producer of multiple values and it is pushing them into Observers (Consumers)
## Generator and Function difference
function returns singular value and generator returns none to infinite potentially.
## Functions, generators, observables
lazy, promises not (f,g,o will not execute unless called)
## Observables are synchronous
## Observable can return multiple values over time
functions can return one value, one time.
## Rxjs pipeable operator
(function) takes observables as an input and returns another observable (a pure operation) (subscribing to output observable will also subscribe to input observable











# JS FUNCTIONAL PATTERNS:
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
8.  Binary search recursive


let recursiveFunction = function (arr, x, start, end) {
 
    // Base Condition
    if (start > end) return false;
 
    // Find the middle index
    let mid = Math.floor((start + end) / 2);
 
    // Compare mid with given key x
    if (arr[mid] === x) return true;
 
    // If element at mid is greater than x,
    // search in the left half of mid
    if (arr[mid] > x)
        return recursiveFunction(arr, x, start, mid - 1);
    else
 
        // If element at mid is smaller than x,
        // search in the right half of mid
        return recursiveFunction(arr, x, mid + 1, end);
}
 
// Driver code
let arr = [1, 3, 5, 7, 8, 9];
let x = 5;
 
if (recursiveFunction(arr, x, 0, arr.length - 1)) {
    console.log("Element found!");
}
else { console.log("Element not found!"); }
 
x = 6;
 
if (recursiveFunction(arr, x, 0, arr.length - 1)) {
    console.log("Element found!");
}
else { console.log("Element not found!"); }

9. Bubble Sort

function bblSort(arr) {

    for (var i = 0; i < arr.length; i++) {

        // Last i elements are already in place  
        for (var j = 0; j < (arr.length - i - 1); j++) {

            // Checking if the item at present iteration 
            // is greater than the next iteration
            if (arr[j] > arr[j + 1]) {

                // If the condition is true
                // then swap them
                var temp = arr[j]
                arr[j] = arr[j + 1]
                arr[j + 1] = temp
            }
        }
    }

    // Print the sorted array
    console.log(arr);
}

// This is our unsorted array
var arr = [234, 43, 55, 63, 5, 6, 235, 547];

// Now pass this array to the bblSort() function
bblSort(arr);
```











# JS Chanlenges:
```js
// scroll to the top
const scrollToTop = () => window.scrollTo(0, 0);
// swapping 2 vars
[foo, bar] = [bar, foo];
```
```js
// create variable with name as a variable
const a = 'test';
this[a] = 1;
```
```js
  const debounce = (callback, timer, timeout) => (...args) => {
    clearTimeout(timeout);
    timeout = setTimeout(() => callback(args), timer);
  };
  // or
  // const debounce = (callback, delay) => args => {
  //   clearTimeout(debounce.timerId);
  //   debounce.timerId = setTimeout(() => callback(args), delay);
  // }

const process = debounce((someStr) => console.log(someStr), 5000);
process('test');
process('test');
process('test');
```
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

```js
const isMirror = (t1, t2) => {
  if (t1 === null && t2 === null) return true;
  if (t1 === null || t2 === null) return false;
  return (t1.val === t2.val)
      && isMirror(t1.right, t2.left)
      && isMirror(t1.left, t2.right);
};
const isSymmetric = root => isMirror(root, root);
// isMirror([1,2,2,3,4,4,3]) // true
// isMirror([1,2,2,null,3,null,3]) // false
```

```js
const maxDepth = root => {
    const check = (node, depth = 0) => {
        if (!node) return 0;
        if (node.val || node.val === 0) depth++;
        const leftChildDepth = node.left ? check(node.left, depth) : depth;
        const rightChildDepth = node.right ? check(node.right, depth) : depth;
        return  leftChildDepth > rightChildDepth ? leftChildDepth : rightChildDepth;
    };
    return check(root);
};
// maxDepth([3,9,20,null,null,15,7]) // 3
// maxDepth([1,null,2]) // 2
// maxDepth([]) // 0
```

```js
// helper
const maxDepth = root => {
    const check = (node, depth = 0) => {
        if (!node) return 0;
        if (node.val || node.val === 0) depth++;
        const leftChildDepth = node.left ? check(node.left, depth) : depth;
        const rightChildDepth = node.right ? check(node.right, depth) : depth;
        return  leftChildDepth > rightChildDepth ? leftChildDepth : rightChildDepth;
    };
    return check(root);
};

// a binary tree in which the left and right subtrees of every node differ in height by no more than 1
const isBalanced = function(root) {
    if (!root) {
        return true;
    }
   const leftMax = maxDepth(root.left);
   const rightMax = maxDepth(root.right);
   const diff = leftMax - rightMax;
    if (![-1,0,1].includes(diff)) return false;
    return isBalanced(root.left) && isBalanced(root.right);
};

// is there a path (root to leaf, leaf doesn't have children) which has desired sum.
const hasPathSum = (root, targetSum, currentSum = 0) => {
    if (!root) return false;
    const newCurrentSum = currentSum + root.val;
    const isLeaf = !root.left && !root.right;
    if (isLeaf && newCurrentSum === targetSum) return true;
    const leftBranch = !!root.left && hasPathSum(root.left, targetSum, newCurrentSum);
    const rightBranch = !!root.right && hasPathSum(root.right, targetSum, newCurrentSum);
    return leftBranch || rightBranch;
};


// given number of pascal triangle level determine array of arrays for this level

const generate = function(numRows) {

    if (numRows === 1) return [[1]];
    let pascalTriangle = [[1], [1,1]];

    if (numRows === 2) return pascalTriangle;

   const getRow = (iteration, position = 0, rowSoFar = []) => {
       switch(true) {
            case position === 0:
                return getRow(iteration, position + 1, [1]);
            case position === pascalTriangle.length:
                return [...rowSoFar, 1];
            default:
                return getRow(iteration, position + 1, [...rowSoFar, pascalTriangle[iteration -1][position - 1]+pascalTriangle[iteration -1][position]]);
       }
   };

   for(i = 2; i<numRows;i++) {
    pascalTriangle = [...pascalTriangle, getRow(i)];
   }
   return pascalTriangle

};


// with given ammount and given coins calculate coins for amount			     
			     
const convertIntoCoins = (amount, coins) => {
    const checkCoin = (newAmount, newCoins, coinsSoFar = []) => {
        if (newCoins.length === 0 && newAmount !== 0) return false;
        if (newCoins.length === 0 && newAmount === 0) return coinsSoFar;
        const [coin, ...rest] = newCoins;
        const coinNumber = Math.floor(newAmount/coin)
        const restAmmount = newAmount % coin;
        return checkCoin(restAmmount, rest, [...coinsSoFar, {[coin]: coinNumber}])
        
    }
    const helper = (newCoins = coins) => {
        const candidate = checkCoin(amount, newCoins);
        if (candidate) return candidate;
        const [_first, ...coinsRest] = newCoins;
        return helper(coinsRest);
    }
    return helper();
};

convertIntoCoins(46, [25, 10, 5, 2])
convertIntoCoins(46, [25, 10, 5, 2, 1])






// write a function that will return random value with each call with falsy param, and same value as previous with truthy param

const getParam = (
  (param = Math.random()) =>
    useOld =>
      useOld ?
        param
        :
        (param = Math.random()) && param
)()

getParam() // random value
getParam() // random value x
getParam(true) // value x
getParam(true) // value x
getParam() // random value
getParam() // random value y
getParam(true) // value y
getParam(true) // value y
// etc...
			     
			     
```
