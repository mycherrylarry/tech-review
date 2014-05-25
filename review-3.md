## Scala 

#### String casting: **implicit**
*  **Scala.Predef** hasdefined may implicit methods before compiling, such as StringOpt: 
 
``` 
implicit def augmentString(x : scala.Predef.String) : scala.collection.immutable.StringOps = { /* compiled code */ }
```

* [Context Bound and View Bound](http://stackoverflow.com/questions/4465948/what-are-scala-context-and-view-bounds)

