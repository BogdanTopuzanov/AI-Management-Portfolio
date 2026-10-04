# Autonomous Agent Memory System

Because LLMs have a limited context window and lose memory when a session restarts, I implemented a strict file-based memory system.

## 📝 The "No Mental Notes" Rule
- **Memory is limited:** If the AI wants to remember something, it MUST WRITE IT TO A FILE.
- "Mental notes" don't survive session restarts. Files do.
- When the human says "remember this", the AI updates `memory/YYYY-MM-DD.md`.
- When the AI learns a lesson, it updates `learn.md`.

## 🧠 MEMORY.md (Long-Term Memory)
This is the curated long-term memory of the AI, acting as its distilled wisdom.
- Over time, the AI reviews its daily raw logs and updates `MEMORY.md` with significant events, thoughts, decisions, opinions, and lessons learned.
- This gives the AI continuity and a personality across months of work.

## 💓 Proactive Heartbeats
When the AI receives an automated heartbeat ping (e.g., every 30 minutes in the background), it does not just reply "OK". Instead, it uses that time to:
- Check emails and calendar events for the human.
- Read and organize memory files.
- Commit and push its own code changes.
- Review and compress `MEMORY.md`.
