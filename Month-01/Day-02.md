# Day 2: APIs and the JSON Data Format

## 🧠 What I Learned Today
Today, I learned how the different components of an AI automation system communicate with each other:
*   **API (Application Programming Interface):** I understood the concept of an API using the "restaurant waiter" metaphor. An API acts as the messenger that takes a request from my script, delivers it to the AI model (the "chef"), and brings back the processed result.
*   **JSON (JavaScript Object Notation):** I learned that programs don't exchange raw human text because it's too difficult for scripts to parse. Instead, they use JSON—a structured data format based on `"key": "value"` pairs. 
*   **Structured Output:** Getting an AI model to return data in a strict JSON format is crucial for building reliable automation pipelines, such as sorting detected objects or extracting specific data points.

## 💡 Next Steps
I am ready to complete my practical assignment by manually writing my first JSON structure to understand its syntax rules.
### Practical Assignment 2: Designing an API Response (Structured Output)

**🎯 Business Objective:** 
To automate the collection of a massive dataset of playing cards from online clients, a connection needs to be established between a parser script and a Computer Vision (CV) model. The AI model must return data about the recognized card in a strict format so the script can automatically sort the screenshots into folders without human intervention.

**🛠 What was done:**
I designed a JSON schema (data contract) that obligates the AI to return:
1. Basic object attributes (suit, rank).
2. An array of `bounding_box` coordinates to programmatically crop the card from the full screenshot.
3. A nested `table_context` object to collect additional game statistics (player position).

**📄 Solution file:** `Practical-assignment-2.json`

