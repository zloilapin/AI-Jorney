# Day 16: Dynamic Logging with F-Strings

## 📖 Theory: Making Strings Dynamic
When building automation bots, static text logs like "Gas is too high" are not informative enough for debugging or monitoring. We need the bot to report the exact numbers it processed. In Python, the most elegant way to inject variables into text is by using **f-strings** (Formatted String Literals).

## 🧱 The F-String Syntax
To create an f-string, prefix the string with the letter `f` (outside the quotes). Then, place any variable you want to insert inside curly braces `{}`.

*   **Static (Old way):** `print("Reward is low")`
*   **Dynamic (F-string):** `print(f"Reward is currently {reward} SNX")`

When the code runs, Python evaluates the variables inside the brackets and seamlessly converts them into text as part of the entire message.
