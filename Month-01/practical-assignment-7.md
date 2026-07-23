# Practical Assignment: Day 07

## 🎯 Task Description
Write an autonomous loop script that mimics a poker tracker waiting for a new hand to start. The script must utilize an infinite loop, correct indentation, and a controlled 5-second delay to optimize system resources.

## 🛠️ My Solution
```python
import time

while True:
    print("ожидание новой раздачи...")
    time.sleep(5)
