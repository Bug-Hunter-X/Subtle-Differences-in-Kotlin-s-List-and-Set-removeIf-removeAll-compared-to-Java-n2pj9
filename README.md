# Kotlin's removeIf/removeAll Subtleties

This repository demonstrates a subtle difference in behavior between Kotlin's `MutableList.removeIf`, `MutableList.removeAll`, `MutableSet.removeIf`, and `MutableSet.removeAll` methods when compared to their Java counterparts. While seemingly similar, these functions can produce unexpected results if not handled carefully. The key difference lies in how they handle concurrent modification exceptions.

## The Bug

The code in `Bug.kt` showcases the unexpected behavior using `MutableList` and `MutableSet`.  The methods `removeIf` and `removeAll` function as expected, removing even numbers from the collection. However, a direct comparison to Java's similar methods would reveal different results in more complex scenarios involving multiple threads or external modifications. 

## The Solution

The `BugSolution.kt` file doesn't offer a direct solution because the behavior is not a bug, but rather a design choice in Kotlin. It simply highlights the behavior to make developers aware of the differences between the two languages.