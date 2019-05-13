---
layout: post
title: David Edwards / Blog
topic: Understanding Elusive Aspects of the Scala Type System
date: 2013-05-09
---
During the course of studying the inner workings of the [Spray DSL](http://spray.io), I stumbled upon a feature in the Scala type system that seemed to evade comprehension.

Here is the snippet of code from the source. Pay special attention to the method signature.

```scala
def complete: (=> CompletionMagnet) => StandardRoute = magnet => new StandardRoute {
  def apply(ctx: RequestContext) {
    magnet.route(ctx)
  }
}
```

I believe this could have been simplified and written as follows. Doing so helps clarify my point.

```scala
def complete(magnet: => CompletionMagnet): StandardRoute = new StandardRoute...
```

As we know, `magnet` represents a by-name function parameter, which means the function is not evaluated until referenced. This is useful in cases where a block of code must be provided by the caller, but the execution of that block is done by the callee. A by-name function parameter is easily detected by the absence of a parameter list in the type.

A by-name function parameter would look like this.

```scala
def foo(fn: => Int)
```

Whereas, in contrast, a by-value function parameter would be written as follows.

```scala
def foo(fn: () => Int)
```

Notice the subtle difference in notation. Using the by-name variant, foo is invoked with an arbitrary block of code whose value must be Int. These are all valid invocations.

```scala
foo { 1 }

foo(1)

foo {
  println("hello")
  1
}
```

In all cases, the block of code is NOT evaluated until the function `foo` references `fn`. If you had instead defined `foo` as follows.

```scala
def foo(n: Int)
```

Then, each of the invocations above would still compile, but their corresponding block of code would be evaluated prior to calling `foo`.

Using the by-value variant of `foo`, above, note the difference in invocation.

```scala
foo { () => 1 }

foo { () =>
  println("hello")
  1
}
```

In this case, even though we are passing the function by-value, the statements in the block are not evaluated. The reason is that the type of the block is `() => Int`, which is read as a "function with no parameters returning an `Int`".

Try entering the following expressions in the Scala REPL and you’ll better understand the distinction.

```scala
scala> { 1 }
res0: Int = 1

scala> { () => 1 }
res1: () => Int = <function0>
```

The first example is a block that evaluates to an `Int`, whereas the second is a block that evaluates to a "function returning an `Int`".

Anyhow, back to my original reason for this post. In a Spray application, you might use the `complete` method in the following way.

```scala
complete {
  <html>
    <body>
      <h1>Hello</h1>
    </body>
  </html>
}
```

The type of this user-defined block of code, when evaluated, is `scala.xml.NodeSeq`, not `CompletionMagnet`, which is specified in the definition of `complete`. As one would expect, there is an implicit method in scope that converts any object into an instance of `CompletionMagnet`, making it suitable for calling `complete`. Otherwise, the compiler would yell. But, the value being implicitly converted is a by-name function that has yet to be evaluated. It turns out this is okay, because the compiler knows the value of the block, and hence, can search for a suitable implicit to perform the conversion. You just have to ensure the block is not evaluated (referenced) prematurely, which is the case with `complete`–`magnet` is not referenced until the `apply` method is called on the anonymous instance of `StandardRoute`.

Part of the difficulty in understanding the Scala type system is the language syntax and the heavy use of implicits that are often necessary when building a DSL. My suggestion is to study these libraries and DSLs in greater detail, which will give you a much better appreciation of how things work.
