# Core Coding & Workflow Standards

To ensure Senior-level code quality, ALL agents must adhere to the following standards regardless of the language:

## 💻 Code Quality Rules
1. **Modular Code:** Functions/methods must do one thing. If a function is >40 lines, the AI must break it down.
2. **Robust Error Handling:** The AI must NEVER swallow exceptions (e.g., empty `except:` or `catch (e) {}`). It must catch specific errors, log them with context, and fail gracefully.
3. **Logging > Printing:** Never use raw `print()` or `console.log()` for debugging in production code.
4. **Environment Awareness:** The AI must always verify it is in the correct virtual environment (e.g., `.venv`, `node_modules`) before installing packages or running scripts.

## 🚀 Advanced Workflow Patterns (Lifehacks)
To maximize efficiency and minimize context pollution, ALL agents use these advanced patterns:

1. **Self-Correction (TDD Approach):** The AI must never output code and just say "done". It must run the code itself or write a quick test script to verify it works. If it encounters an error, it fixes it before responding.
2. **Save Points (Local Backups):** Before making sweeping changes to critical files, the AI creates a save point (e.g., a local git commit or copying to a backup folder).
3. **Incremental Check-ins (The 30% Rule):** For large tasks, the AI does NOT generate massive amounts of code at once. It builds the skeleton/interfaces, stops, and asks the human "Does this architecture look correct?" before proceeding.
4. **Context Scratchpads:** The AI does NOT dump huge logs or complex calculations directly into the chat. It creates temporary files in a `scratch/` directory, analyzes them, and outputs only the concise summary.
5. **Tool-making:** If the AI finds itself running the same complex terminal commands repeatedly, it writes a small shell/python automation script.
