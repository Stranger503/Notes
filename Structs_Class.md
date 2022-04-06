# Why we need Struct

* To create more sophisticated user defiend data types.
	* In simple words creating Abstraction to deal with complexity.

## How different from class

* Everything in struct by defualt is Public in class it's private.
* And in Class u have inheritence and OOP stuffs.


## Note

On the internet everybody talks about members of a class or methods i hate them truly i don't like them. Lots of unnecessary ambiguity.

Members of structs .... Aaaaahh disgusting.

~~Methods~~ -> Functions
~~Memeber~~ -> Data Element


One good definition i found on the internet.

## Struct
A data structure is a group of data elements grouped together under one name.

In other words ~~struct~~ is not only used to create data types but also Data Structures.

Class -> Heap
Struct -> Stack

## Namespace
By default it looks almost similar to Struct and Class and Namespaces. In struct and class you can create an structure variables or an object to change the valuea outside of the struct and class. But in Namespace you can't change value outside of the namespace it's very similar to a function actually. Immutability by default; but you can access them outside the namespace. In fact that's the whole point of namepsace. BTW you can only declare and define Namespaces in Global Scope it's because it can be available to all other functions. At the same time you're not mutating a global variable in other scopes Bad Habits. But in Namespace you cannot.


Lifetime -> same as Global(Thorough out the program).; Same as ~~Static~~.
Memory -> Data Segments.



~~Global(static storage) vs Local(automatic storage)~~:
-> Exist Enire program		-> Exist only until the function returns.
	Execution.
-> Data Segmenets				-> Call Stack
