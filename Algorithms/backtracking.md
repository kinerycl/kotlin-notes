# Backtracking 🔄

## Recursive Backtracking 🔍
- **Explore potential solutions** — Try different possibilities in a step-by-step approach 🔄
  - Example: Trying out different combinations or paths in a puzzle or problem-solving scenario.

- **Undo last step to try a different path (backtrack)** — When a solution path doesn’t work, backtrack to the previous decision point and try a new path ↩️
  - Example: When generating all permutations, if a solution doesn’t lead to a valid result, undo the last choice and try another option.

- **Example** — Solving permutations or combinations 🔢
  - Example: Generating all permutations of a string involves trying each character in every possible position, backtracking when necessary.

- **“Pruning”** — Eliminate branches of the solution tree early to optimize 🪓
  - Example: If a certain path is already proven to be unproductive, it’s “pruned” to save time by not exploring it further.