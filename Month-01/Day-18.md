# Day 18: API Authorization and Headers

## 📖 Theory: Passing the Bouncer
While fetching public data (like gas prices) requires a simple GET request, interacting with private accounts or executing transactions requires identification. APIs need to verify who is making the request to prevent unauthorized access. This "ID check" is handled through **Headers**.

## 🧱 Structuring Headers
Headers are metadata sent alongside your request. In Python, headers are structured exactly like standard dictionaries, using `Key: Value` pairs. 
When the API provider issues you a secret API Key, you store it in a headers dictionary and pass it to the `requests` function using the `headers=` parameter.

*   **Dictionary Creation:** `my_headers = {"API-Key": "your_secret_token"}`
*   **Execution:** `requests.get("https://api.com/secure-endpoint", headers=my_headers)`
*   
