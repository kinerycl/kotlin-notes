# Strings 🧵

## String Properties and Functions 🔠
- `.length` / `.size` / `.indices` — Length and indices for iteration 🔢
  - Example:
    ```kotlin
    val str = "Kotlin"
    println(str.length)  // Output: 6
    ```

- `S.toCharArray().sorted().joinToString("")` — Sort characters in a string 🔡
  - Example:
    ```kotlin
    val sorted = "Kotlin".toCharArray().sorted().joinToString("")
    println(sorted)  // Output: Kilnot
    ```

- `.substring(start, end)` — Extract part of a string ✂️
  - Example:
    ```kotlin
    val str = "Kotlin"
    val sub = str.substring(1, 4)  // Output: "otl"
    ```

## Character Checks 🔍
- `.isDigit()` — Check if a character is a digit 🔢
  - Example:
    ```kotlin
    println('5'.isDigit())  // Output: true
    println('a'.isDigit())  // Output: false
    ```

- `.isLetter()` — Check if a character is a letter 🔤
  - Example:
    ```kotlin
    println('a'.isLetter())  // Output: true
    println('1'.isLetter())  // Output: false
    ```

- `.isLetterOrDigit()` — Check if a character is a letter or digit 🔠🔢
  - Example:
    ```kotlin
    println('a'.isLetterOrDigit())  // Output: true
    println('%'.isLetterOrDigit())  // Output: false
    ```

## Character Transformations 🔄
- `.uppercase()` — Convert a string to uppercase 🔠
  - Example:
    ```kotlin
    val upper = "kotlin".uppercase()
    println(upper)  // Output: KOTLIN
    ```

- `.lowercase()` — Convert a string to lowercase 🔡
  - Example:
    ```kotlin
    val lower = "KOTLIN".lowercase()
    println(lower)  // Output: kotlin
    ```

## Conversions 🔄
- `digitToInt()` — Convert a digit character to an integer 🔢
  - Example:
    ```kotlin
    val digit = '5'.digitToInt()  // Output: 5
    ```

- `1 - '0' = 1` — Convert character `'1'` to integer 1 🔠➡️🔢
  - Example:
    ```kotlin
    val num = '1' - '0'  // Output: 1
    ```