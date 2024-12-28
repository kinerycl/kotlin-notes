# List vs Array ⚖️

## Mutable List
- **`mutableListOf(26) { 0 }`** — Mutable list with default values. You can change elements after creation. 📝

  **Example:**
  ```kotlin
  val mutableList = mutableListOf(26) { 0 }
  mutableList[0] = 5 // Modify the first element
  println(mutableList) // Output: [5, 0, 0, 0, 0, ..., 0]
  ```

## Integer Array
- **`IntArray(size) { default }`** — Integer array with default values. A more memory-efficient structure for storing integers. 🔢

    **Example:**
    ```kotlin
    val intArray = IntArray(5) { 0 } // Array of 5 integers, all initialized to 0
    intArray[2] = 10 // Modify the third element
    println(intArray.joinToString()) // Output: 0, 0, 10, 0, 0
    ```

## Character Array
- **`CharArray(X)`** — Character array with `X` elements, useful for handling individual characters. 🔤

    **Example:**
    ```kotlin
    val charArray = CharArray(3) { 'a' }
    charArray[1] = 'b' // Modify the second character
    println(charArray.joinToString()) // Output: a, b, a
    ```

## Boolean Array
- **`BooleanArray(size) { false }`** — Boolean array of specified size with default `false` values. ⚪

    **Example:**
    ```kotlin
    val booleanArray = BooleanArray(4) { false }
    booleanArray[2] = true // Modify the third element
    println(booleanArray.joinToString()) // Output: false, false, true, false
    ```

## 2D Array
- **`Array(rows) { IntArray(cols) { 0 } }`** — 2D array of integers. An array of arrays to represent a matrix. ➗

    **Example:**
    ```kotlin
    val matrix = Array(2) { IntArray(3) { 0 } }
    matrix[0][1] = 5 // Modify the first row, second column
    matrix[1][2] = 7 // Modify the second row, third column
    println(matrix.joinToString { it.joinToString() }) // Output: 0, 5, 0 | 0, 0, 7
    ```

## Array Copying
- **`toList()`** — Convert an array to a list.  
    **Example:**
    ```kotlin
    val array = intArrayOf(1, 2, 3)
    val list = array.toList()
    println(list) // Output: [1, 2, 3]
    ```
- **`array.copyOf()`** — Creates a shallow copy of an array.  
    ```kotlin
    val originalArray = intArrayOf(1, 2, 3)
    val copiedArray = originalArray.copyOf()
    println(copiedArray.joinToString()) // Output: 1, 2, 3
    ```
- **`array.copyOfRange(startIndex, endIndex)`** — Copy a specific range of elements from the array.  
    ```kotlin
    val originalArray = intArrayOf(1, 2, 3, 4, 5)
    val copiedRange = originalArray.copyOfRange(1, 4)
    println(copiedRange.joinToString()) // Output: 2, 3, 4
    ```
- **Deep copy of list**:  
  Use **`list.map { it.copy() }`** for deep copying a list of objects (note: this requires the objects in the list to be copyable).
    ```kotlin
    data class Person(val name: String)

    val originalList = listOf(Person("Alice"), Person("Bob"))
    val copiedList = originalList.map { it.copy() }

    println(copiedList) // Output: [Person(name=Alice), Person(name=Bob)]
    ```

## Common Array Methods
- **`toIntArray()`** — Converts a list of integers into an integer array. 
    ```kotlin
    val intList = listOf(1, 2, 3)
    val intArray = intList.toIntArray()
    println(intArray.joinToString()) // Output: 1, 2, 3
    ``` 
- **`toDoubleArray()`** — Converts a list to a double array.  
    ```kotlin
    val doubleList = listOf(1.1, 2.2, 3.3)
    val doubleArray = doubleList.toDoubleArray()
    println(doubleArray.joinToString()) // Output: 1.1, 2.2, 3.3
    ```
- **`toCharArray()`** — Converts a string to a character array. 
    ```kotlin
    val str = "Hello"
    val charArray = str.toCharArray()
    println(charArray.joinToString()) // Output: H, e, l, l, o
    ``` 

## Array Equality
- **`Array.contentEquals(otherArray)`** — Compares two arrays for equality. Returns `true` if arrays have the same size and elements.  
    ```kotlin
    val array1 = intArrayOf(1, 2, 3)
    val array2 = intArrayOf(1, 2, 3)
    println(array1.contentEquals(array2)) // Output: true
    ```
- **`Array.contentDeepEquals(otherArray)`** — Compares two arrays for equality, supports deep equality checks for nested arrays.
    ```kotlin
    val array1 = arrayOf(intArrayOf(1, 2), intArrayOf(3, 4))
    val array2 = arrayOf(intArrayOf(1, 2), intArrayOf(3, 4))
    println(array1.contentDeepEquals(array2)) // Output: true
    ```

## Differences 🆚
- **List**: Resizable, can hold any type of elements. 🔄  
- **Array**: Fixed size, more memory-efficient. 🏷️