# MVC and DDD
## My understanding of MVC
architecture:

* What is MVC
* What is MVC used for
* Why MVC (Benefits)
* MVC's components

**Model-View-Controller** which also called MVC is a kind of software architecture design parrtern that used to implement web user interfaces. 

MVC is mostly used for designing and implementing web applications. It is used by many modern software frameworks such as Play Framwork, Ruby Rails, Django and so on.

By using MVC, the application is divided into seperate parts, which cooperate with each other by the data flow. With the seperation of code between these three different parts, you obtain a seperation in web application logic.
The application is divided into three different parts: Model, View and Controller. This allows for each portion to be designed, implemented and tested independently from one another.

There're three components of MVC, Model, View, Controller. We'll talk about them in detail in the next chapter.

[Reference](http://www.onextrapixel.com/2012/03/14/a-detailed-overview-of-the-model-view-controller-mvc-coding-structure/)

## My understanding of  DDD



* [**Domain-Driven Design and MVC Architectures**](http://blog.fedecarg.com/2009/03/11/domain-driven-design-and-mvc-architectures/)

* [**Domain-Driven Desing: Data Access Strategies**](http://blog.fedecarg.com/2009/03/12/domain-driven-design-and-data-access-strategies/)

* DDD is a way of thinking how to manage codes and strucutres. You can use DDD to organize the MVC's Module, which makes your code more precise and clear.

* DDD shows an innovatinal method of constructing business logics. It introduces terms as Entity, Value Object, Repository and Service.

* Entity is an immutable Object with unique identity. 
* Value Object is an Object with no identity, represents some common values of Entities. Such as constant.
* Repository is used to create, delete, and update entities from different database implementations.
* Service provides operations for a particular usage. For example, methods for controllers.


