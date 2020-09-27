[Table of Contents](README.md)

# Access Control

## Review, Research and Discussion:

1. Why is access control important?

    Access control is important because, as the name implies, it allows you to control who has access to various CRUD methods on your app. Since access control is given after a valid signup/signin, you can asign roles to anyone who signs in, potentially limiting their capabilities. For example, a guest user visiting a news blog would not need, nor would you want them to have, the ability to create content. So when building access control into your api, one thing you might do is restrict access to `POST` routes to only the users who need to create new content such as authors and admin accounts. By properly implementing access control into all of your CRUD routes, you can better ensure that resources are created or deleted unecessarily. 

2. Describe an application that would need access control.

    As in the above example, one type of application that would need access control is a  news blog. Another type of app that might need access control is an online store. By giving roles to specific users, you would have less chances of product inventory being accidently or intentionally wrongfully modified. If a consumer account had access to create or update routes, for example, they could potentially modify the price of various products allowing them to purchase for below the value of the product. Enuring that all new users have the appropriate level of access control would be providing an additional level of security to your procuct inventory.

3. What is a role used for?

    A role is a property assigned to a user that shows what that users capabilities are. For example, a user with the role of `admin` will have the access to any of the available CRUD routes. And a user with the roll of `shopper` will only have access to routes that are used to purchase a product, for example. Roles are typically assigned upon the creation of a new user.

4. Why is role based access control more scalable than discretionary or mandatory access control?

## Vocabulary:

* `Authorization` -  
* `Role Based Access Control` - 
* `Capabilities` - 


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

* Video: [Role Based Access Control](https://www.youtube.com/watch?v=C4NP8Eon3cA)
* Article: [5 steps to simple role-based access control](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)
- Wikipedia: [Role-based access control](https://en.wikipedia.org/wiki/Role-based_access_control)

## Additional Resources:

* Article: []()
