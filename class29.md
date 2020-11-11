[Table of Contents](README.md)

# Hash Tables

## Review, Research and Discussion:

What are hash tables? Hash tables are a way to store data inside of an array and be able to retireve that data with an O(1) time complexity. Unlike simply looping through an array to see if a value exists, hash tables are made up of key value pairs and the key is used to instantly go right to the index that contains the value. One of the traits of a hash table is that the array that it is assiciated with has to have a predetermined size. The reason for this will be addressed below.

Inside of each index of the hash tables array are what we call buckets. These buckets are able to store more than one key value pair. While a perfect hash table has one one pair per bucket, it's not bad for a bucket to have multiple pairs. When more than one pair is assigned to the same bucket, we call this a collision. To make the handling of collisions easier, the inside of a bucket is made up of a linked list so that each time a pair is placed in a bucket, it is appended to the end of the linked list. So if you know the key of the value you are looking for, you can get the hash of the key which will point directly to the index in the array where the value is stored. Now you're probably asking what a hash is.

A hash is simply a ket in the form of a string that is run through an algorithm that returns a number. The number is then used as the index for the key value pair to be stored. The hash can be calculated many different ways so long as the resulting index value is within the length of the array. This is the reason that a hash tables array needs a set length. 

A hash table has four primary internal methods:
-  `add()` - Adds a key value pair hashing the key and then storing the whole key value pair into the index that was determined by the hash.
- `find()` - Gets the hash of the key to determine which index of the array to go to and then uses the key to assert that the value is there and returns it. In the case that the bucket containinf the key is a linked list, meaning the bucket has mulitple key value pairs, the `find()` method will also iterate the linked list to get the correct pair.
- `contains()` - Gets the hash of the key to determine which index of the array to look in. Checks to see if the bucket contains the key value pair that corresponds to the provided hashed key and returns a boolena value.
- `getHash()` - Takes a key, which will be a string, and runs it thorugh an algorithm that reuurns a number that will corresponf to a soecific index of te hash tables array.

## Vocabulary:

* `Hash` - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.  
* `Buckets` - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
* `Collisions` - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

## Additional Resources:

* Article: [Hashtables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
* Video: [What is a HashTable Data Structure - Introduction to Hash Tables , Part 0](https://www.youtube.com/watch?v=MfhjkfocRR0)
* Article: [Basics of Hash Tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)
* Wikipedia: [Hash table](https://en.wikipedia.org/wiki/Hash_table)