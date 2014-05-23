## Java Concurrency

### Books

* [Java Concurrency in practice](http://www.periodicooficial.oaxaca.gob.mx/files/2011/05/EXT02-2011-05-19.pdf)

### Tips
* Prefer using executors and tasks to threads.
* Pay attention to java.util.concurrent which includes three parts such as Executor Framework, Concurrent Collections and Synchronizers.


## DDD and MVC

* [**Domain-Driven Design and MVC Architectures**](http://blog.fedecarg.com/2009/03/11/domain-driven-design-and-mvc-architectures/)

* [**Domain-Driven Desing: Data Access Strategies**](http://blog.fedecarg.com/2009/03/12/domain-driven-design-and-data-access-strategies/)

* DDD is a way of thinking how to manage codes and strucutres. You can use DDD to organize the MVC's Module, which makes your code more precise and clear.

* DDD shows an innovatinal method of constructing business logics. It introduces terms as Entity, Value Object, Repository and Service.

* Entity is an immutable Object with unique identity. 
* Value Object is an Object with no identity, represents some common values of Entities. Such as constant.
* Repository is used to create, delete, and update entities from different database implementations.
* Service provides operations for a particular usage. For example, methods for controllers.


## Scala

#### andThen
* **andThen** puts the result of the prvious method to the parameter of the following method.

```
object MethodA extends(Int => String) {
	def apply(m: Int): String = "hello " + m.toString
}

object MethodB extends(String => String) {
	def apply(s: String): String = s + " end"
}

val mx = MethodA andThen MethodB
mx(1) // expected hello 1 end

```
is the same as

```
def methodA(m: Int): String = "hello " + m.toString

def methodB(s: String): String = s + " end"

val mx = methodA _ andThen methodB _
mx(1) // expectd hello 1 end
```
but in the first example, "**_**" is not needed


