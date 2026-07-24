# Day 17: JSON Responses and Dictionaries

## 📖 Theory: Replacing Mock Data with Real Data
A production bot must fetch real-time market data instead of relying on hardcoded variables. When you send a request to a modern API, the server replies with a JSON payload. In Python, this JSON is converted into a structure called a **Dictionary**.

## 🧱 Unpacking Data
Dictionaries store data in `Key: Value` pairs. To utilize the data sent by the server, you must extract it using its specific key.
1.  **Capture the response:** Store the API's reply in a variable (`response = requests.get(...)`).
2.  **Parse the JSON:** Convert the raw response into a Python dictionary using the `.json()` method.
3.  **Extract by Key:** Use square brackets `[]` with the exact key name as a string to extract the value. 
    *Example:* `current_gas = data["gas"]`.
    
