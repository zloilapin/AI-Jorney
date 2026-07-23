# Practical Assignment: Week 1 Master Script

## 🎯 Business Task Description
Develop a complete automation script to analyze a poker table screenshot (`table.png`) using an AI Vision API. The script must encode the image, construct the correct API request with headers and payload, parse the JSON response, and safely extract the current pot size using error handling (`try/except`).

## 🛠️ Solution: Full Automation Script
```python
import requests
import base64

# 1. Open and encode the image file securely
with open("table.png", "rb") as image_file:
    encoded_img = base64.b64encode(image_file.read()).decode('utf-8')

# 2. Construct API credentials and payload
my_headers = {
    "Authorization": "Bearer YOUR_API_KEY", 
    "Content-type": "application/json"
}

my_body = {
    "model": "vision-advanced-01", 
    "prompt": "Analyze Pot on the table",
    "image_base64": encoded_img
}

# 3. Send the POST request to the API
response = requests.post(
    url="[https://api.poker-vision.com/analyze](https://api.poker-vision.com/analyze)",
    headers=my_headers,
    json=my_body
)

# 4. Parse the JSON response
data = response.json()

# 5. Safely extract the target data
try: 
    pot_table = data["pot"]
    print("Success! Current pot size:", pot_table)
except KeyError:
    print("Error: Pot size not found in the response.")
```

## 🧠 Key Engineering Concepts Mastered
* **Network Communication:** Using the `requests` library to send POST requests.
* **Data Encoding:** Converting images to text format using `base64`.
* **API Structure:** Building correct `Headers` (authentication) and `Body` (payload) for the AI model.
* **Data Parsing:** Transforming raw text responses into Python dictionaries using `.json()`.
* **Error Handling:** Protecting the script from crashing during dictionary key extraction using `try/except`.
* 
