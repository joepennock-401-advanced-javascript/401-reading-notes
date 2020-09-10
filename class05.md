[Table of Contents](README.md)

# Linked Lists

What are linked lists? Essentially they are a data structure that can be used to organize data. Linked lists are a sequence of nodes that are connected to each other. Using the `Next` keyword, each node references the next node in sequence. There are two types of Linked Lists, singly and doubly. Singly and Doubly simply refer to how many references each node has. First, let's look at the terminology that makes up Linked Lists:

#### Linked List Terminology

* `Linked List`: A data structure that contains nodes that link to the next node in the list. 
* `Node`: The individual item that contains the data for each link in the sequence.
* `Singly`: This refers to the number of references a node has. In a singly linked list, each node only has one reference which always points to the `Next` node in the list.
* `Doubly`: This means that each node in the list now has two references, one pointing to the `Next` node and one to the `Previous` node.
* `Head`: This is a reference to the first node in the sequence.
* `Next`: A property of each node in a Linked List that points to the next node.
* `Current`: This is a reference to the current node being examined. Used when traversing through a linked list.
* `Traversal`: The process of maneuvering through all nodes of a linked list.

Now that we know what a Linked List is and the components that make them up, let's take a look at how a Linked List works. For our current use case, we will be discussing a Singly Linked List.

![Linked Liset Diagram](/resources/linkedListDiagram.jpeg)

In the above diagram, we can see that a linked list is a linear data structure. This simply means that there is a sequence, or order, to how the linked list is made and how it is traversed. Each node in the linked list has two components: the data the node contains and a pointer to the next node. The last node in the sequence will have a value of `null`, indicating that there is no `next` to traverse to. 

While you might be thinking this seems a lot like an array, you're not far off. Arrays and Linked Lists are similar in thay they both are data structures that hold collections of other data structures. One of the key differences between the two is the way they use CPU memory. Arrays require a contiguous block of memory to be created, relational to the size of the array itself. So if an array holds 100kb of data, it will requre 100kb in one solid block. Linked lists, on the other hand, are dynamic in that each byte of data that makes up a linked list can live independently in your computers memory. The end result is thay linked lists are very lean to create and run, requiring much fewer resources than some other data structures. 

Ok, now that the what and why is out of the way, lets take a look at how my might be able to navigate around a linked list. Here's pseudo code example of a linked list in action: 

```
ALGORITHM traverse(LinkedList)

  VARIABLE current = LinkedList.Head

  WHILE current NOT EQUAL TO null

    check(current.Value)
    current = current.Next

  RETURN;
```

Basically, what we are doing is setting the first node equal to `head` which is the start of our linked list. Then, using a while loop, we will keep checking to see if the value is true or not. If we can keep assigning current to another node, it means we have not yet reached the end of the linked list, hence the use of the while loop.

These are just some of the very basic concepts of a linked list. Check out some of the resources below for more info on what linked lists are and how to use them.

## Additional Resources:

* Article: [Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

* Article: [What’s a Linked List, Anyway? - [Part 1]](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

* Article: [What’s a Linked List, Anyway? - [Part 2]](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

* Article: [Introduction to Linked Lists](https://www.cs.cmu.edu/~adamchik/15-121/lectures/Linked%20Lists/linked%20lists.html)

* Article: [Linked Lists: The Basics](https://people.engr.ncsu.edu/efg/210/s99/Notes/LinkedList.1.html)