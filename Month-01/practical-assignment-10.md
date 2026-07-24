# Practical Assignment: Day 10

## 🎯 Task Description
Implement a cost-saving logic gate using Boolean values. The script must simulate a local sensor that checks if it is the player's turn (`is_my_turn = False`) before executing hypothetical resource-intensive data analysis.

## 🛠️ My Solution
```python
# 1. Local sensor data (Boolean flag)
is_my_turn = False

# 2. Inverted logic evaluation
if is_my_turn == False:
    # Triggers when it's the opponent's turn (Saves resources)
    print("Ход оппонента, жду")
else:
    # Triggers when action is required
    print("Мой ход, анализирую шансы")
