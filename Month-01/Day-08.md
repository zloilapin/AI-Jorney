# Day 08: Logic and Decision Making (If/Else)

## 📖 Theory: Conditionals in Python
Automation requires scripts to make decisions based on the current state of data. Python uses the `if` and `else` statements to create logic branches. 
The script evaluates a condition (e.g., is a number greater than zero?), and if the statement evaluates to `True`, it executes a specific block of code. If `False`, it falls back to the `else` block.

## 🧱 Theory: Scope in Conditionals
Just like loops, conditionals rely strictly on indentation (4 spaces) to define which code belongs to which branch.
1. `if condition:` opens the primary branch.
2. `else:` (always on the same indentation level as `if`) opens the fallback branch.
3. Code indented under these statements is executed only when the specific branch is triggered.

## ⚠️ Key Rule: Case Sensitivity
Python is strictly case-sensitive. Variables named `Balance` and `balance` are treated as completely independent entities. Mismatches in casing will result in a `NameError`.
