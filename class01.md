[Table of Contents](https://joepennock-401-advanced-javascript.github.io/401-reading-notes/)

# Node Ecosystem, TDD, CI/CD

## Research Questions:

1. Why would you want to run JavaScript code outside of a browser?

    JavaScript can be run outside of the browser for a couple different reasons. Probably one of the primary reasons for this is for backend developmet using node.js to interact with and create server applications and RESTful APIs. Node.js is a JavaScript runtime environment, meaning that it allows JavaScript code to be written and tested without the use of a browser. 

2. What is the difference between a module and a package?

    In relation to node.js and npm, many npm packages are also modules and many modules are also packages. But this is not always the case. There are a few requirements to be considered either a package or a module.

    A module is any file or directory in the `node_modules` directory that can be loaded by the node.js `require()` function. According to the official [npm](https://docs.npmjs.com/about-packages-and-modules) documentation, a file or directory needs to fit one of three criteria to be classified as a module:
      1. A folder with a `package.json` file containing a 'main' field
      2. A folder with an `index.js` file in it
      3. A JavaScript file

    A package, on the other hand, is any file or directory that is described by a `package.json` file. 

3. What does the node package manager do?

    The node package manager, more commonly referred to as npm, is an open source software registry. It contains thousands of packages containing often specialized libraries that do one specific thing well. Developers can publish packages they have written to do something or use a package written by someone else to help improve their code. Some of the benefits of using npm are:
      * Saves time by using a library to perform a task, requring less actual code to be written
      * Use outside expertise to bolster your code
      * Save and recycle your own code via packages

4. Provide code snippets showing 3 different ways to export a function from a node module:

    1. Requiring an npm mudule:
    
    ```
    const someModule = require('someModule.js')
    ```

    2. Creating and exporting a module:
    
    ```
    First, create a user.js file and this code:

      const getName = () => {
        return 'Joe';
      }

      exports.getName = getName;

    Now, creat an indes.js file and add the following:

      const user = require('./user');
      console.log(`User: ${user.getName()}`);

    In the terminal, if you run the command `node index.js` you should get `User: Jim` as the output.
    ```

    3. Using the exports shortcut:

    ```
    Inside a file called helloWorld.js:

      module.exports = exports = function() {
        console.log('Hello World!');
      }

    Then, inside of index.js:

      const helloWorld = require('./helloWorld.js');
        helloWorld(); 

    Invoking the function inside of index.js should print 'Hello World!' to the console.
    ```

## Vocabulary:

* ecosystem - "a collection of software projects, which are developed and co-evolve in the same environment" - [Mircea Lungu](https://mircealungu.github.io/)
* Node.js - a JavaScript runtime environment that allows JavaSvript development outside of the browser, often used for testing and backend development
* V8 Engine - Google's open source JavaScript engine, written in C++. It is utilized in both Google Chrome and in Node.js
* module - a file or directory loaded in node.js, often containing a specialized js library
* package - a file or directory containing a package.json file 
* node package manager (npm) - an open source software registry containing js code libraries
* server - a backend program or machine that deals directly with the database, separate from the frontend application
* environment - space in which a framework is run, determined by its makeup of hardware, software and or other variables
* interpreter - a program that reads and executes code in a structured manner
* compiler - translates code written for human understanding into a code to be executed by a computer

## Sources

* [https://nodejs.org/en/docs/](https://nodejs.org/en/docs/)
* [https://docs.npmjs.com/](https://docs.npmjs.com/)
* [https://www.sitepoint.com/understanding-module-exports-exports-node-js/](https://www.sitepoint.com/understanding-module-exports-exports-node-js/)
* [https://nodejs.org/api/modules.html](https://nodejs.org/api/modules.html)
* [https://v8.dev/](https://v8.dev/)