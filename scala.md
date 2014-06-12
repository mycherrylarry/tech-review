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


#### String casting: **implicit**
*  **Scala.Predef** hasdefined may implicit methods before compiling, such as StringOpt: 
 
``` 
implicit def augmentString(x : scala.Predef.String) : scala.collection.immutable.StringOps = { /* compiled code */ }
```

* [Context Bound and View Bound](http://stackoverflow.com/questions/4465948/what-are-scala-context-and-view-bounds)

* *pimp my library pattern* and *[typeclass pattern](http://www.casualmiracles.com/2012/05/03/a-small-example-of-the-typeclass-pattern-in-scala/)*

