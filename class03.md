[Table of Contents](README.md)

# Data Modeling & NoSQL Databases

## Research Questions:

1. Why would a developer choose to make data models?

    A data model is a visual diagram that shows the relationship between all of the data being used in a n application and the data's real world counterparts. A primary reason developers would make and use data models is to help visualize how their application recieves and processes data. Having a visual representation on the data flow will help when creating the functional code that recieves and manipulates that data.

2. What purpose do CRUD operations serve?

    CRUD operations are a core component of many different types of applications. The acronym `C.R.U.D.` stands for:

    * Create
    * Read
    * Update
    * Delete

    CRUD operations are used when persisting data to storage. In the case of RESTful API's, CRUD operations would be the http methods like `GET`, `POST`, `UDATE` and `DELETE`. Though it's common so see CRUD operations within a REST API, any time you are manipulating persistent storage you will be using some variation of CRUD operations.

3. What kind of database is Postgres? What kind of database is MongoDB?

    Postgres is an SQL style database, SQL meaning structured query language. Postgres is a type of relational database, storing data in related tables. Entries in a table are referred to as records. Each table is regulated by a schema file and all data that goes in to that table has to adhere to the scheme file. The tables are related to one another by use of primary and foreign keys.

    MongoDB, on the other hand, is a NoSQL style database. With MongoDB, data is stored in collections. Each entry in a collection is called a document. The data in NoSQL databases is formatted in JSON. 

4. What is Mongoose and why do we need it?

    Mongoose is an ORM, or object relational mapping library designed to be used with MongoDB and Node.js. Since NoSQL databases do not use a schema by default, Mongoose helps to manage relationships between data collections and provides a scheme-like validation. It's a very useful tool to use when working with MongoDB. 

5. Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.

    Say we have an application that allows a user to order books. In this application, three related pieces of data would be the user, the book and the user's order. These three things are all separate pieces of data but are also related in the fact that they work off of each other. Each order requires a user and a book. You can't have an order without a user to place that order. The order has to have content, hence the book. While they are all three separate pieces of data themselves, they are related to each other in that the the user and book makes up an order. Without a user and a book, there would be no order placed.

## Vocabulary:

* `database` - A collection of persistent data. Can be both on a local machine and cloud based.
* `data model` - A visual diagram that shows the relationship between all of the data being used in a n application and the data's real world counterparts
* `CRUD` - Stand for Create, Read, Update and Delete. Describes the basic functions of manipulating persistent data inside of a database.
* `schema` - A file used as a blueprint for how data should be formatted inside of a database. 
* `sanitize` - The process of examining a collection of data and permanently and irreversibly destroying  data that is unwanted. This is commonly used to remove data that does not pass validation or data that is potentially malicious.
* `Structured Query Language (SQL)` - A database style that uses relational tables to store data based off of a schema file. Specific syntax is used to make queries of the database. Typically a more secure way to store data at the expense of speed.
* `Non SQL (NoSQL)` - A database style that does not use schemas to format the data. The data is stored in collections, written in JSON. The collections are not inherintly relational in nature. While not as secure as SQL databases, NoSQL databases typically offer greater speed when reading and writing into the database.
* `MongoDB` - A popular NoSQL database software that can be hosted either locally or in the cloud. It stores data as JSON documents within collections.
* `Mongoose` - A third party JavaScript library that is designed to be used with MongoDB and node.js. It offers increased control and validation when manipulating data.
* `record` - A data entry in a SQL style database.
* `document` - A data entry in a NoSQL style database.
* `Object Relation Mapping (ORM)` - The idea of being able to write queries, such as the ones used in typical SQL, using the object-oriented paradigm of your preferred programming language. Essentially, it is interacting with a database with the language of your choice instead of SQL.

## Sources:

* Wikipedia: [Data Modeling](https://en.wikipedia.org/wiki/Data_model)

* Article: [What is an ORM and Why You Should Use it](https://blog.bitsrc.io/what-is-an-orm-and-why-you-should-use-it-b2b6f75f5e2a)

* Article: [Data Sanitization](https://www.webopedia.com/TERM/D/data-sanitization.html)

## Additional Resources:

* Cloud-based mongoDB services:
    * [MLab](https://www.mlab.com/)
    * [Atlas](https://www.mongodb.com/cloud/atlas)
    * [DynamoDB](https://aws.amazon.com/dynamodb/)
    * [CosmosDB](https://cosmos.azure.com/)

* Video: [SQL vs NoSQL or MySQL vs MongoDB](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

* Article: [SQL vs NoSQL Database Differences Explained with few Example DB](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

* Article: [NoSQL Data Modeling Techniques](https://highlyscalable.wordpress.com/2012/03/01/nosql-data-modeling-techniques/)

* Docs: [Mongoose](https://mongoosejs.com/docs/guide.html)