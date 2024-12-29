# Numbers and Math ➗

## Integer Properties 🔢
- `Int.MAX_VALUE` — Maximum value of an `Int` 🌐
  - Example:
    ```kotlin
    println(Int.MAX_VALUE)  // Output: 2147483647
    ```

- `Int.MIN_VALUE` — Minimum value of an `Int` 🏔️
  - Example:
    ```kotlin
    println(Int.MIN_VALUE)  // Output: -2147483648
    ```

## Math Functions ➕➖
- `Math.pow(10.0, exponent)` — Power function 📊
  - Example:
    ```kotlin
    val result = Math.pow(10.0, 2.0)  // Output: 100.0
    ```
- **`abs()`**: Returns the absolute value of a number.
  - Example:
    ```kotlin
    val number = -42
    println(abs(number)) // 42
    ```

- `maxOf(x, y)` — Maximum of two values 🔝
  - Example:
    ```kotlin
    val max = maxOf(5, 10)  // Output: 10
    ```

- `minOf(x, y)` — Minimum of two values 🔻
  - Example:
    ```kotlin
    val min = minOf(5, 10)  // Output: 5
    ```

- `.coerceAtMost(y)` — Returns the smaller of two values (similar to `minOf(x, y`) 🌱
  - Example:
    ```kotlin
    val result = 5.coerceAtMost(10)  // Output: 5
    ```

## Difference Between `i++` and `i += 1`
- **`i++` (Post-Increment)**: Increments `i` by 1, but returns the original value before incrementing.
  - Example:
    ```kotlin
    var i = 5
    println(i++) // Prints 5, then i is incremented to 6
    println(i)    // Prints 6
    ```

- **`i += 1`**: Directly increments `i` by 1 and updates the value.
  - Example:
    ```kotlin
    var i = 5
    println(i += 1) // Prints 6, i is incremented directly
    println(i)      // Prints 6
    ```

## Conversions 🔄
- `.toIntOrNull()` — Safely convert a string to an `Int` (returns null if conversion fails) 🛑
  - Example:
    ```kotlin
    val number = "123".toIntOrNull()  // Output: 123
    val invalid = "abc".toIntOrNull()  // Output: null
    ```

- `.split(".")` — Split a string into parts using a delimiter 🧩
  - Example:
    ```kotlin
    val parts = "apple.orange.banana".split(".")
    println(parts)  // Output: [apple, orange, banana]
    ```

- `.toLong()`  —  Converts a number to a Long
  - Example:
    ```kotlin
      val number = 42
      val longNumber = number.toLong() // 42L
    ```
