# Day 6: Parsing JSON Responses in Python

## 🎯 Objective
To extract specific data points from an AI model's JSON response and use them in the script's decision-making logic.

## 🧠 What I Learned
* **Unpacking Responses:** I learned to use the `.json()` method on the response object to convert the server's text reply into a readable Python dictionary.
* **Data Extraction (Parsing):** I understand how to target specific values using their keys (e.g., `data["suit"]`). This isolates the exact piece of information the script needs.
* **Completing the Loop:** I can now connect the extracted data to my `if/else` logic, completing the full automation cycle: Request $\rightarrow$ Response $\rightarrow$ Parse $\rightarrow$ Action.

## 🛠️ Code Example
```python
data = response.json()
detected_suit = data["suit"]

if detected_suit == "hearts":
    # Action for hearts
    pass
