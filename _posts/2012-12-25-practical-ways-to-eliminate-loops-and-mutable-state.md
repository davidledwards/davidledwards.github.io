---
layout: post
title: Blog
topic: Practical Ways to Eliminate Loops and Mutable State in Scala Programs
date: 2012-12-25
---
<div class="content" markdown="1">
I recently [published](https://davidedwards.io/2012/12/17/a-scala-api-and-cli-for-zookeeper) the source code for a side project I started with the primary objective of becoming more proficient in the [Scala](https://www.scala-lang.org) programming language, though perhaps the more compelling reason was a growing interest in functional approaches to program design.

I must confess that nowadays I spend a very small fraction of my professional life ensconced in writing code, but as a technology executive, I’ve always been of the firm opinion that maintaining some level of currency on modern topics only enhances your ability to manage your organization and make smarter decisions.

An interesting property of both the API and CLI portion of this [project](https://github.com/davidledwards/zookeeper) is that, with one minor exception in the CLI, the entire program is purely functional. If your background is etched with an imperative style of programming, one of the most significant practical challenges is dispensing with the use of looping constructs, such as while loops. So, I thought I would share a couple of practical techniques for eliminating their use.

The following is a contrived example from the CLI that processes an indefinite command loop, which executes the given steps:

1. initializes the context to “/”
2. reads a command and its arguments
3. invokes the command function with the arguments and the context, returning a new context
4. exits the loop if the context is null
5. otherwise, jumps to step 2

Here are the parts of the processing loop that we don’t particularly care about, but including them for sake of completeness. Notice that the `quit` function returns a `null` context, which ends the processing loop.

```scala
object CLI {
  type Command = (Seq[String], String) => String

  val commands = Map[String, Command](
    "cd" -> cd _,
    "quit" -> quit _
  )

  def main(args: Array[String]) {
    process()
  }

  def process(): Unit = ???

  def cd(args: Seq[String], context: String): String = {
    println("new directory is "	+ args.head)
    args.head
  }

  def quit(args: Seq[String], context: String): String = {
    println("goodbye")
    null
  }

  def read(): (String, Seq[String]) = ???
}
```

The first form of the processing loop is an imperative style that uses a while construct with mutable state, which should look pretty familiar to most of us.

```scala
def process() {
  var context = "/"
  while (context != null) {
    val (cmd, args) = read()
    context = commands(cmd)(args, context)
  }
}
```

A simple technique for eliminating this mutable state is to convert the while loop into a tail-recursive function. Annotating the function with `@tailrec` allows the optimizer to convert the recursive function into a loop, thus avoiding the potential for stack exhaustion. This is particularly important for the class of recursive functions, such as the following, whose terminating condition may theoretically never happen.

```scala
def process() {
  @tailrec def process(context: String) {
    if (context != null) {
      val (cmd, args) = read()
      process(commands(cmd)(args, context))
    }
  }
  process("/")
}
```

Another interesting discovery was the versatile use of the `fold` functions. While developing the CLI, I ran into several scenarios where I not only needed to apply a function to elements in a sequence, but also needed to know the relative position of that element for formatting reasons.

Imagine for a moment that you need to print a list of words separated by commas. A naive implementation would print the word followed by a comma, but that would look a bit strange with a comma appended to the last word. So, you might introduce a simple index, incrementing with each word, but that introduces mutable state, which we’re trying to avoid. Here is an example:

```scala
object Print {
  def main(args: Array[String]) {
    var i = 1
    args foreach { arg =>
      print(arg)
      if (i < args.size) print(",")
      i = i + 1
    }
    println()
  }
}
```

An alternative is to apply a `fold` operation, left to right, supplying the index as the start value. Since the function applied to each element must return a value matching the type of the start value, we can let the `fold` operation manage state on our behalf. Here is the same example rewritten using `foldLeft` (`/:`):

```scala
object Print {
  def main(args: Array[String]) {
    (1 /: args) { case (i, arg) =>
      print(arg)
      if (i < args.size) print(",")
      i + 1
    }
    println()
  }
}
```
</div>
