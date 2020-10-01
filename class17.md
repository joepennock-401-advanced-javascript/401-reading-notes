[Table of Contents](README.md)

# TCP Severs

## Review, Research and Discussion:

1. Given the examples of front-end events such as button click, window resize, form submit, etc, what are some examples of back-end events?

    When a user clicks on a button and fires of an event to submit a form, there is also an event that happens on the back-end to:
      1. recieve the data
      2. verify that the data is valid
      3. process data

2. Why are events sometimes better than asynchronous actions with callbacks?

    Events are something that has already happened whereas asnync callbacks are waiting to be called in order to run. 

3. What does an EventEmitter instance do?

    In Node.js, the EventEmitter is a class. All objects that emit events are instances of the EventEmitter class. A single instance of the EventEmitter can be used to have all events listen/emit on the same instance, therefore allowing them to communicate.

4. When is a program’s call stack, event queue, and event loop active?

    The call stack and event queue contain all operations to be executed in a program. Tne event loop will run asynchronously, checking to see if the call stack is empty. Once the call stack is empty, there are no more operations to be run, then the event loop will end.

## Vocabulary:

* `Event Driven Programming` - A programming paradigm where the flow of the program execution is determined by events. 
* `Observer Pattern` - A programming design pattern that defines a one-to-many relationship wherein if the state of the 'one' is changed, the 'many' are changed and updated automatically.
* `Listener` - A function within a program whose sole puspose is to wait for a specified event to happen and when that event happends, do some stuff.
* `Event Handler` - A fucntion that is typically tied to a listener. When the event happens that the listener is waiting for, it's the event handler that does something in respose to the awaited event.
* `Event Loop` - The paradigm, or perhaps the process by which JavaScript manages events or fucntions and the order in which they are executed. It is a behind the scenes part of JS that itslef manages the call stack event queue.
* `Event Queue` - A part of the event loop that handles, in queue FIFO format, all the messages that are to be processed. Each message in the event queue will have some function attached to it which gets called to handle the message.
* `Call Stack` - A part of the event loop that keeps track of all operations to be executed, in a stack FILO format. When a function is finished, the stack pops it off the top.
* `Emit/Raise/Trigger` - 
    * `Emit` - Emitters are what fire off events. 
    * `Raise` - ???
    * `Trigger` - Triggers signal that an event or action was completed.
* `Subscribe` - Subscribe an event handler to a specific event.
* `Database` - A structured collection of data that can be accessed, added to or manipulatd. A database is used when persisting data. There are many types of databases, but are essentially split into relational (SQL) and non-relational (NoSql).

## Preview: 

1. What are some things had you heard about previously and now have better clarity on?

    1. The inner working of how networks communicate.
    2. Internet protocols.
    3. What TCP/IP is and how it differs from OSI.

2. What are some things are you hoping to learn more about in the upcoming lecture/demo?

    1. Importance of TCP/UDP in web development.
    2. How the OSI model affects us as devs.

3. What are you most excited about trying to implement or see how it works?

    1. Building out a server with OSI model in mind.
    2. Further devloping an understanding of internet protocols.

## Additional Resources:

* Wikipedia: [Event-driven programming](https://en.wikipedia.org/wiki/Event-driven_programming)
* Article: [Design Patterns — A quick guide to Observer pattern](https://medium.com/datadriveninvestor/design-patterns-a-quick-guide-to-observer-pattern-d0622145d6c2)
* Wikipedia: [Event Loop](https://en.wikipedia.org/wiki/Event_loop#:~:text=In%20computer%20science%2C%20the%20event,or%20messages%20in%20a%20program.)
* Video: [OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)
* Video: [TCP - Three-way handshake in details](https://www.youtube.com/watch?v=xMtP5ZB3wSk)
* Article: [What Is The OSI Model?](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)
* Article: [TCP (Transmission Control Protocol)](https://searchnetworking.techtarget.com/definition/TCP)
* Article: [Node.js: Simple TCP Server & Client and Promisify the Client](https://techbrij.com/node-js-tcp-server-client-promisify)
* Documentation: [Node Docs - Net](https://nodejs.org/api/net.html)
