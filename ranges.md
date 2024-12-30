# Ranges in Kotlin 📏

In Kotlin, ranges are used to represent a sequence of values between a starting and an ending point. Ranges can be inclusive or exclusive, and you can use them to iterate over a sequence of numbers in loops or perform other operations.

## Types of Ranges 🔄

### 1. **Inclusive Range (`..`)**
   - The range created by the `..` operator is **inclusive** of both the start and end values.
   - For example, `1..5` includes `1`, `2`, `3`, `4`, and `5`.

   **Example:**
   ```kotlin
   for (i in 1..5) {
       println(i)
   }
   ```
   **Output**
   ```kotlin
    1
    2
    3
    4
    5
```

### 2. **Exclusive Range (`until`)**
   - The `until` operator creates a range that is **exclusive** of the end value.
   - For example, `1 until 5` includes `1`, `2`, `3`, and `4`, but **not** `5`.

**Example:**
   ```kotlin
for (i in 1 until 5) {
    println(i)
}
```

**Output**
   ```kotlin
    1
    2
    3
    4
    5
```

### 3. Downward Range (`downTo`)
   - The `downTo` operator allows you to create a range that counts **down** from a starting value to an ending value, **inclusive** of both values.
   
   **Example:**
   ```kotlin
   for (i in 5 downTo 1) {
       println(i)
   }
   ```

   **Output**
```kotlin
5
4
3
2
1
```

### 4. Step in Range (`step`)
   - The `step` function allows you to specify an interval or "step" for the range. It’s useful when you want to skip certain numbers in the sequence.
   
**Example:**
   ```kotlin
   for (i in 1..10 step 2) {
       println(i)
   }
   ```

**Output**
   ```kotlin
    1
    3
    5
    7
    9
   ```

## Conclusion 🏁

- Kotlin’s range operators (`..`, `until`, `downTo`, `step`) offer flexible ways to represent sequences of numbers.
- Depending on your needs, you can choose whether to use an inclusive or exclusive range, count downwards, or skip values with the `step` function.
- These range techniques are especially useful for loops and iteration.
- By understanding the differences between them, you can write more efficient and readable Kotlin code.