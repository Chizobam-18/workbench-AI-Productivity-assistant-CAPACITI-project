# Workbench — Project Documentation

**Candidate:** Tracey Chukwuyem
**Programme:** CAPACITI AI Skills Accelerator (UVU Africa)
**Project:** AI-Powered Workplace Productivity Assistant

---

## 1. Problem Statement

Professionals spend a significant portion of their working day on repetitive tasks: drafting emails, summarizing meetings, planning schedules, and researching information. Doing these manually is slow and inconsistent — the same email might take 15 minutes to word correctly, and meeting notes often go unread because no one has time to organize them into action items.

## 2. Solution Overview

**Workbench** is a browser-based AI assistant that automates five of these workplace tasks in one place: a smart email generator, a meeting notes summarizer, a task planner, a research assistant, and a general chatbot. Each tool is built around a carefully engineered prompt template that constrains the AI's output to something structured, relevant, and immediately usable — rather than a generic, open-ended chat response.

The app is a single HTML file with no backend or build step, so it can be opened directly in a browser or hosted for free on GitHub Pages. It calls Google's Gemini API directly from the browser using the user's own free API key.

## 3. Tools Used

- **Google Gemini API** (`gemini-2.0-flash`) — generates all AI content.
- **Google AI Studio** — used to obtain a free Gemini API key.
- **HTML / CSS / JavaScript** — the application itself.
- **GitHub** — version control and submission.

## 4. Sample Prompts

**Email Generator** (tone: persuasive, audience: manager):
```
Write a persuasive email to a manager.
Purpose: asking for a deadline extension
Context: The project is delayed because of a supplier issue, I need 3 extra
days, and I want to reassure them quality won't suffer.

Requirements:
- Match the tone precisely...
- Adjust formality to suit a manager (brevity, clear ask)...
- Include a subject line, keep it under 150 words, don't invent facts.
```

**Meeting Summarizer:**
```
Raw meeting notes: """[pasted notes]"""

Produce a structured summary with these exact sections:
1. Key Points (max 5 bullets)
2. Decisions Made
3. Action Items (Owner — Task — Deadline)
4. Open Questions / Follow-ups
```

The full prompt for every tool is visible live in the app itself (the "prompt console" panel shown before each result), so graders can see exactly how each output was engineered.

## 5. Challenges and Solutions

| Challenge | Solution |
|---|---|
| Generic AI chat responses (rambling, unstructured) don't work as a "task planner" or "email generator" | Each tool uses a rigid prompt template that specifies exact output sections/format, so the model returns something structured every time rather than free-form text |
| API keys shouldn't be hardcoded into a public GitHub repo | The app asks the user for their own key at runtime and keeps it only in browser memory for that session — nothing is committed to the repo or written to storage |
| AI can generate incorrect or invented information, especially for research summaries | Prompts explicitly instruct the model not to invent facts beyond what's provided, and the Research Assistant tool displays a visible disclaimer to verify important facts against original sources |
| Keeping the tool lightweight enough to run without installation | Built as a single static HTML file with vanilla JavaScript — no npm install, no server, works by just opening it in a browser or via GitHub Pages |

## 6. Ethical & Responsible AI Considerations

- **Transparency:** every generated output is shown alongside the exact prompt that produced it.
- **No fabrication:** prompts instruct the model to only use information the user actually provided.
- **Human-in-the-loop:** the tool is positioned as a *draft generator*, not a final-answer machine — emails, summaries, and plans are meant to be reviewed before use.
- **Limitations disclosed:** the Research Assistant carries a visible warning about verifying AI-generated facts.

## 7. Impact

Workbench demonstrates how a single, well-scoped prompt library can turn a general-purpose AI model into five distinct, purpose-built workplace tools — cutting the time spent on emails, meeting admin, planning, and research from many minutes down to seconds, while keeping a human in control of the final output.
