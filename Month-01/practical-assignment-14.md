# Practical Assignment: Day 14

## 🎯 Task Description
Enhance the Synthetix claim bot by introducing a second conditional check. The script should issue an API request via `requests.get()` only when the pool is active AND network gas fees are low.

## 🛠️ Solution: Smart Synthetix Claimer

```python
import time
import requests

while True:
    
    # 1. Mock variables for testing logic
    pool_active = True
    gas_low = True
    
    # 2. Combined condition using the 'and' operator
    if pool_active and gas_low:
        
        # 3. Protected API request block
        try:
            requests.get("[https://api.synthetix.io/pool/claim](https://api.synthetix.io/pool/claim)")
            print("Success! Rewards claimed (gas fees were low).")
        except:
            print("Network Error! Server is unreachable.")
            
    else:
        # Executed if the pool is inactive OR gas fees are high
        print("Skipping execution. Pool is inactive or gas is too high.")
        
    # 4. Delay before the next loop iteration
    time.sleep(10)
