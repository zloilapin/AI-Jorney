# Day 13: Complex Architecture & Nested Logic

## 📖 Theory: Deep Nesting in Python
Building a production-ready automation script requires combining multiple logic gates within an infinite loop. This creates "deep nesting," where code indentation can reach 12 or 16 spaces.

1. **Level 1 (0 spaces):** The core loop initialization (`while True:`).
2. **Level 2 (4 spaces):** Primary environment checks (e.g., verifying if a system is online).
3. **Level 3 (8 spaces):** Secondary condition evaluations combining logical operators (`and` / `or`).
4. **Level 4 (12+ spaces):** Execution blocks and safety nets (`try/except`) for external API interactions.

## 🧱 Theory: Matching `if` and `else`
In deeply nested structures, an `else` statement is strictly bound to the `if` statement that shares its exact indentation level. Misaligning an `else` block by even one space changes the entire logic of the script and can cause fatal execution errors.
