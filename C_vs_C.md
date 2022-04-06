# C vs C++
Here I'm gonna list things which i thing will be useful in c
from c++ but not available in c.

Now that i'm writing this and learning now i know what C++ OOP stuff
really is and i think Polymorphism is a main thing. Because whenever i wanna
do something in c most of the time i couldn't do it because i came from
a python bacakground. And i didn't know i was really missing is polymorphism.
But actually i didn't know polymorphic functions is a thing because in Haskell
it's natural to have higher order function and function composition and functions
as first class citizen. This all enables because of Parametric Polymorphism.


## Note:

All things available in C is also available in c++.
But it's not the other way around.

So, When something is missing in c i wrote the exact
code in c but with .cpp extension and compile it
with a cplusplus compiler like (clang++, g++, zapcc++).

I know it's a Clever Hack that C programmers using
for a long time. In fact they're doing it just to
mock C++ programmers and frustrate them.


## Pointers and Reference

Pointers point towards a memory address. And Reference is just
a Syntactical Sugar around it.

- Pointers available both in  c/c++.
- Reference is a C++ thing.

I mean there is reference but not with a nice syntactical sugar like
in c++.

Ex: Pointers

~~~cpp
int* a = &x;
*a + 20;		//Access them
~~~

Ex: Reference
~~~cpp
int& a = x;
a + 20;
~~~
Tell me which looks good.

[cplusplus.com/tutorial/pointers](http://www.cplusplus.com/doc/tutorial/pointers/)

- & is the reference operator and can be read as “address of”.
- * is the dereference operator and can be read as “value pointed by”.
