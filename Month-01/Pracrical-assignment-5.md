# Practical Assignment 5: Building the API Request Module

## 🎯 Task Description
The automation system requires a core script to physically transmit the captured card images to the AI server over the internet. The objective is to write the complete Python code block that imports the necessary network library, isolates the authorization headers from the payload, and executes the HTTP POST request.

## 🛠️ Solution: Python `requests` Implementation

```python
# 1. Import the standard library for making HTTP requests
import requests

# 2. Define the Headers variable (Metadata and Security)
my_headers = {
    "Authorization": "Bearer YOUR_SECRET_API_KEY",
    "Content-Type": "application/json"
}

# 3. Define the Body variable (Instructions and Data payload)
my_body = {
    "model": "vision-advanced-01",
    "prompt": "Analyze this image and return the card suit and rank in strict JSON format.",
    "image_base64": "iVBORw0KGgoAAAANSUhEUgAAAMgAA..." # Truncated for readability
}

# 4. Execute the POST request
# We pass the URL, the headers box, and the json body box to the courier
response = requests.post(
    url="[https://api.vision-model-provider.com/v1/analyze](https://api.vision-model-provider.com/v1/analyze)",
    headers=my_headers,
    json=my_body
)

