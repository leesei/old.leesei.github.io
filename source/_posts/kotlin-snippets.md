---
title: Kotlin
categories:
  - comp.lang
tags:
  - kotlin
toc: true
date: 2019-04-11 23:33:53
---

## List and Array

Use `List<T>.toTypeArray()` to get primitive Java array (`T[]`)

// range to array
// array to list

## Class

https://khan.github.io/kotlin-for-python-developers/#inheritance

Kotlin classes are closed (Java `final`) by default, use `open` modifier to allow inheritance.

`constructor` keyword can be omitted for primary constructor unless you specify access modifiers (`protected`, `internal`, etc)or annotations.

Primary constructor can use the parameters to initialize properties of the same name with default getters and setters. Note property setter is not invoked in this process. Declare variable in class, use `init{}` block and set the property manually to invoke the setter. Private property is also declared this way.
Use keyword `field` refer to the field in accessor instead of using actual property name to avoid infinite recursion.
https://khan.github.io/kotlin-for-python-developers/#setters-and-getters

Primary constructor calls the parent contractor right away by class name. So from the superclass's perspective, calling an open function in constructor is risky: it might be overridden in the subclass.
Secondary constructor calls other constructor (if available) with `this()` or parent constructor with `super()` (if none constructor available)

Subclass may refer functions and properties of superclass via `super` keyword: `super.foo()`.

Property = hidden field + default/custom accessor
Computed property without backing field can also be (declare it without initialization)
[android - What's Kotlin Backing Field For? - Stack Overflow](https://stackoverflow.com/questions/43220140/whats-kotlin-backing-field-for)

```kotlin
val isNewborn
    get() = age == 0
```

### Reflection

https://khan.github.io/kotlin-for-python-developers/#member-references-and-reflection

```kotlin
// getting class of object
// since 1.1
// https://kotlinlang.org/docs/reference/reflection.html#class-references
instance::class.qualifiedName

// obsolete style
instance.javaclass
instance.javaclass.kotlin

// getting name of variable
::instance.name
```

### Smartcast

```kotlin
if (obj is String) {  // obj: Any
  print(obj.toUpperCase())     // obj is now known to be a String
}
```

```kotlin
// extension not using contract, no smartcast
fun String?.isNotNull(): Boolean = this != null

fun foo(s: String?) {
    if (s != null) s.length // smartcast here
    if (s.isNotNull()) s.length // No smartcast :(

    if (!s.isNullOrEmpty()) {
        println("length of '$s' is ${s.length}") // Yay, smartcasted to not-null!
    }
}
```

### Delegates

```kotlin
interface View {
  fun click()
  fun toggle()
}

class ViewImpl: View {
  override fun click()  { println("click!") }
  override fun toggle() { println("toggle!") }
}

class EmptyDelegate(view: View): View by view

class OverridingDelegate(view: View): View by view {
  override fun click()  { println("CLICK!") }
}

fun main() {
   val view = ViewImpl()
   val e = EmptyDelegate(view)
   val o = OverridingDelegate(view)

   println("${e::class.qualifiedName}")
   e.click()
   e.toggle()

   println("${o::class.qualifiedName}")
   o.click()
   o.toggle()
}
```

## Label

`continue`, `break`, `this`, `return` in bound to the closest context. Use label (`name@`) to specify the context.
Function and class name are automatically generated labels.

```kotlin
outer@ for (n in 2..100) {
    for (d in 2 until n) {
        if (n % d == 0) continue@outer
    }
    println("$n is prime")
}
```

```kotlin
fun printUntilStopExplicit() {
  val list = listOf("a", "b", "stop", "c")
  list.forEach stop@ {
    if (it == "stop") return@stop
    else println(it)
  }
}

fun printUntilStopImplicit() {
  val list = listOf("a", "b", "stop", "c")
  list.forEach {
    if (it == "stop") return@forEach
    else println(it)
  }
}
```

```kotlin
class A {
  private val somefield: Int = 1
  inner class B {
    private val somefield: Int = 1
    fun foo(s: String) {
      println("Field <somefield> from B" + this.somefield)
      println("Field <somefield> from B" + this@B.somefield)
      println("Field <somefield> from A" + this@A.somefield)
    }
  }
}
```

## Range

```kotlin
class DateRange(val start: MyDate, val endInclusive: MyDate) {
    operator fun contains(item: MyDate): Boolean =
      start <= item && item <= endInclusive
}
```

[Ranges - Kotlin Programming Language](https://kotlinlang.org/docs/reference/ranges.html)

## Spread and Destructuring

Spread (`*list`) and destructuring (`(k, v) = "key" to "value"`) works as in Python and ES6

Map (dict) spreading is more tricky. The parameters have to be of the same type `vararg kwargs: Pair<String, X>` or in the worst cast `vararg kwargs: Pair<String, Any>` and it's for the function to typecast them to the correct type.

```kotlin
val numbers = listOf(1, 2, 3)
sum(*numbers.toIntArray())

foo("bar" to 42, "test" to "hello")

// destructuring example
```

## Lambda

https://khan.github.io/kotlin-for-python-developers/#receivers

```kotlin
fun buildString(action: StringBuilder.() -> Unit) : String {
  val sb = StringBuilder()
  sb.action()  // invoke the lambda as StringBuilder's extension function
  return sb.toString()
}

// inside the lambda, `this` refer to the StringBuilder object
val s = buildString {
  // this lambda has prototype `() -> Unit`
  append("Hello!")
  append("How are you?")
}
```

### Single Abstract Method (SAM)

```kotlin
//https://play.kotlinlang.org/koans/Introduction/SAM%20conversions/Task.kt

import java.util.*

fun getList(): List<Int> {
    val arrayList = arrayListOf(1, 5, 2)
    // Collections.sort(arrayList, object: Comparator<Int> {
    //     override fun compare(a:Int, b:Int) = b - a
    // })
    // use lambda SAM instead of anonymous object
    Collections.sort(arrayList, { x, y -> y - x })
    return arrayList
}
```

```kotlin
https://play.kotlinlang.org/koans/Introduction/Extensions%20on%20collections/Task.kt

fun getList(): List<Int> {
    val a = arrayListOf(1, 5, 2)
    a.sortWith(object: Comparator<Int> {
        override fun compare(x:Int, y:Int) = y - x
    })
    // lambda also works but you have to specify the
    // `Comparator` type (template type is inferred)
    a.sortWith(Comparator { x, y -> y - x })
    return a
}
```

[Why Can't Kotlin Infer The Type For Comparator - Stack Overflow](https://stackoverflow.com/questions/52292293/why-cant-kotlin-infer-the-type-for-comparator)
[SAM for Kotlin classes : KT-7770](https://youtrack.jetbrains.com/issue/KT-7770)

## Extension

Syntax:

```kotlin
fun {Class}.{name}({param}): {type} {

}
```

The class specified is the "receiver" of extension. Use `this` in the function body to refer to the receiver object instance. `this` can be omitted if there is no ambiguity, i.e.: the receiver object is the context of the code block.
https://khan.github.io/kotlin-for-python-developers/#extension-functionsproperties
https://khan.github.io/kotlin-for-python-developers/#receivers
[[Kotlin pearls 6] Extensions: The Good, The Bad and The Ugly](https://proandroiddev.com/kotlin-pearls-6-extensions-the-good-the-bad-and-the-ugly-23c88fcab235)

```kotlin
// extension function
fun Byte.toUnsigned(): Int {
    return if (this < 0) this + 256 else this.toInt()
}

// extension property
val Byte.unsigned: Int
    get() = if (this < 0) this + 256 else this.toInt()
```

## Context functions

Personally I prefer not using receiver (not using `this`).

```kotlin
maybeNull?.run { /* receiver, use `this` */ }
maybeNull?.let { /* parameter, use `it` */ }
with(expression) { /* receiver, use `this` */ }

maybeNull?.apply {
  /* receiver, use `this` */
}?.memberFunction()

maybeNull?.also {
  /* parameter, use `it` */
}?.memberFunction()
```

## DSL

[Type-Safe Builders - Kotlin Programming Language](https://kotlinlang.org/docs/reference/type-safe-builders.html)

### Tree DSL

```kotlin
class TreeNode(val name: String) {
    val children = mutableListOf<TreeNode>()

    fun node(name: String, initialize: (TreeNode.() -> Unit)? = null) {
        val child = TreeNode(name)
        children.add(child)
        if (initialize != null) {
            child.initialize()
        }
    }

    fun toString() {
      TODO()
    }
}

fun tree(name: String, initialize: (TreeNode.() -> Unit)? = null): TreeNode {
    val root = TreeNode(name)
    if (initialize != null) {
        root.initialize()
    }
    return root
}

val t = tree("root") {
    node("math") {
        node("algebra")
        node("trigonometry")
    }
    node("science") {
        node("physics")
    }
}
```
