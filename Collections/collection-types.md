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

## Collection Operations

- **Add**: Adding elements to the collection (e.g., `add()`, `put()`).
- **Remove**: Removing elements from the collection (e.g., `remove()`, `removeAt()`).
- **Modify**: Modifying elements in the collection (e.g., `set()` in mutable lists).

These operations are available for mutable collections like `MutableList`, `MutableSet`, and `MutableMap`, but not for immutable collections like `List`, `Set`, and `Map`.

## Conclusion

Kotlin’s collection types provide powerful tools for working with groups of data. By understanding the differences between mutable and immutable collections, you can choose the right type for your application. In future notes, we will explore how collections interact with functional programming concepts such as filtering, mapping, and reducing.