# Kotlin Collection Types

In Kotlin, collection types are used to store and manage groups of objects. These types can be classified as mutable or immutable based on whether you can modify their contents. This document provides an overview of common Kotlin collection types, including lists, sets, and maps, as well as how they differ in terms of mutability and operations.

## Collection Types Overview

| Collection Type    | Mutable (Resize/Modify) | Modify Elements | Resize (Add/Remove) | Example                |
|--------------------|-------------------------|-----------------|---------------------|------------------------|
| **MutableList**     | ✅                      | ✅               | ✅                   | `mutableListOf(1,2)`   |
| **List (Read-Only)**| ❌                      | ❌               | ❌                   | `listOf(1,2)`          |
| **MutableSet**      | ✅                      | ❌               | ✅                   | `mutableSetOf(1,2)`    |
| **Set (Read-Only)** | ❌                      | ❌               | ❌                   | `setOf(1,2)`           |
| **MutableMap**      | ✅                      | ✅               | ✅                   | `mutableMapOf(1 to "A")` |
| **Map (Read-Only)** | ❌                      | ❌               | ❌                   | `mapOf(1 to "A")`      |
| **Pair**            | ❌                      | ❌               | ❌                   | `"apple" to "fruit"`    |

## Common Operations

- **Add**: Adding elements to the collection (e.g., `add()`, `put()`).
- **Remove**: Removing elements from the collection (e.g., `remove()`, `removeAt()`).
- **Modify**: Modifying elements in the collection (e.g., `set()` in mutable lists).
- **Transform**: Transforming elements in the collection.
  - **`map()`**: Transforms a collection by applying a transformation function to each element.
      ```kotlin
      val numbers = listOf(1, 2, 3)
      val squaredNumbers = numbers.map { it * it } // [1, 4, 9]
      ```
  - **`mapIndexed()`**: Similar to `map()`, but also provides the index of each element along with the element itself.
      ```kotlin
      val numbers = listOf(10, 20, 30)
      val indexedNumbers = numbers.mapIndexed { index, value -> "$index: $value" }
      println(indexedNumbers) // ["0: 10", "1: 20", "2: 30"]
      ```

These operations are available for mutable collections like `MutableList`, `MutableSet`, and `MutableMap`, but not for immutable collections like `List`, `Set`, and `Map`.


These operations are available for mutable collections like `MutableList`, `MutableSet`, and `MutableMap`, but not for immutable collections like `List`, `Set`, and `Map`.

## Sorting Collections

Kotlin provides several ways to sort collections:

- **`sorted()`**: Returns a new list sorted in ascending order.
    ```kotlin
    val numbers = listOf(5, 3, 8, 1)
    val sortedNumbers = numbers.sorted() // [1, 3, 5, 8]
    ```

- **`sortedDescending()`**: Returns a new list sorted in descending order.
    ```kotlin
    val numbers = listOf(5, 3, 8, 1)
    val sortedNumbersDesc = numbers.sortedDescending() // [8, 5, 3, 1]
    ```

- **`sortedBy()`**: Sorts by a custom condition (e.g., by length of strings).
    ```kotlin
    val words = listOf("apple", "banana", "kiwi")
    val sortedByLength = words.sortedBy { it.length } // [kiwi, apple, banana]
    ```

- **`sortedByDescending()`**: Sorts by a custom condition in descending order.
    ```kotlin
    val words = listOf("apple", "banana", "kiwi")
    val sortedByLengthDesc = words.sortedByDescending { it.length } // [banana, apple, kiwi]
    ```

- **`sort()`**: Sorts a mutable list in place.
    ```kotlin
    val numbers = mutableListOf(5, 3, 8, 1)
    numbers.sort() // [1, 3, 5, 8]
    ```

- **`sortDescending()`**: Sorts a mutable list in place in descending order.
    ```kotlin
    val numbers = mutableListOf(5, 3, 8, 1)
    numbers.sortDescending() // [8, 5, 3, 1]
    ```

## Conclusion

Kotlin’s collection types provide powerful tools for working with groups of data. By understanding the differences between mutable and immutable collections, you can choose the right type for your application. In future notes, we will explore how collections interact with functional programming concepts such as filtering, mapping, and reducing.