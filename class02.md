[Table of Contents](https://joepennock-401-advanced-javascript.github.io/401-reading-notes/)

# Classes, Inheritance, Functional Programming

## Research Questions:

1. Name 3 advantages to Test Driven Development:

    Test driven development, or TDD for short, is the practice of writting tests for a piece of functional code. This gives the developer a metric against which to develop their functionality. It set's a minimum requirement so that when they manage to pass the test, the code is doing everything initially required. Once the code is written and the test passed, you can then refactor the code as needed to make it wasier to read, reproduce etc.

    1. One of the benefits of TDD is that it produces fewer bugs in production. While the additional tests might result in longer test run times, down the line there will be fewer bugs that require time to fix, ultimately resulting in a faster, more stable production release.

    2. Another benefit of TDD is being built in acceptance criteria. When developing new code, there is typically some minimum requirements or features that are required. Using this criteria as the base for your tests, you will be able to easily know when your MVP (minimum viable product) has been met by simply passing your tests.

    3. A third benefit of TDD is using the tests written as living documentation. Since tests are written for specific scenarios, you can often look at the expected results of a test to help understand how a particular piece of code works. This can help give you a better understanding of the development process behind the code.

2. In what case would you need to use beforeEach() or afterEach() in a test suite?

    The `beforeEach` and `afteEach` commands are used to set up and tear down tasks at the beginning and end of test blocks. They can both handle asynchronous code just as the tests themselves can. The reason we would want to use `beforeEach` and `afterEach` would be to help keep your code clean and prevent duplicate code. If the tests are required to interact with a specific piece of code in order to run, using these commands will save time and make things easier to read and require less resources for the test suite to run.

3. What is one downside of Test Driven Development?

    While TDD has many reasons why it should be used, it is not without fault. One downside to TDD is time. When you are using TDD, the end product will take longer to finish since there are extra steps involved to write and pass tests before any actual production. If time is of the essence, TDD might not be the right choice. If, for example, you have a small start up that simply needs to show proof of life, adding a bunch of tests to the development process would nit be beneficial. Once you have MVP up and running, that would be a good time to begin implementation of TDD practices.

4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?

    The primary difference between ES6 Classes and more vanilla Constructor/Prototype Classes would be readability. While you can get virtually the same end result using either method, the newer ES6 Classes are much easier to read and understand with just a quick glance. In addition, they are easier to write as the syntax is much more straight forward.

5. Name a use case for a static method:

    As with Classes, static methods are a new addition to ES6. Static methods are designed to be used inside of a Class, and unlike the older prototype methods, the are not called on the instance of the Class but on the Class itself. Often times they are used for utility purposes. So why would you want to use static methods if they're not called on the instance created from the Class? One good reason would be inheritance. If you have a parent Class that itslef has subclasses inside of it, and static method called in the parent Class is also available to the subclasses. Utilizing the `this` keyword, you can use a static method from another static method within the same class as `this`.

6. Write an example of a Higher Order function and describe the use case it solves:

    Higher Order Functions are functions that operate on other functions. JavaScript has a lot of these as built in methods for various data types. Here's a simple example of a Higher Order Function:

    ```
    let array = [1, 2, 3];

    let sum = array.reduce(function(a,b) {return a + b; }, 0);
    ```
    With the above snippet, `sum` will now have the value of the sum of the array. Reduce is a built in JavaScript array method that itself uses another callback function. 

## Vocabulary:

* **functional programming** - A programming methodology where programs are developed by writting and using functions. [source](https://en.wikipedia.org/wiki/Functional_programming)
* **pure function** - A pure function is a function that, given the same input, will always return the same output. [source](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976)
* **higher-order function** - A function that operates on another function. 
* **immutable state** - A state, which can refer to objects, arrays etc., that can not be modified after it is created.
* **object** - A data type in JavaScript that is used to easily store data in key:value pairs.
* **object-oriented programming (OOP)** - 
* **class** - An ES6 replacement to the Constructor function, Classes effectively do the same thing as Constructor functions in a more readable, easier to write way. 
* **prototype** - A method, that is not stand alone, built on to the parent Constructor or function.
* **super** - A keyword in JavaScript that is used to access and call functions on an object's parent. [source](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super)
* **inheritance** - The process where a 'child' or subclass or function inherits, or gains, properties or methods from the parent class or functions.
* **constructor** - A function that is used as a blueprint from which `new` instances can be created.
* **instance** - An single occourance of something, such as a Constructor function or Class.
* **context** - The value of the `this` keyword.
* **this** - A keyword in JavaScript that refers to whatever the parent is where it is writen. It is often used within Constructors and Class objects.
* **Test Driven Development (TDD)** - A development style where tests are the first bit of code written, acting as the MVP required when developing a functional piece of code.
* **Jest** - A testing software used with node.js.
* **Continuous Integration (CI)** - A development practice where developers integrate their code into a shared mainline multiple times per day.
* **unit test** - A software testing practice where unit tests are written against individual units of code.

## Sources:

* Article: [9 Benefits of Test Driven Development](https://www.madetech.com/blog/9-benefits-of-test-driven-development)

* Article: [Benefits of Test-Driven Development](https://medium.com/@MasterOfCodeGlobal/benefits-of-test-driven-development-64a24bbe743e)

* GitHub Wiki: [BeforeEach and AfterEach](https://github.com/pester/Pester/wiki/BeforeEach-and-AfterEach)

* Article: [Static Methods in ES6](https://medium.com/@yyang0903/static-objects-static-methods-in-es6-1c026dbb8bb1)

* Article: [Understanding Higher-Order Functions in JavaScript](https://blog.bitsrc.io/understanding-higher-order-functions-in-javascript-75461803bad)

## Additional Resources:

* Video: [TDD in JS](http://www.letscodejavascript.com/)

* Video: [Javascript context tutorial](https://www.youtube.com/watch?v=fjJoX9F_F5g)

* Docs: [Inheritance and the prototype chain](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)

* Docs: [this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)

* Docs: [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

* Docs: [Jest Documentation](https://jestjs.io/docs/en/setup-teardown)

* Docs: [MDN - Static](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/static)