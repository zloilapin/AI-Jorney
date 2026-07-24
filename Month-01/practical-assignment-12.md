# Practical Assignment: Day 12

## 🎯 Task Description
Assemble a fully autonomous observation script that combines loops, conditional cost-saving logic, API request handling, and error protection into a single, cohesive architecture.

## 🛠️ My Solution
```python
import time
import requests

while True:
    is_my_turn = True 
    
    if is_my_turn:
        try:
            response = requests.get("[https://api.openai.com/v1/models](https://api.openai.com/v1/models)")
            print("API Success: Data received.")
        except:
            print("Network Error: Safe fallback triggered.")
    else:
        print("Standby: Conserving resources.")
        
    time.sleep(3)
