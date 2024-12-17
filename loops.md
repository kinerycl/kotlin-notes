# Loops and Iteration 🔁

## Looping Techniques 🔄
- `.indices` — Iterate over indices of a list or string 📜.
  - Example:
    ```kotlin
    val list = listOf(1, 2, 3)
    for (i in list.indices) {
        println("Index: $i, Value: ${list[i]}")
    }
    ```

- `downTo` — Count down from one number to another ⬇️.
  - Example:
    ```kotlin
    for (i in 10 downTo 1) {
        println(i)
    }
    ```

- `until` — Loop up to, but not including, a specific value ➖.
  - Example:
    ```kotlin
    for (i in 0 until 5) {
        println(i)
    }
    ```

## Special Techniques ✨
- **Swap** — Swap two elements in a list or array 🔄💡.
  - Example:
    ```kotlin
    val nums = mutableListOf(1, 2, 3, 4)
    val k = 0
    val j = 3
    nums[k] = nums[j].also { nums[j] = nums[k] }
    println(nums)  // Output: [4, 2, 3, 1]
    ```

- **Multiplication Trick** — Calculate the index of a result array when combining two numbers ✖️➗.
  - Example:
    ```kotlin
    val i = 2
    val j = 3
    val index = (i + j + 1)
    println("Index: $index")
    ```