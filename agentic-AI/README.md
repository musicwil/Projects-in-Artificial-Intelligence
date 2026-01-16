# Educational Coach — Agentic AI Case

Educational Coach is a cloud-deployed, interactive AI system that helps users understand technical and analytical concepts through structured explanations, optional spoken responses, and guided follow-up prompts.

This project demonstrates how modern AI systems combine:
- Large Language Models (LLMs)
- Authentication & access control
- Conditional tool use (speech-to-text, text-to-speech)
- Cloud-native deployment
- User-facing web integration

The live demo is embedded on my website and accessible to signed-in members.

---

## Architecture Overview

**High-level flow**
1. User submits a question (typed or recorded audio)
2. Request is authenticated via Ghost member JWT
3. Input is routed to the AI reasoning layer
4. Optional tools are invoked (speech-to-text, text-to-speech)
5. Structured response is returned to the UI

---

## Repository Structure

```text
agentic-AI/
├── backend/        # FastAPI service (Cloud Run)
├── frontend/       # HTML / JS client (Ghost embed)
├── assets/         # Images, diagrams
├── docs/           # Architecture notes & design decisions
├── README.md
└── .gitignore

Technologies Used

Backend: Python, FastAPI

LLM: Google Gemini (via API)

Speech Services: Azure Speech-to-Text & Text-to-Speech

Auth: Ghost Members JWT

Deployment: Google Cloud Run

Frontend: HTML, CSS, JavaScript (embedded via Ghost)

Status

✅ Live and functional
✅ Auth-protected
✅ Audio + text workflows supported

Live Demo

The Educational Coach can be used directly from the project post on my site:
👉 https://www.wil725.com
