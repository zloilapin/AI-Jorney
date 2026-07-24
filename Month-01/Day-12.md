# Day 12: Architectural Integration (The Master Script)

## 📖 Theory: Component Integration
Real automation scripts are built by combining modular concepts. An autonomous agent typically requires:
1. **Execution Engine:** `while True` loop to keep the script alive.
2. **Resource Manager:** `if/else` logic with Boolean flags to prevent unnecessary, costly API calls.
3. **Safety Net:** `try/except` blocks wrapping any external network requests to prevent fatal crashes.
4. **Pacing Control:** `time.sleep()` to manage system resource consumption and avoid rate limits.

## 🧱 Theory: Deep Indentation
As logic becomes nested (e.g., a `try` block inside an `if` block, which is inside a `while` loop), indentation deepens (4, 8, 12 spaces). Maintaining strict visual hierarchy is critical; otherwise, Python will execute commands in the wrong sequence or throw an `IndentationError`.
