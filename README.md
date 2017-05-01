# Front-end Job Interview Questions

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## Table of Contents

  1. [General Questions](#general-questions)
  1. [HTML Questions](#html-questions)
  1. [CSS Questions](#css-questions)
  1. [JS Questions](#js-questions)
  1. [Testing Questions](#testing-questions)
  1. [Performance Questions](#performance-questions)
  1. [Network Questions](#network-questions)
  1. [Coding Questions](#coding-questions)
  1. [Fun Questions](#fun-questions)

## Getting Involved

  1. [Contributors](#contributors)
  1. [How to Contribute](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/CONTRIBUTING.md)
  1. [License](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/LICENSE.md)

#### General Questions:

* What did you learn yesterday/this week?
* What excites or interests you about coding?
* What is a recent technical challenge you experienced and how did you solve it?
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* Talk about your preferred development environment.
* Which version control systems are you familiar with?
* Can you describe your workflow when you create a web page?
* If you have 5 different stylesheets, how would you best integrate them into the site?
* Can you describe the difference between progressive enhancement and graceful degradation?
* How would you optimize a website's assets/resources?
* How many resources will a browser download from a given domain at a time?
  * What are the exceptions?
* Name 3 ways to decrease page load (perceived or actual load time).
* If you jumped on a project and they used tabs and you used spaces, what would you do?
* Describe how you would create a simple slideshow page.
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* What does CORS stand for and what issue does it address?

#### HTML Questions:

* What does a `doctype` do?

`<!DOCTYPE>` tells the browser which version of HTML (or XML) is being used to write this webpage.

* What's the difference between full standards mode, almost standards mode and quirks mode?

In full standards mode, the behavior strictly follows HTML and CSS specification. In almost standards mode, there are a few number of quirks implemented. In quirks mode, non-standard behaviors are used for the sake of backward compatibility with websites (designed for Navigator 4 and IE 5) that were built before the widespread adoption of web standards.

* What's the difference between HTML and XHTML?

HTML can travel over the network to a browser either in HTML syntax or an XML syntax called XHTML. The MIME type for HTML is `text/html`, whereas for XHTML is `application/xhtml+xml`.

* Are there any problems with serving pages as `application/xhtml+xml`?

Internet Explorer 8 and older browsers will show a download dialog box for unknown file types when they see an XHTML document with the correct XHTML MIME type. Many popular JavaScript libraries and developer tools have limited or no support for XHTML.

* How do you serve a page with content in multiple languages?
* What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
* What is progressive rendering?
* Have you used different HTML templating languages before?

#### CSS Questions:

* What is the difference between classes and IDs in CSS?

Classes can be applied to multiple DOM elements on the webpage, whereas there could be only one element with a specific ID.

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

http://stackoverflow.com/questions/6887336/what-is-the-difference-between-normalize-css-and-reset-css

* Describe Floats and how they work.

It is a CSS property that specifies an element should be placed along the left or right side of its container, where text and inline elements will wrap around it. A floated element is taken out of the normal flow of the document. It is shifted to the left or right until it touches the edge of its containing box or another floated element.

* Describe z-index and how stacking context is formed.

The z-index property specifies the z-order of a positioned element and its descendants. When elements overlap, z-order determines which one covers the other. An element with a larger z-index generally covers an element with a lower one.

Stacking context is the three-dimentional conceptualization of HTML elements along an imaginary z-axis relative to the user who is assumed to be facing the viewport or the webpage. Positioning and assigning a z-index value to an HTML element creates a stacking context, (as does assining non-full opacity). Stacking contexts can be contained in other stacking contexts, and together create a hierarchy of stacking contexts. Eaching stacking context is self-contained: after the element's
contents are stacked, the whole element is considered in the stacking order of the parent stacking context.

* Describe BFC(Block Formatting Context) and how it works.

A block formatting context is a part of a visual CSS rendering of a web page. it is the region in which the layout of block boxes occurs and in which floats interact with each other. A block formatting context is a box that satisfies at least one of the following:

- the value of `float` is not `none`.
- the used value of `overflow` is not `visible`.
- the value of `display` is `table-cell`, `table-caption`, or `inline-block`.
- the value of `position` is neither `static` nor `relative`.

* What are the various clearing techniques and which is appropriate for what context?
* Explain CSS sprites, and how you would implement them on a page or site.
* What are your favourite image replacement techniques and which do you use when?
* How would you approach fixing browser-specific styling issues?
* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
* What are the different ways to visually hide content (and make it available only for screen readers)?
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Are you familiar with styling SVG?
* How do you optimize your webpages for print?
* What are some of the "gotchas" for writing efficient CSS?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Describe pseudo-elements and discuss what they are used for.

Pseudo-elements are added to selectors to style certain parts of a element. For example, ::first-line targets only the first line of an element specified by the selector.

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?

The `width` and `height` properties of an element include content, padding and border, but not margin. Advantage?

* List as many values for the display property that you can remember.

```css
display: none;

display: inline;
display: block;
display: inline-block;
display: contents;
display: list-item;
display: inline-list-item;
display: table;
display: inline-table;
display: table-cell;
display: table-column;
display: table-column-group;
display: table-footer-group;
display: table-header-group;
display: table-row;
display: table-row-group;
display: table-caption;
display: flex;
display: inline-flex;
display: grid;
display: inline-grid;
display: subgrid;
display: ruby;
display: ruby-base;
display: ruby-text;
display: ruby-base-container;
display: ruby-text-container;
display: run-in;

/* Global values */
display: inherit;
display: initial;
display: unset;
```

* What's the difference between inline and inline-block?

Inline elements:

- respect left & right margins and padding, but not top & bottom
- cannot have a width and height set
- allow other elements to sit to their left and right.

Inline-block elements:

- allow other elements to sit to their left and right
- respect top & bottom margins and padding
- respect height and width

Block elements:

- respect all of those
- force a line break after the block element

http://stackoverflow.com/questions/9189810/css-display-inline-vs-inline-block

* What's the difference between a relative, fixed, absolute and statically positioned element?

static: This keyword lets the element use the normal behavior, that is it is laid out in its current position in the flow.  The top, right, bottom, left and z-index properties do not apply.

relative: This keyword lays out all elements as though the element were not positioned, and then adjust the element's position, without changing layout (and thus leaving a gap for the element where it would have been had it not been positioned). The effect of position:relative on table-*-group, table-row, table-column, table-cell, and table-caption elements is undefined.

absolute: Do not leave space for the element. Instead, position it at a specified position relative to its closest positioned ancestor if any, or otherwise relative to the initial containing block. Absolutely positioned boxes can have margins, and they do not collapse with any other margins.

fixed: Do not leave space for the element. Instead, position it at a specified position relative to the screen's viewport and don't move it when scrolled. When printing, position it at that fixed position on every page. This value always create a new stacking context. When an ancestor has the transform property set to something different than none then this ancestor is used as container instead of the viewport (see CSS Transforms Spec).

* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* How is responsive design different from adaptive design?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?

#### JS Questions:

* Explain event delegation

Event delegation allows us to bind an event handler to a single parent element, and that handler will get executed whenever the event occurs on any of its child nodes. This is achieved by event bubbling (aka event propagation). The benefit is that with event delegation, the number of event bindings can be drastically decreased by moving them to a common parent element, as a result, the total memory used by event listeners goes down.

http://stackoverflow.com/questions/1687296/what-is-dom-event-delegation

* Explain how `this` works in JavaScript

The value of `this` is determined by how a function is called.

In the global context, `this` refers to the global object, whether is strict mode or not.

In the function context:

- non-strict mode: `this` refers to global object.
- strict mode: if `this` was not defined by the execution context, it remains undefined.

Use `call` or `apply` to pass the value of `this` from one context to another. Or use `bind` so a new function with binded `this` can be called later.

In arrow functions, `this` is set lexically, i.e., it's set to the value of the enclosing execution context's `this`.

As an object method, `this` is set to the object the method is called on.

As a constructor, `this` is set to the new object being constructed.

As a DOM event hanlder, `this` is set to the element the event fired from.

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this

* Explain how prototypal inheritance works

Every JavaScript object has a link to a prototype object. When trying to access a property of an object, the property will not only be sought on the prototype of the object, the prototype of the prototype, and so on until either a property with a matching name is found or the end of the prototype chain if reached.

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain

* What do you think of AMD vs CommonJS?
* Explain why the following doesn't work as an IIFE: `function foo(){ }();`.
  * What needs to be changed to properly make it an IIFE?

This is not an immediately invoked function. To make it an IIFE, wrap the function with `()` so it looks like: `(function foo(){})()`. Alternatively, `+function foo(){}()` will also work.

* What's the difference between a variable that is: `null`, `undefined` or undeclared?
  * How would you go about checking for any of these states?

A variable is undeclared when it does not use the `var` keyword. It gets created on the global object, thus it operates in a different space as the declared variables. It will not work in strict mode.

A variable is `undefined` if it hasn't been defined yet.

`null` is a variable that is defined to have a null value, which is an object.

* What is a closure, and how/why would you use one?

A closure is a function that remembers the environment in which they were created. The environment consists of any local variables that were in-scope at the time that the closure was created. A closure lets you associate some data (the environment) with a function that operates on that data. 

Use cases:
- Use a closure anywhere that you might normally use an object with only a single method.
- Emulate private methods using closures, which is also known as the module pattern.

* What's a typical use case for anonymous functions?

- The function is only ever called in one place.
- Inline functions that can access variables in the parent scopes.
- Closure.

* How do you organize your code? (module pattern, classical inheritance?)
* What's the difference between host objects and native objects?

Host object: supplied by the host environment to complete the execution environment of ECMAScript. For example for browser environment, `window`, `document`, `location`.
Native object: object in an ECMAScript implementation whose semantics are fully defined by this specification rather than by the host environment. For example, `Object`, `Date`, `indexOf`, `replace`...

* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* What's the difference between `.call` and `.apply`?

They both call a function with a given `this` value and arguments. `.call` takes a list of arguments whereas `.apply` takes an array of arguments.

* Explain `Function.prototype.bind`.

Creates a new function that, when called, set its `this` keyword set to the provided value.

* When would you use `document.write()`?

To include third party code. Since `document.write()` is always available, it is a good choice for third party vendors to use it to add their scripts.

* What's the difference between feature detection, feature inference, and using the UA string?
* Explain Ajax in as much detail as possible.
* What are the advantages and disadvantages of using Ajax?
* Explain how JSONP works (and how it's not really Ajax).
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".

Because variable declarations are processed before any code is executed, declaring a variable anywhere in the code is equivalent to declaring it at the top. This also means that a variable can appear to be used before it's declared.

* Describe event bubbling.
* What's the difference between an "attribute" and a "property"?

Attribute is in the HTML itself (of type string), whereas property belongs to DOM objects, which can be different types.

* Why is extending built-in JavaScript objects not a good idea?
* Difference between document load event and document DOMContentLoaded event?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]

function duplicate(arr) {
    return arr.concat(arr)
}
```
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What is `"use strict";`? what are the advantages and disadvantages to using it?

It is a way to opt in to a restricted variant of JavaScript.

- Eliminates some JavaScript silent errors by changing them to throw errors. 
- Fixes mistakes that make it difficult for JavaScript engines to perform optimizations: strict mode can sometimes be made to run faster than identical code that's not strict mode.
- Prohibits some syntax likely to be defined in future versions of ECMAScript.

* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`

```
for (var i = 0; i <= 100; i++) {
    var multiplesOfThree = i % 3
    var multiplesOfFive = i % 5

    if (multiplesOfThree) console.log("fizz")
    if (multiplesOfFive) console.log("buzz")
    if (multiplesOfThree & multiplesOfFive) console.log("fizzbuzz")
}
```

* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?

It is used to detect a fully-loaded page, which means it has to wait for all stylesheets, images, and subframes to finish loading. We can use `DOMContentLoaded` to detect that the DOM has been completely loaded without having to wait for stylesheets, images, and subframes to finish loading.

* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* What language constructions do you use for iterating over object properties and array items?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
    String and Number object.
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`

#### Testing Questions:

* What are some advantages/disadvantages to testing your code?
* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?

#### Performance Questions:

* What tools would you use to find a performance bug in your code?
* What are some ways you may improve your website's scrolling performance?
* Explain the difference between layout, painting and compositing.

#### Network Questions:

* Traditionally, why has it been better to serve site assets from multiple domains?
* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
* What are the differences between Long-Polling, Websockets and Server-Sent Events?
* Explain the following request and response headers:
  * Diff. between Expires, Date, Age and If-Modified-...
  * Do Not Track
  * Cache-Control
  * Transfer-Encoding
  * ETag
  * X-Frame-Options
* What are HTTP methods? List all HTTP methods that you know, and explain them.

#### Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
```

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

#### Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Who inspires you in the front-end community?
* Do you have any pet projects? What kind?
* What's your favorite feature of Internet Explorer?
* How do you like your coffee?


#### Contributors:

This document started in 2009 as a collaboration of [@paul_irish](https://twitter.com/paul_irish) [@bentruyman](https://twitter.com/bentruyman) [@cowboy](https://twitter.com/cowboy) [@ajpiano](https://twitter.com/ajpiano)  [@SlexAxton](https://twitter.com/slexaxton) [@boazsender](https://twitter.com/boazsender) [@miketaylr](https://twitter.com/miketaylr) [@vladikoff](https://twitter.com/vladikoff) [@gf3](https://twitter.com/gf3) [@jon_neal](https://twitter.com/jon_neal) [@sambreed](https://twitter.com/sambreed) and [@iansym](https://twitter.com/iansym).

It has since received contributions from over [100 developers](https://github.com/h5bp/Front-end-Developer-Interview-Questions/graphs/contributors).
