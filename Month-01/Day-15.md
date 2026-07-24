# Day 15: Comparison Operators (>, <, ==)

## 📖 Theory: Evaluating Numbers
In previous days, we used simple boolean variables (`True` or `False`) to trigger our script logic. In reality, APIs return numerical data (like the amount of rewards pending or current gas prices). To evaluate these numbers, Python uses Comparison Operators:

*   **`>` (Greater than):** Checks if the left value is larger. Example: `reward > 50`.
*   **`<` (Less than):** Checks if the left value is smaller. Example: `gas < 15`.
*   **`==` (Equal to):** Checks if two values are exactly the same. (Note: A double equals sign is used for comparison, while a single `=` is used to assign a value to a variable).
*   **`>=` / `<=`:** Greater than or equal to / Less than or equal to.

## 🧱 The Dynamic Condition Pattern
By combining logical operators (`and`) with comparison operators (`>`, `<`), we can build precise automation rules. 
For example, we only want our bot to execute a transaction if the pending reward is high enough to be profitable, AND the gas fee is cheap enough:
`if reward > 50 and gas < 15:`
