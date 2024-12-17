# Sorting 🔢

## `.sort()` — Sort elements in a list 📊
- Example:
  ```kotlin
  val numbers = mutableListOf(5, 3, 8, 1)
  numbers.sort()
  println(numbers)  // Output: [1, 3, 5, 8]

  # Sorting Algorithms 🔀
- **Merge Sort** — Divide and conquer algorithm that splits the list into halves, sorts them, and merges them back together 🧩
- **Quick Sort** — Partitions the list into two smaller sub-lists and recursively sorts them 🔪
- **Bubble Sort** — Repeatedly steps through the list, compares adjacent elements, and swaps them if they’re in the wrong order 🫧

## Time Complexity ⏱️
- **Sorting time complexity** — Commonly **O(n log n)** 🔄
  - This is the time complexity for efficient sorting algorithms like Merge Sort and Quick Sort.
- **O(N!)** — Used in problems like permutations and recursion-heavy backtracking problems 😱
  - Example: When generating all possible permutations of a set, the number of operations grows exponentially as **N!**.