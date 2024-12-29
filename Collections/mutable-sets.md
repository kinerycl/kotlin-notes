# Mutable Sets in Kotlin

A **Mutable Set** in Kotlin is a collection that holds unique elements and allows modification (adding/removing elements).

## Key Operations

- **`mutableSetOf()`**: Creates a mutable set.
    ```kotlin
    val set = mutableSetOf(1, 2, 3)
    ```

- **`add()`**: Adds an element to the set.
    ```kotlin
    val set = mutableSetOf(1, 2)
    set.add(3)  // set = [1, 2, 3]
    ```

- **`remove()`**: Removes an element from the set.
    ```kotlin
    val set = mutableSetOf(1, 2, 3)
    set.remove(2)  // set = [1, 3]
    ```

- **`clear()`**: Removes all elements from the set.
    ```kotlin
    val set = mutableSetOf(1, 2, 3)
    set.clear()  // set = []
    ```

- **`contains()`**: Checks if an element exists in the set.
    ```kotlin
    val set = mutableSetOf(1, 2, 3)
    val containsThree = set.contains(3)  // true
    ```

- **`size`**: Returns the size of the set.
    ```kotlin
    val set = mutableSetOf(1, 2, 3)
    val size = set.size  // 3
    ```

## Example

```kotlin
fun main() {
    val numbers = mutableSetOf(1, 2, 3)
    
    numbers.add(4)  // Adds 4 to the set
    numbers.remove(2)  // Removes 2 from the set
    
    println(numbers)  // Output: [1, 3, 4]
}
```

## `.toMutableSet()`

- **`toMutableSet()`**: Converts an immutable set or a list to a mutable set, allowing modification of elements.

    ### From an Immutable Set:
    ```kotlin
    val immutableSet = setOf(1, 2, 3)
    val mutableSet = immutableSet.toMutableSet() // Mutable set: [1, 2, 3]
    mutableSet.add(4) // Mutable set after adding element: [1, 2, 3, 4]
    ```

    ### From a List:
    ```kotlin
    val list = listOf(1, 2, 3)
    val mutableSet = list.toSet().toMutableSet() // Converts list to mutable set: [1, 2, 3]
    mutableSet.add(4) // Mutable set after adding element: [1, 2, 3, 4]
    ```

## Differences from Immutable Set

- **Mutable Set**: Allows adding/removing elements after creation.
- **Immutable Set**: The set is fixed, and you cannot modify its contents after initialization.

## Conclusion

Mutable sets are useful when you need a collection that doesn’t allow duplicates and can be modified after creation.