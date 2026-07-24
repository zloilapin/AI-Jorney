# Practical Assignment: Day 15

## 🎯 Task Description
Upgrade the bot to process numerical data. Define mock variables for `reward` and `gas`. The script must use comparison operators to evaluate if the reward is greater than 50 AND the gas price is less than 15 before attempting the API request.

## 🛠️ Solution: Threshold-Based Automation

```python
import time
import requests

while True:
    
    # 1. Mock numerical data (simulating real API responses)
    reward = 80
    gas = 12
    
    # 2. Combined condition using comparison operators
    if reward > 50 and gas < 15:
        
        # 3. Protected API execution
        try:
            requests.get("[https://api.synthetix.io/pool/claim](https://api.synthetix.io/pool/claim)")
            print("Success! Claimed rewards because they are profitable.")
        except:
            print("Network Error! Server is unreachable.")
            
    else:
        # Executed if the reward is too low OR gas is too high
        print("Skipping execution. Reward is too low or gas is too expensive.")
        
    # 4. Standard delay to prevent CPU overload
    time.sleep(10)
