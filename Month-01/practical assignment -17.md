# Practical Assignment: Day 17

## 🎯 Task Description
Upgrade the bot to interact with a real-time data flow. The script must first make a GET request to fetch current pool information, parse the JSON response into a dictionary, extract the `reward` and `gas` variables using dictionary keys `[]`, and then use those dynamic values in the existing `if` logic.

## 🛠️ Solution: Fully Dynamic API Bot

```python
import time
import requests

while True:
    
    # Wrapping all network operations in a single safety net
    try:
        # 1. Fetching real-time market data from the server
        response = requests.get("[https://api.mock-defi.com/pool/info](https://api.mock-defi.com/pool/info)")
        
        # 2. Parsing the JSON response into a Python dictionary
        data = response.json()
        
        # 3. Extracting values using square brackets and keys
        reward = data["reward"]
        gas = data["gas"]
        
        # 4. Evaluating the real-time data
        if reward > 50 and gas < 15:
            # Making a second request to actually claim the rewards
            requests.get("[https://api.mock-defi.com/pool/claim](https://api.mock-defi.com/pool/claim)")
            print(f"Success! Claimed {reward} tokens at {gas} gwei gas.")
            
        else:
            print(f"Skipping. Current reward is {reward}, gas is {gas}.")
            
    except:
        # Protects against failures in either of the two requests
        print("Network Error! Could not fetch data or claim rewards.")
        
    time.sleep(10)
