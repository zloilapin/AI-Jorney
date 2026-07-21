# Practical Assignment 5: Handling Missing Data (Error Prevention)

## 🎯 Task Description
AI models can sometimes hallucinate or fail to return the expected JSON structure. If the Python script attempts to access a missing key (like `"suit"`), it will trigger a `KeyError` and crash the entire automation loop. 
The objective is to implement a safety mechanism to catch these errors so the script continues running smoothly even when the AI fails.

## 🛠️ Solution: Try/Except Block

In Python, we use a `try / except` block. We tell the script to *try* extracting the data. If it encounters a `KeyError`, it will not crash. Instead, it will execute the fallback plan inside the *except* block (e.g., move the bad screenshot to an error folder and continue to the next one).

### Python Code Implementation

```python
# The script receives an unpredictable response from the AI
data = response.json()

try:
    # 1. We TRY to extract the suit
    detected_suit = data["suit"]
    
    # 2. If successful, we route the file
    if detected_suit == "hearts":
        print("Success: Moving to Hearts folder")
        
except KeyError:
    # 3. If the "suit" key is completely missing, the script jumps here INSTEAD of crashing
    print("Warning: AI failed to return the card suit.")
    print("Action: Moving screenshot to 'recognition_errors' folder.")
