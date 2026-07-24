# Practical Assignment: Day 08

## 🎯 Task Description
Implement a logic gate for a crypto staking automation script. The script must check a wallet balance and print a specific command if the balance is greater than zero, or a standby message if the balance is empty.

## 🛠️ My Solution
```python
# Defined the starting condition
balance = 50

# Logic gate to determine the next action
if balance > 0:
    # Executes if condition is True
    print("отправляю в стейкинг пула")
else:
    # Executes in all other cases
    print("баланс пуст, ожидание")
