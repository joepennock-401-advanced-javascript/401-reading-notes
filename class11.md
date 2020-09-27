[Table of Contents](README.md)

# Authentication

## Review, Research and Discussion:

1. Explain what a “Singleton” is (in Computer Science terms).

    A Singleton is a design patternt that limits a class or object to a single instance. This single instance can then be used in multiple places thoughought an application to help provide consistent access to that object or class. Use of a Singleton will essentially provide global access to the one instance of the class or object.

2. Explain how the Singleton pattern can be used with Node modules, specifically with classes.

    When a Singleton is used inside of node.js, you can ensre that only a single instance of a class or object is created. This can be taken a step further with modularization.
    
    If you were to create a class in its own module, do some work inside the class, then export that class, you would then be able to create new instances of that class in other modules so long as you 'require' in the file containing that class. In many cases, this is not an issue. In fact, you may very well want to use a new instance of that class in multiple locations. But what if you don't? If, in fact, it would behoove you to always use a sinlge instance of the same class in multiple locations, you would want to use a Singleton. 

    Lets say we have a module containing a class for error handling. We can create the class, do the logic required, and then export the class. But instead of just using `module.exports = className`, we could use a singleton by exporting a new instance of the class. It might look something like this:


    ```
    class errorHandler {

      // do stuff in here to handle errors
      // maybe keep a record of error logs
      // let errorLogs = [];

    };

    module.exports = new errorHanlder()
    ```


    By creating a new instance of `errorHandler` as the object that is being exported, we are creating a Singleton. This way, the instance of `errorhandler` that we export is the only instance we will gave access to. So in other modules, instead of using `let foo = new errorHandler()`, we simply require in the file containing the Singleton. Now, everwhere we use this instance will be the same one as the one that is exported.

3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

    If I were to go about creating a fully functioning middleware system on the scale of what is used in Express, I would first map out what all function need to happen in the various pieces of middleware. Do we need a logger function to log what methid is being called or the path we are calling it on? Maybe we would want some sort of way to timestampe our requests. Or we might want some sort of validation function. Regardless, having a list of required functions would be the first step.

    Once I figured out what all middleware I needed, I would put them into their own modules. This way, it keeps them all separate so it would be easier to identify issues or bugs. Also, having them all in their own modules would easily allow each one to be called as needed. So instead of running all middleware at once, they would all be run off of the Express object as needed. This would give the user more control over what middleware they are using and easy access to each piece.

## Vocabulary:

* `Router Middleware` - Router middlewatre is used as a go between for your routes and your server file. Instead of having all of your routes directly on the server file, you can use a router to keep all the various routes needed in their own modules. 
* `Dynamic Module Loading` - The practice of loading modules on the inital application start. This allows desired modules to be 'pre-loaded', giving the application access to them from the beginning.
* `Singleton Pattern` - A software design pattern that limits the instantiation of an object or class to a single instance. This can be used gloabally to allow access to the single instance anywhere in the application.
* `CRUD -> REST Method Matches` - 
  * Create === POST
  * Read === GET
  * Update === PUT/PATCH
  * Delete/Destroy === DELETE
* `Mock Testing` - Mock testing is a process of writing unit tests for units that require exernal dependencies. By mocking the data, we can simulate how those dependencies would work and instead of focusing on those dependencies, we can focus on the function of the unit being tested.

## Preview: 

1. Which 3 things had you heard about previously and now have better clarity on?

    1. .
    2. .
    3. .

2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

    1. .
    2. .
    3. .

3. What are you most excited about trying to implement or see how it works?

    1. .
    2. .
    3. .

## Sources:

* Wikipedia: [Singleton pattern](https://en.wikipedia.org/wiki/Singleton_pattern)
* Article: [Node.js Design Patterns — Singleton pattern ( Series -1)](https://medium.com/@maheshkumawat_83392/node-js-design-patterns-singleton-pattern-series-1-1e0ab71e3edf)
- Documentation: [Writing middleware for use in Express apps](https://expressjs.com/en/guide/writing-middleware.html)

## Additional Resources:

* Wikipedia: [Basic access authentication](https://en.wikipedia.org/wiki/Basic_access_authentication)
* Article: [Introduction to JSON Web Tokens](https://jwt.io/introduction/)
* Cheat sheet: [Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
* npm package/documentation: [node.bcrypt.js](https://www.npmjs.com/package/bcrypt)