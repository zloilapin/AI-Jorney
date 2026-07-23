# Day 07: Infinite Loops and Execution Scope

## 📖 Theory: The `while True` Statement
In automation, scripts need to run continuously rather than executing once and terminating. Python handles this using the `while` loop. 
The statement `while True:` creates an infinite loop because the condition `True` never evaluates to `False`. This is the core engine for any background worker, observer, or autonomous agent.

## 🧱 Theory: Scope and Indentation
Unlike other languages that use brackets `{}` to define what belongs inside a loop, Python uses strict visual indentation (Scope).
1. The colon `:` opens the loop logic.
2. Every line indented by **4 spaces** belongs inside the loop.
3. Once the indentation ends, the loop scope ends. Without proper indentation, Python throws an `IndentationError`.

## ⏱️ Theory: Controlling the Rhythm (`time.sleep`)
An unconstrained `while True` loop will execute millions of times per second, maxing out CPU usage and immediately triggering spam protections on APIs. 
To control the rhythm, engineers use the `time` module. The `time.sleep(seconds)` function tells the script to pause entirely for the specified duration before moving to the next line of code.
