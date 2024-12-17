# Tail Recursion 🔁

- **Tail Recursion** — A recursion where the last statement is the recursive call 🌀
  - Example:
    ```kotlin
    tailrec fun factorial(n: Int, acc: Int = 1): Int {
        return if (n == 0) acc else factorial(n - 1, n * acc)
    }
    ```

- **Optimizable by Kotlin** — Kotlin can optimize tail recursion to prevent stack overflow 🚀
  - Kotlin automatically optimizes tail-recursive functions by converting them into a loop to avoid stack overflow errors, making it more efficient for deep recursion.