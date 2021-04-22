# JavaScript Interview Questions

> For the most part, these are not very interesting questions.  Unless you are being interviewed for a job that requires you to maintain a large amount of pre-existing JavaScript code, it's hard to see why an interviewer would ask questions like these.  They would learn more if they asked you to write, or simply describe how you would go about writing, code to solve a simple problem.
>
> Because good answers to many of these questions are on the website for [W3Schools](https://www.w3schools.com/js/default.asp), I do try to answer many of them here.

Explain event delegation.

Explain how `this` works in JavaScript.

Explain how prototypal inheritance works.

What do you think of AMD vs CommonJS?

> I don't know what these are.

Explain why the following doesn't work as an IIFE: `function foo(){ }();`. What needs to be changed to properly make it an IIFE?  &#128078;&#127998;

> I wouldn't use notation that was this obscure.

What's the difference between a variable that is: null, undefined or undeclared? How would you go about checking for any of these states?

> A variable is undeclared if it has not been created by execution of a `var`, `let`, or `const` statement.  It is undefined if it has been declared, but not yet assigned a value.  It is null if it has been assigned the value null.
>
> Use `!x`, `x == null`, and `x === null`.

What is a closure, and how/why would you use one?

> A closure is like a lambda function.

Can you describe the main difference between a `.forEach` loop and a `.map()` loop and why you would pick one versus the other?

> I have never used `.map()`.

What's a typical use case for anonymous functions?

> To attach a function to an event handler.

How do you organize your code? (module pattern, classical inheritance?)

> I try to organize my code using the model-view-controller design pattern.  For complicated programs, I prefer to use TypeScript, which lets me define and use classes with strict type checking.  I almost never use more than one level of inheritance.
>
> &#128077;&#127998;&#128078;&#127998;  The first part of this question is good, the parenthesized part is not.  My answer addresses the first part and pretty much ignores the second, which invites a boring answer about JavaScript technicalities rather than an interesting answer about how I approach problems.  It shows familiarity with a buzzword (inheritance) in the question, but avoids going into the difference between classical inheritance (as used in TypeScript) and prototypical inheritance (as used in JavaScript).  Likewise, it avoids going into a discussion of modules in JavaScript, which are simply ways to manage namespaces (so that different programmers can use the same identifiers for different purposes in different modules).
>
> Different answers to the question might talk about how and why you divide your code into separate files (and organize those files in separate directories) or about how and why you use classes.

What's the difference between host objects and native objects?

> JavaScript provides native objects such as Number, String, Array, and Function.
>
> The DOM model provides host objects such as window.  Various APIs provide additional host objects, such as the office object in the Microsoft Office JavaScript API.

Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?

> `function Person(){...}` is a function declaration.
> `var person = Person()` invokes that function to obtain a value.
> `var person = new Person()` is used to create a new instance of the `Person` class using the constructor for that class.

What's the difference between `.call` and `.apply`?

Explain `Function.prototype.bind`.

When would you use `document.write()`?

What's the difference between feature detection, feature inference, and using the UA string?

Explain Ajax in as much detail as possible.

What are the advantages and disadvantages of using Ajax?

Explain how JSONP works (and how it's not really Ajax).

Have you ever used JavaScript templating? If so, what libraries have you used?

> I've used templating in Angular.

Explain "hoisting".

Describe event bubbling.

> Events triggered on a DOM element bubble up to (i.e., are handled by) the nearest ancestor with an attached event listener.

What's the difference between an "attribute" and a "property"?

Why is extending built-in JavaScript objects not a good idea?

> This can create severe interoperability problems for programs that use multiple libraries.

Difference between document load event and document DOMContentLoaded event?

> I'm more familiar with the Angular life-cycle events.

What is the difference between == and ===?

> == does type conversions, === does not.  It's safer to use === to avoid things like `2 == '2'` being true.

Explain the same-origin policy with regards to JavaScript.

Make this work: `duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]`

> `function duplicate(a) { return a.concat(a); }`

Why is it called a Ternary expression, what does the word "Ternary" indicate?

> A ternary expression has three components, as in `x < 0 ? x + 1 : x - 1`.  Ternary means three, just as binary means two and unary means one.

What is `use strict;`? what are the advantages and disadvantages to using it?

Create a for loop that iterates up to 100 while outputting "fizz" at multiples of 3, "buzz" at multiples of 5 and "fizzbuzz" at multiples of 3 and 5.

````javascript
for (let i = 1; i <= 100; i++) {
console.log(i % 15 == 0 ? 'fizzbuzz' : 
            i % 5 == 0 ? 'buzz' :
            i % 3 == 0 ? 'fizz' : '');
}
````

Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?

> I understand that global variables in general are not a good idea: they make information available (to be read and tampered with) where it is not needed, and global variables defined in one module can conflict with those defined in another.  However, I find myself using them to make the model in a model-view-controller design pattern available to event handlers.

Why would you use something like the load event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?

> I use it if I want to draw graphics on a canvas when displaying a page.

Explain what a single page app is and how to make one SEO-friendly.

What is the extent of your experience with Promises and/or their polyfills?

What are the pros and cons of using Promises instead of callbacks?

What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?

> TypeScript provides strong type checking, which I find essential for catching syntactic errors in large programs.  Type annotations also make programs easier to understand.  TypeScript also provides features like enums that lead to more readable code.
>
> TypeScript introduces another level of complexity because it must be transpiled into JavaScript.  Debugging with TypeScript also depends upon the transpiler producing a source map that relates transpiled code to source code.

What tools and techniques do you use debugging JavaScript code?

> I use eslint for static checking, the debuggers provided by Chrome and Firefox, and console.log statements.  I also embed sanity checks in my code (for example, to ensure that arguments supplied to functions are not null).

What language constructions do you use for iterating over object properties and array items?

> Ordinary for loops:  `for (let i = 0; i < n; i++) { ...i... }`
> Loops over objects in a collection:  `for (let x of a) { ...x... }`
> Loops over indices in a collection: `for (let i in a) { ...a[i]... }`
> `arr.forEach`

Explain the difference between mutable and immutable objects.  &#128077;&#127998;

> Assignment statements in imperative languages, such as `a[5] = 3` and `a.push(3)`, can change the state of mutable objects like arrays.
>
> They cannot change the state of immutable objects such as numbers and strings.
>
> Functional programming avoids side effects by making all objects immutable.  However, compilers for functional programming languages must implement optimizations to avoid the cost, for example, of an entire array when all that is needed is a change in one element of the array.

Explain the difference between synchronous and asynchronous functions.  &#128077;&#127998;

> Synchronous functions run to completion before relinquishing control.  They block different program elements from operating in parallel.
>
> An asynchronous function does not block execution of the statement following its call.  Instead, it generates an event or issues a call-back when it finishes its computation.

What is event loop? What is the difference between call stack and task queue?

Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`.

> `function foo() {...}` declares a function.
>
> `var bar = function() {}` assigns an anonymous function as the value of a variable, just as `var bar = foo` would have assigned the named function foo as the value of a variable.

What are the differences between variables created using `let`, `var` or `const`?

> `let x = ...` declares `x` to be a variable accessible within a block of code enclosed in braces {}
>
> `var x = ...` declares `x` to be a variable accessible within a function definition or within the global scope
>
> `const x = ...` declares a variable whose value cannot be changed by an assignment statement

What are the differences between ES6 class and ES5 function constructors?

> Why is it important to know this?

Can you offer a use case for the new arrow => function syntax? How does `this` new syntax differ from other functions?

> I use it in when attaching event listeners, as in
> `document.getElementById('foo').addEventListener(event => myHandler());`
> This syntax makes the keyword `this` within the definition of myHandler refer to the global state of my JavaScript code, not to the state of the document.

What advantage is there for using the arrow syntax for a method in a constructor?

What is the definition of a higher-order function?

> A higher-order function is one that takes another function as an argument.  A generalized sorting function, `mySort(arr, lessThan)`, might have two parameters, an array of objects and a function `lessThan(obj1, obj2)` for comparing objects in the array.

Can you give an example for destructuring an object or an array?

ES6 Template Literals offer a lot of flexibility in generating strings, can you give an example?

> ES6 template literals provide functionality like the sprintf function in C.  You can write

````javascript
s = 'The sum of ' + x + ' and ' + y + ' is ' + z + '.');
````

> more simply as `s = 'The sum of $[x} and ${y} is ${z}.';`

Can you give an example of a curry function and why this syntax offers an advantage?

What are the benefits of using spread syntax and how is it different from rest syntax?

How can you share code between files?

Why you might want to create static class members?  &#128077;&#127998;

> Static properties can be used to define constants whose values of the same for all instances of the class.  A static property can also be used to create a singleton class.
>
> Static methods can be used as factory methods to create instances of a class.

## JavaScript General

Can you name two programming paradigms important for JavaScript app developers?

> Imperative and functional programming.

What is functional programming?  &#128077;&#127998;

> Functional programming differs from imperative programming in that it describes what a program does, not how it does it. Looping behavior is achieved by recursive function calls.

What is the difference between classical inheritance and prototypal inheritance?

> With classical inheritance, classes inherit properties and methods from superclasses.  With prototypical inheritance, objects inherit properties and methods from other objects.  I much prefer classical inheritance.

What are the pros and cons of functional programming vs object-oriented programming?  &#128077;&#127998;

> In functional programming, function evaluation has no side effects.  However, functional programs can be harder to understand than object-oriented programs, which associate actions directly with the objects they affect.

What are two-way data binding and one-way data flow, and how are they different?

> This question, which concerns how data flows between JavaScript and a web page, seems to be more about frameworks like Angular and React than it is about JavaScript, which can push information to and pull it from the innerHTML of elements on a page.  In Angular, constructs like `{{name}}` or `{{total()}}` allow data to flow from JavaScript into an element, whereas constructs like `@Input` and `@Output` allow for data to flow in both directions.

What is asynchronous programming, and why is it important in JavaScript?  &#128077;&#127998;

> Synchronous programs that run largely without interruption (except for I/O) are insufficient for handling user interactions with web pages.  Asynchronous programs use event queues to schedule tasks that should not be made to wait until other tasks run to completion.
