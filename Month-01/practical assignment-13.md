# Practical Assignment: Day 13

## 🎯 Task Description
Develop a comprehensive, continuous monitoring bot for the Synthetix DeFi protocol. The script must utilize boolean flags, compound logical operators, external API requests, and exception handling, all enclosed within an optimized infinite loop.

## 🛠️ Solution: Synthetix Pool 420 Auto-Claimer
```python
import time
import requests

# 1. Continuous execution engine
while True:
    pool_420_active = True
    
    # 2. Primary state check
    if pool_420_active:
        reward = 80
        gas = 12
        
        # 3. Compound logical evaluation
        if reward > 50 and gas < 20:
            
            # 4. Fault-tolerant execution block
            try:
                requests.get("[https://api.synthetix.io/pool420/claim](https://api.synthetix.io/pool420/claim)")
                print("Успех! Токены заклеймлены.")
            except:
                print("Ошибка сети! Сервер Synthetix недоступен.")
                
        else:
            print("Невыгодно. Копим дальше.")
            
    else:
        print("Пул на паузе, ждем...")
        
    # 5. Resource management delay
    time.sleep(10)
