- # Bitwise Operators and Binary Math in Kotlin ⚙️

Kotlin supports bitwise operations on integer types, allowing you to manipulate data at the bit level. These operations are essential for tasks like low-level data processing and optimization.

## Bitwise Operators 🛠️

- **AND (`&`)**: Performs a bitwise AND operation between two operands. 
  - Example: `a & b` — Only sets a bit if both bits are `1`.
  - ```kotlin
    val result = 5 & 3  // result is 1 (binary 0101 & 0011 = 0001)
    ```

- **OR (`|`)**: Performs a bitwise OR operation between two operands.
  - Example: `a | b` — Sets a bit if either of the bits is `1`.
  - ```kotlin
    val result = 5 | 3  // result is 7 (binary 0101 | 0011 = 0111)
    ```

- **XOR (`^`)**: Performs a bitwise XOR operation between two operands.
  - Example: `a ^ b` — Sets a bit if only one of the bits is `1` (but not both).
  - ```kotlin
    val result = 5 ^ 3  // result is 6 (binary 0101 ^ 0011 = 0110)
    ```

- **NOT (`inv`)**: Inverts all the bits of the operand.
  - Example: `a.inv()` — Flips all the bits in `a`.
  - ```kotlin
    val result = 5.inv()  // result is -6 (binary ~0101 = 1010)
    ```

## Shift Operators 🔄

- **Left Shift (`shl`)**: Shifts the bits of the operand to the left by the specified number of positions.
  - Example: `a shl n` — Shifts the bits of `a` left by `n` positions, adding `0` bits on the right.
  - ```kotlin
    val result = 5 shl 1  // result is 10 (binary 0101 << 1 = 1010)
    ```

- **Right Shift (`shr`)**: Shifts the bits of the operand to the right by the specified number of positions.
  - Example: `a shr n` — Shifts the bits of `a` right by `n` positions, adding `0` bits on the left.
  - ```kotlin
    val result = 10 shr 1  // result is 5 (binary 1010 >> 1 = 0101)
    ```

- **Unsigned Right Shift (`ushr`)**: Shifts the bits to the right, without preserving the sign bit (used for unsigned integers).
  - Example: `a ushr n` — Shifts the bits of `a` right by `n` positions, inserting `0` bits on the left.
  - ```kotlin
    val result = -10 ushr 1  // result is a large positive value (binary of -10 shifted right)
    ```

## Binary Math 🧮

- **Binary Literal (`0b`)**: Kotlin supports binary literals, allowing you to write numbers directly in binary form.
  - Example: `0b1101` represents the binary number `1101`, which is `13` in decimal.
  - ```kotlin
    val num = 0b1101  // num is 13 in decimal
    ```

- **Convert to Binary (`toString(2)`)**: Converts an integer to its binary string representation.
  - Example: `a.toString(2)` — Converts the integer `a` to its binary string form.
  - ```kotlin
    val binaryString = 5.toString(2)  // binaryString is "101"
    ```

- **Convert to Integer (`toInt()`)**: Converts a binary string back to an integer.
  - Example: `"101".toInt(2)` — Converts the binary string `"101"` to the integer `5`.
  - ```kotlin
    val number = "101".toInt(2)  // number is 5
    ```

## Common Binary Operations 🧑‍💻

- **Binary Exponentiation**: Efficient algorithm to compute large powers of numbers by breaking the power into smaller parts and using bit shifts.
  - Example: Compute `x^n` using binary exponentiation.
  - ```kotlin
    fun binaryExponentiation(x: Int, n: Int): Int {
        var result = 1
        var base = x
        var exponent = n
        while (exponent > 0) {
            if (exponent % 2 == 1) {
                result *= base
            }
            base *= base
            exponent /= 2
        }
        return result
    }
    ```

## Constants and Values 🔢

- **Zero Constant (`0L`)**: Represents zero as a long integer type.
  - Example: `0L` is a `Long` value with a value of `0`.
  - ```kotlin
    val zeroLong = 0L  // zeroLong is of type Long
    ```

- **Check If a Bit Is Set (`bitAnd`)**: To check if a specific bit is set, use the `and` operator.
  - Example: Check if the second bit is set.
  - ```kotlin
    val isBitSet = (num and (1 shl 1)) != 0  // Check if the second bit is set
    ```

## Tips 📝

- Use **bitwise operators** for performance optimization, especially in areas like encryption, compression, and low-level data manipulation.
- **Shifting bits** can be used to multiply or divide numbers by powers of two quickly.