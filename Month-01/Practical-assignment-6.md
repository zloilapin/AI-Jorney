# Practical Assignment 6: Parsing JSON Responses

## 🎯 Business Task Description
After receiving a response from the AI Vision model, the script must parse the raw JSON text into a usable Python dictionary. The objective is to extract specific data points (e.g., the rank of the recognized card) from this dictionary and assign them to isolated variables for further logic processing.

## 📋 Mock Data
The AI returns the following structured data:
```json
{
  "is_visible": true,
  "suit": "hearts",
  "rank": "Ace"
}
```

## 🛠️ Solution: Data Extraction Code
```python
# Step 1: Parse the raw response into a Python dictionary
data = response.json()

# Step 2: Extract the specific value using its Key
detected_rank = data["rank"]

# The variable 'detected_rank' now holds the string value "Ace"
```
