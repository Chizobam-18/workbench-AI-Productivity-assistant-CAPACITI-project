# Workbench — AI-Powered Workplace Productivity Assistant

A single-page web app that automates five common workplace tasks using Google's Gemini API. Built for the CAPACITI AI Skills Accelerator Programme project brief.

## Live features

1. **Smart Email Generator** — generates context-based, tone-adjusted emails for clients, managers, or teams.
2. **Meeting Notes Summarizer** — turns messy notes into key points, decisions, action items, and deadlines.
3. **AI Task Planner / Scheduler** — turns a task list into a prioritized, time-blocked plan.
4. **AI Research Assistant** — summarizes an article or topic into plain-language insights.
5. **AI Chatbot Interface** — a general-purpose assistant chat window.

Every tool shows the **exact prompt** sent to the model before showing the AI's response, so the prompt engineering behind each feature is visible, not hidden.

## Tools used

- **Google Gemini API** (`gemini-2.0-flash`) — the AI model powering every feature, called directly from the browser.
- **HTML / CSS / vanilla JavaScript** — no framework, no build step.

## How to run it

1. Get a free Gemini API key at [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey).
2. Open `index.html` in any browser (double-click it, or use a local server / GitHub Pages).
3. Click **"Set Gemini API key"** (bottom left) and paste your key.
4. Pick a tool from the sidebar and try it.

Your API key is kept only in the browser tab's memory for that session — it is never saved to a file, sent anywhere but Google's API, or written to disk/storage. Refreshing the page clears it.

## Responsible AI notes

- The Research Assistant tool includes a visible disclaimer that AI summaries can be incomplete and should be verified against original sources.
- Prompts explicitly instruct the model not to invent facts that weren't provided by the user.
- The app is transparent about what prompt produced each output (see the prompt console under each tool).

## Project documentation

See [`docs/documentation.md`](docs/documentation.md) for the problem statement, solution overview, sample prompts, and challenges/solutions writeup.

## Project brief

Built for the CAPACITI (UVU Africa) AI Skills Accelerator Programme — "AI-Powered Workplace Productivity Assistant" project.
