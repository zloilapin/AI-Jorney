# Practical Assignment: Day 18

## 🎯 Task Description
Implement an authorization layer in the automated claim bot. Construct a headers dictionary containing a secret API key and attach it to the POST request responsible for executing the claim transaction, ensuring the server authenticates the bot.

## 🛠️ Solution: Authenticated API Execution

```python
import time
import requests

while True:
    try:
        # Fetching public market data (No headers required)
        response = requests.get("[https://api.mock-defi.com/pool/info](https://api.mock-defi.com/pool/info)")
        data = response.json()
        
        reward = data["reward"]
        gas = data["gas"]
        
        if reward > 50 and gas < 15:
            # 1. Constructing the authorization dictionary
            api_headers = {
                "API-Key": "crypto_token_999"
            }
            
            # 2. Passing the headers to authenticate the transaction
            requests.get("[https://api.mock-defi.com/pool/claim](https://api.mock-defi.com/pool/claim)", headers=api_headers) 
            
            print(f"Success! Claimed {reward} tokens.")
            
        else:
            print(f"Skipping. Reward is {reward}, gas is {gas}.")
            
    except:
        print("Network Error! Could not complete the cycle.")
        
    time.sleep(10)
