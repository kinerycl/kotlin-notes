# Dynamic Programming in Kotlin 🚀

## What is Dynamic Programming? 🧩  
Dynamic Programming (DP) is an optimization technique used to solve problems by breaking them into overlapping subproblems. The results of these subproblems are stored and reused to avoid redundant calculations.  

---

## Top-Down Dynamic Programming (Memoization) 🧠  
Top-down DP, also known as **Memoization**, is a recursive approach where we break the problem into smaller subproblems and solve them. Instead of recalculating the results for the same subproblems multiple times, we store the results in a cache (usually a dictionary or map) and reuse them. This approach is more intuitive and works well for problems where we can directly

### Example: Fibonacci Numbers  
```kotlin
val memo = mutableMapOf<Int, Int>()

fun fib(n: Int): Int {
    if (n <= 1) return n
    if (n in memo) return memo[n]!!
    memo[n] = fib(n - 1) + fib(n - 2)
    return memo[n]!!
}
```

### Key Points  
- Ideal for recursive problems with overlapping subproblems.  
- Cache results to improve time complexity.  
- Avoids recalculating results for the same inputs.

## Bottom-Up Dynamic Programming (Tabulation) ⬇️

Bottom-up DP, also known as Tabulation, solves the problem iteratively by solving all the subproblems from the smallest to the largest. Instead of using recursion, it starts from the base cases and works its way up to the final solution, storing the results of all subproblems in a table (typically an array). This method is often more efficient in terms of space and avoids the overhead of recursive function calls.

Example: Fibonacci Numbers
``` kotlin
fun fib(n: Int): Int {
    if (n <= 1) return n
    val dp = IntArray(n + 1)
    dp[0] = 0
    dp[1] = 1
    for (i in 2..n) {
        dp[i] = dp[i - 1] + dp[i - 2]
    }
    return dp[n]
}
```
### Key Points
- Builds solutions iteratively (from the smallest to the largest) rather than recursively.
- Uses a table (e.g., an array) to store results of subproblems.
- Often more memory-efficient than memoization.

## Optimized Dynamic Programming (Greedy Approach) ⚡

lthough not strictly classified as DP, the Greedy Algorithm approach can be considered a special type of DP for certain problems. Greedy algorithms make the locally optimal choice at each step with the hope that these local optimizations lead to a global optimum. It’s an approach used when we can make a choice that does not depend on previous decisions.

Characteristics
- Simple and efficient for certain problems.
- Does not always guarantee the optimal solution.

Example: Coin Change Problem
``` kotlin
fun coinChange(coins: IntArray, amount: Int): Int {
    val dp = IntArray(amount + 1) { amount + 1 }
    dp[0] = 0
    for (i in 1..amount) {
        for (coin in coins) {
            if (coin <= i) dp[i] = minOf(dp[i], dp[i - coin] + 1)
        }
    }
    return if (dp[amount] > amount) -1 else dp[amount]
}
```
### Key Points
- Greedy algorithms are often faster and simpler.
- Can be optimal for problems like coin change (when greedy works).
- Does not guarantee the optimal solution for all problems.

## Key Types of Dynamic Programming 📚
- **Top-Down DP (Memoization)**: Recursive, stores results in a cache.
- **Bottom-Up DP (Tabulation)**: Iterative, builds solutions from the smallest subproblem.
- **Greedy Algorithms**: Local optimization choice; not always optimal but efficient for specific problems.
- **Space Optimized DP**: Reduces memory usage while solving DP problems.
- **Linear DP**: Solves problems with a sequence of subproblems based on previous ones.
- **Divide and Conquer**: Divides the problem into independent subproblems and combines results.

