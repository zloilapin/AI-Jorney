# Day 14: Logical Operators (and / or)

## 📖 Theory: Combining Conditions
Automation scripts often need to verify multiple factors before executing an action. Logical operators allow us to join conditions together:
*   **`and`:** The code proceeds ONLY if BOTH conditions evaluate to `True`.
*   **`or`:** The code proceeds if AT LEAST ONE condition evaluates to `True`.

## 🧱 The `and` Operator Pattern
To claim staking rewards efficiently, we must ensure that the pool is active (`pool_active`) AND that network gas fees are low (`gas_low`).
Instead of writing complex nested blocks, we combine them into a single line:
`if pool_active and gas_low:`

If either variable is `False` (for example, the pool is active but gas fees are too high), Python treats the entire expression as false and routes execution to the `else` block.
