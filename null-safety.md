# Null Safety Operators ⚠️

- `?` — Nullable type (e.g., `String?` means the variable can hold a string or null) 💭
  - Example:
    ```kotlin
    val name: String? = null  // This can hold either a string or null
    ```

- `!!` — Assert that the value is not null (throws an exception if it is) 🚨
  - Example:
    ```kotlin
    val length = name!!.length  // Throws NullPointerException if 'name' is null
    ```

- `?:` — Elvis operator, provides a default value if the left-hand side is null 😅
  - Example:
    ```kotlin
    val length = name?.length ?: 0  // If 'name' is null, default to 0
    ```

# Higher-Order Functions 🔧

- `.let { }` — Apply operations on an object, often used to handle null values 💡
  - Example:
    ```kotlin
    val name: String? = "Kotlin"
    name?.let {
        println("The name length is: ${it.length}")
    }
    ```