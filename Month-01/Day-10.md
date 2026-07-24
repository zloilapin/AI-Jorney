# Day 10: Boolean Logic and Cost-Efficient Architecture

## 📖 Theory: Booleans (True / False)
In automation, variables don't just store numbers or text; they also store states. Python uses Boolean values (`True` and `False`) to represent flags. These flags act as simple, binary indicators (e.g., `is_active = True`). Note that `True` and `False` must always be capitalized and written without quotes.

## 🧱 Theory: Local Checks (Cost Efficiency)
Before an automation script sends a request to an expensive external API (like a paid AI model), it should always perform a free, local check using a Boolean flag. If the flag indicates that the action is unnecessary (e.g., it's not the user's turn), the script skips the API call, saving resources and budget.

## 🧠 Best Practices: Shorthand Evaluation
Instead of explicitly checking `if variable == True:`, Python allows a shorthand evaluation: `if variable:`. 
Similarly, to check for a negative state, engineers use the `not` operator: `if not variable:` instead of `if variable == False:`.
