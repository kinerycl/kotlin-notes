# Manacher's Algorithm 🔄

Manacher's Algorithm is an efficient algorithm to find the longest palindromic substring in a string with a time complexity of **O(n)**, where `n` is the length of the string. It processes the string in linear time, making it much faster than the brute-force approach.

## Key Concepts
- **Palindrome**: A string that reads the same forwards and backwards (e.g., "madam").
- **Transformed String**: The algorithm first transforms the string by inserting a special separator (e.g., `#`) between each character, which ensures that both even and odd-length palindromes are handled uniformly.
  
  Example transformation:
  - Original: `"aba"`
  - Transformed: `"#a#b#a#"`

- **Center and Right Boundary**: The algorithm tracks the center and rightmost boundary of the current longest palindrome.
- **Palindrome Length Array**: An array `P[i]` holds the length of the palindrome centered at position `i`.

## Algorithm Steps
1. **Preprocess the string** by inserting a separator (e.g., `#`) between every character and around the string.
2. **Iterate through the string**:
   - Use a mirror of the current index `i` around the current center.
   - Expand the palindrome around the current index, if possible.
   - Update the `center` and `right` boundary whenever a new palindrome extends beyond the current right boundary.
3. **Track the longest palindrome** and its length as you iterate.

## Example in Kotlin
```kotlin
fun manacher(s: String): String {
    // Transform the string by adding separators
    val transformed = "#${s.map { "$it#" }.joinToString("")}"
    val n = transformed.length
    val p = IntArray(n)
    var center = 0
    var right = 0
    var maxLength = 0
    var maxCenter = 0

    for (i in 0 until n) {
        val mirror = 2 * center - i
        if (i < right) p[i] = minOf(right - i, p[mirror])

        var left = i - (p[i] + 1)
        var rightIndex = i + (p[i] + 1)
        while (left >= 0 && rightIndex < n && transformed[left] == transformed[rightIndex]) {
            p[i]++
            left--
            rightIndex++
        }

        if (i + p[i] > right) {
            center = i
            right = i + p[i]
        }

        if (p[i] > maxLength) {
            maxLength = p[i]
            maxCenter = i
        }
    }

    val start = (maxCenter - maxLength) / 2
    return s.substring(start, start + maxLength)
}

val input = "babad"
println(manacher(input)) // Output: "bab"