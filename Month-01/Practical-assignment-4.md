# Practical Assignment 4: Designing an API POST Request

## 🎯 Task Description
To automate the extraction of playing card data from gaming clients, the system must send captured screenshots to a Vision AI model. The objective is to design the exact structure of the HTTP POST request that the Python script will execute, ensuring all network protocols (Headers) and data requirements (Body) are met.

## 🛠️ Solution: API Request Structure

### 1. The Endpoint (Where to send)
**Method:** `POST`
**URL:** `https://api.vision-model-provider.com/v1/analyze`

### 2. Headers (The Metadata & Security)
The headers must contain the authorization key to access the AI server and specify that the body is formatted as JSON.

```json
{
  "Authorization": "Bearer YOUR_SECRET_API_KEY_HERE",
  "Content-Type": "application/json"
}
### 3. Body
{
  "model": "vision-advanced-01",
  "prompt": "Analyze this image and return the card suit and rank in strict JSON format.",
  "image_base64": "iVBORw0KGgoAAAANSUhEUgAAAMgAAADICAYAAACtWK6eAAAB...",
  "require_structured_output": true
}
