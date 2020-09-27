[Table of Contents](README.md)

# Event Driven Applications

## Review, Research and Discussion:

1. Why is access control important?

    Access control is important because, as the name implies, it allows you to control who has access to various CRUD methods on your app. Since access control is given after a valid signup/signin, you can asign roles to anyone who signs in, potentially limiting their capabilities. For example, a guest user visiting a news blog would not need, nor would you want them to have, the ability to create content. So when building access control into your api, one thing you might do is restrict access to `POST` routes to only the users who need to create new content such as authors and admin accounts. By properly implementing access control into all of your CRUD routes, you can better ensure that resources are created or deleted unecessarily. 

2. Describe an application that would need access control.

    As in the above example, one type of application that would need access control is a  news blog. Another type of app that might need access control is an online store. By giving roles to specific users, you would have less chances of product inventory being accidently or intentionally wrongfully modified. If a consumer account had access to create or update routes, for example, they could potentially modify the price of various products allowing them to purchase for below the value of the product. Enuring that all new users have the appropriate level of access control would be providing an additional level of security to your procuct inventory.

3. What is a role used for?

    A role is a property assigned to a user that shows what that users capabilities are. For example, a user with the role of `admin` will have the access to any of the available CRUD routes. And a user with the roll of `shopper` will only have access to routes that are used to purchase a product, for example. Roles are typically assigned upon the creation of a new user.

4. Why is role based access control more scalable than discretionary or mandatory access control?

    The reason RBAC is more scalable than MAC or DAC is because there is no limit to the amount of roles that can be set for the ACL. Roles can be created as need to allow access to any combination of pieces of an API server. These roles can then be set to the appropriate users and updated/changed as necessary.

    DAC is more used when allowing each individual user to manage the content they own. As such, DAC is limited to the scope of each individual user. 

    MAC is more for sytem level access. Such as limiting access to core components of a system or a server. Using MAC, set a root system admin account and give it root permissions. Then, no matter what roles a user may have, only the root system admin account would be able to access content on the root of a system.

    With RBAC, there is flexibility to grow and add roles as needed and user that need that flexibility won't be locked out as new content is added to the system.

## Vocabulary:

* `Authorization` - If authentication is confirming you are who you say you are, then authentication would be saying yoy can do these things now that we have confirmed your identity. Authorization is what RBAC allows. 
* `Role Based Access Control` - RBAC is an access control paradigm in system securty that sets various roles in an Access Control List, or ACL. The roles in the ACL are then assigned to users depending on what permissions those users need. 
* `Capabilities` - Capabilites are the permission granted to a user based on their role. For example, an admin role may have the capabilities to `create`, `read`, `update` and `delete` where a guest role may only have the capability to `read`. 


## Preview: 

1. What is something had you heard about previously and now have better clarity on?

    1. Event-Driven Programming. I had heard of the concept back in 301 but knew of it only vaguely from reading about jQuery event listeners. Now I realize that it's much more of an approach to programming itself, or rather a programming style than I had realized just from using `$('foo).on('click', callBAck)` and such from 301.

2. What are some things are you hoping to learn more about in the upcoming lecture/demo?

    1. The `Main Loop`.
    2. Creating real-time event listeners froms scratch.

3. What are you most excited about trying to implement or see how it works?

    1. Creating my own event listeners
    2. Having listeners dynaically handle events in real time and relay those events to other handlers. Essentially, have events "talk" to each other. 

## Additional Resources:

* Article: [Event-Driven Programming in Node.js](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)
* Documentation: [Node.js v14.12.0 Documentation](https://nodejs.org/api/events.html)
* Article: [MAC vs DAC vs RBAC](http://www.cloudauditcontrols.com/2014/09/mac-vs-dac-vs-rbac.html#:~:text=Discretionary%20Access%20Controls%20(DAC)%20and,of%20permissions%20to%20those%20groups.)
* StackExchange: [MAC vs DAC vs RBAC](https://security.stackexchange.com/questions/63518/mac-vs-dac-vs-rbac)
