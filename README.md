# Text → PowerPoint (Template-Aware)


Turn raw text/markdown into a fully styled PowerPoint that inherits colors, fonts, layouts, and images from an uploaded .pptx/.potx template — powered by your own LLM API key (OpenAI, Anthropic, or Gemini). No AI image generation. Keys are never stored or logged.


## Features
- Paste large text or markdown
- Optional one-line guidance (e.g., “investor pitch deck”, “research summary”)
- Bring your LLM API key of choice (OpenAI / Anthropic / Gemini)
- Upload a PowerPoint template (.pptx or .potx)
- Intelligent slide count & structure (LLM + fallback heuristics)
- Copies template styling (masters, layouts, theme colors/fonts) and reuses template images where possible
- Download a new .pptx


## Quick Start


### 1) Clone and install
```bash
# in a fresh folder
git clone <your-repo-url> text-to-pptx
cd text-to-pptx


# Front-end
cd web
npm i
cd ..


# Back-end (Python 3.10+)
cd server
python -m venv .venv && source .venv/bin/activate # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
```


### 2) Run locally
```bash
# back-end
cd server
uvicorn app:app --host 0.0.0.0 --port 8000 --proxy-headers --forwarded-allow-ips "*"


# front-end
cd ../web
npm run dev -- --port 5173
```
Open http://localhost:5173
