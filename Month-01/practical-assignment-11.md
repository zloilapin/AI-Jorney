# Practical Assignment: Day 11

## 🎯 Task Description
Build a complex logic gate for a DeFi automation script. The script must evaluate two independent variables (token reward balance and network gas fee) and execute a claim only if both optimal conditions are met simultaneously.

## 🛠️ My Solution
```python
# 1. Defining the environmental variables
reward = 60
gas = 15

# 2. Complex logic evaluation using 'and'
if reward > 50 and gas < 20:
    # Executes only if BOTH conditions are True
    print("Условия супер, делаю клейм")
else:
    # Executes if ANY of the conditions fail
    print("Ждём лучшие условия")
