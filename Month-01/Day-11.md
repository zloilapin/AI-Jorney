# Day 11: Complex Logic and Multiple Conditions

## 📖 Theory: Logical Operators (`and` / `or`)
Real-world automation rarely relies on a single variable. To evaluate multiple conditions simultaneously, Python uses logical operators:
*   **`and`**: Requires **ALL** connected conditions to be `True`. If even one is `False`, the entire statement evaluates to `False`. It is a strict gatekeeper.
*   **`or`**: Requires **AT LEAST ONE** condition to be `True`. It is a flexible gateway.

## 🧱 Theory: Building Protective Mechanisms
Logical operators are crucial for building protective guardrails in scripts (e.g., verifying both sufficient token balances AND low network gas fees before executing a blockchain transaction). This prevents scripts from executing actions in unfavorable environmental conditions.
