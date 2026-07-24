# Day 9: Nested Scope (Loops + Conditionals)

## 📖 Theory: Combining Core Mechanics
To build truly autonomous AI agents, we must combine the infinite execution engine (`while True`) with the decision-making brain (`if/else`). This allows the script to continuously monitor an environment and react dynamically to changes without human intervention.

## 🧱 Theory: Double Indentation (Nested Scope)
When placing conditional logic inside a loop, Python requires nested indentation.
1. The `while True:` statement opens the main loop.
2. The code inside the loop is indented by **4 spaces**.
3. When writing an `if/else` statement inside the loop, the condition itself sits at the 4-space level.
4. The execution blocks *inside* the `if` and `else` statements require an additional 4 spaces, totaling **8 spaces** of indentation. This creates a nested hierarchy that Python uses to understand execution order.

## 🧠 Best Practices: Mocking Data
Before connecting complex external APIs, engineers use placeholder variables (mock data, e.g., `pot = 0`) to safely test the structural integrity and logic flow of the loop and conditional statements.
