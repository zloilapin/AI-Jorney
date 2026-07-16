# Practical Assignment 3: Designing Routing Logic (Pseudocode)

## 🎯 Task Description
To prevent script crashes and ensure data purity, the automated system needs a logical routing tree. The script must evaluate the JSON response received from the AI model and make physical decisions (moving files into appropriate directories), while safely discarding unreadable or corrupted data.

## 📋 Conditions & Rules
* There are 4 valid card suits: `hearts`, `spades`, `diamonds`, `clubs`. Each requires its own destination folder.
* **Rule 1 (Fail-safe):** The script must first check the `is_visible` boolean. If it is `false` (the card is obscured by another window), move the file to the `recognition_errors` folder and stop processing the current file.
* **Rule 2 (Sorting):** If `is_visible` is `true`, route the file to the correct folder based on the recognized suit.
* **Rule 3 (Fallback):** If the AI returns an unknown or empty suit value (AI hallucination), move the file to the `recognition_errors` folder to prevent script failure.

---

## 🛠️ Solution: Routing Pseudocode

```text
IF is_visible == false:
    Move screenshot to "recognition_errors" folder
    Stop processing current file

ELSE (if is_visible == true):
    IF suit == "hearts":
        Save to "Hearts" folder
        
    ELSE IF suit == "spades":
        Save to "Spades" folder
        
    ELSE IF suit == "clubs":
        Save to "Clubs" folder
        
    ELSE IF suit == "diamonds":
        Save to "Diamonds" folder
        
    ELSE (if an unknown text/suit is received):
        Move screenshot to "recognition_errors" folder
