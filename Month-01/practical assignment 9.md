# Practical Assignment: Day 9

## 🎯 Task Description
Develop the core architecture for a continuous monitoring agent. The script must combine an infinite loop with an `if/else` logic gate, utilizing proper nested indentation (8 spaces) and simulated data injection.

## 🛠️ My Solution
```python
import time

# 1. Start the infinite monitoring engine
while True:
    print("Чекаю стол...")
    
    # Simulated data injection (Mocking)
    pot = 0 
    
    # 2. Decision making logic (4 spaces)
    if pot > 0:
        # Action block (8 spaces)
        print("Отправляем картинку в API")
    else:
        # Fallback logic (4 spaces)
        print("Стол пуст, ждём")
        
    # 3. Resource management (4 spaces)
    time.sleep(5)
    
