---
layout: post
title: Blogging Like a Hacker
---


#### Lazy Values

Lazu values are useful to delay costly initialization statements.

```scala
lazy val words = scala.io.Spource.fromFile("/usr/share/dict/words").mkString
```

> Laziness is not cost-free. Every time a lazy value is accessed, a method is called that checks, in a threadsafe manner, whether the value has already been initialized.

## Exception

```scala
throw new illegalArgumentException("x should not be negative")
```

#### No checked exception in Scala

No function or method need to throw an exception.

#### A `throw` expression has the special type `Nothing`

That is useful in if/else expressions. If one branch has type Nothing, the type of the if/else expression is the type of the other branch.

```scala
// The if statement has a type Double
if (x >= 0) { sqrt(x)} else throw new IllegalArgumentException("x should not be negative")
```

#### Try-catch clause

```scala
try {	process(new URL("http://horstmann.com/fred-tiny.gif"))} catch {	case _: MalformedURLException => println("Bad URL: " + url) 
	case ex: IOException => ex.printStackTrace()}
// "_" here means the variable name is no needed.
```
