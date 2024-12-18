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