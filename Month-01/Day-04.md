# Day 4: Internet Anatomy for Scripts (HTTP, GET, POST)

## 🧠 What I Learned Today
Today, I dove deeply into the theoretical foundation of network requests, learning exactly how local scripts communicate with remote AI models over the internet.
* **Client-Server Architecture:** I learned that my Python script acts as the "Client" that initiates requests, while the AI model acts as the "Server" that processes data and responds.
* **HTTP Protocol & Methods:** I explored the rules of web communication.
  * **GET:** Used strictly to retrieve data without modifying anything on the server.
  * **POST:** The workhorse of AI automation. Used to securely send heavy payloads (like images or complex JSON prompts) to an AI model for processing.
* **Anatomy of an API Request:** A valid POST request requires an Endpoint (URL), Headers (metadata, including API Keys for authorization), and a Body (the actual data payload).
* **HTTP Status Codes:** I learned how to interpret server responses: `200` (Success), `400` (Bad Request/Syntax Error), `401` (Unauthorized/Invalid API Key), and `500` (Server Error).
* 
