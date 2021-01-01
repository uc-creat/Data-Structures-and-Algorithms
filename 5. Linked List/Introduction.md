# Linked List:

### Array:

We all know arrays, arrays is a data structure which can store multiple values of same data type in a sequencial manner. So for eg: 
an array can store 100 integers or 1000 floating numbers, etc.



![array](https://user-images.githubusercontent.com/60755716/103444081-3ea38100-4c8b-11eb-878d-1be93d02d9ef.png)


Like in the above picture, we can see that each element in array 'a' can be accessed through indexing. Index of an array usually starts from 0.
So, if we want to access an element for eg: 7 from the above array 'a', we can do this by - 
``` py

a[3]

```
So, if we can store elements in array, then what is the need for linked list?

### linked list:

The problem with arrays is the fixed amount of space which it provides. Sometimes, there can be a need when we actually don't know as how much size of the array to be 
considered. So, we want some data structure which stores elemetns, but dynamically. Which means that, we want such a data structure which can store elements, and increase
or decrease the size depending upon the input. So in this case we do not have to worry about the size of the data structure.
Arrays have fixed amount of space, and cannot increase or decrease this space.
Linked list overcomes this problem.

In python, first we create a 'node' for a linked list. 

#### Node:
Node a simply a collection of two parts.
1. Data
1. Address of the next node.

![address](https://user-images.githubusercontent.com/60755716/103444220-a3aba680-4c8c-11eb-873e-ee8c79aeddd1.jpg)

Like in the above picture, we can see of how a node can be visualized. Now, this node is specified in the memory.
So, whenever we call a node, we have to specify two fields of it.. one is data field, while other is the address field.

So, now if we want to connect multiple nodes, we simply have to specify the address of one node in the address field of the first node, like shown below - 

![connection](https://user-images.githubusercontent.com/60755716/103444227-b58d4980-4c8c-11eb-9237-6862656bc17a.jpg)

In the above example, we can see that, the first node which is also mentioned as 'head' contains the address of second node. 
While, the second node consists the address of last node, also called as tail of the linked list.
As, after the tail node, there are no more nodes, therefore, tail node have 'NULL' as the address value in the address field.
Basically, here we are creating a link between the nodes by specifying the address of one node in the address field of the other node.
Due to this link, we can traverse through these connections.

This connection of nodes is known as Linked list (lists/arrays which are linked together by 'links')




