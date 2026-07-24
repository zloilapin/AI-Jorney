# Practical Assignment: Day 16

## 🎯 Task Description
Upgrade the Synthetix bot's logging system. Implement f-strings in the `print()` statements to dynamically display the exact values of `reward` and `gas` during both successful executions and skipped cycles.

## 🛠️ Solution: Bot with Dynamic Logging

```python
import time
import requests

while True:
    
    # 1. Mock numerical data
    reward = 40
    gas = 20
    
    if reward > 50 and gas < 15:
        try:
            requests.get("[https://api.synthetix.io/pool/claim](https://api.synthetix.io/pool/claim)")
            # 2. Dynamic log for success
            print(f"Success! Claimed {reward} tokens at {gas} gwei gas.")
        except:
            print("Network Error! Server is unreachable.")
            
    else:
        # 3. Dynamic log for rejection
        print(f"Skipping. Reward is only {reward}, and gas is {gas}.")
        
    time.sleep(10)
