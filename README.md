# Slow & Steady — Your Tiny-Step AI 🦥🌿

A gentle, local-first productivity helper for the “Slow and Steady” open-source AI challenge. It takes an overwhelming to-do list and turns it into tiny, low-pressure next steps.

## Demo
Deploy this repository with GitHub Pages to get a public website link.

## Features
- Responsive, calming interface.
- Smart Mode works directly in the browser with no API key.
- Optional local open-weight AI mode through Ollama (`qwen2.5:3b` by default).
- Task checkboxes and copyable plan.
- No accounts, analytics, or hosted AI API.

## Run it
1. Download or clone this repository.
2. Open `index.html` in a browser for Smart Mode.
3. For local model mode, install [Ollama](https://ollama.com/) and run:
   ```bash
   ollama run qwen2.5:3b
   ```
4. Configure Ollama to allow requests from the page origin using `OLLAMA_ORIGINS` before launching Ollama. For a local development test, `OLLAMA_ORIGINS=*` is convenient, but use it only in a trusted local environment.
5. Open the page and expand “Want to use a real open-weight AI model?”, enable “Use local AI”, and click “Make it feel smaller”.

> Note: Static hosting such as GitHub Pages serves the frontend only. Local AI mode works only on a computer where Ollama is installed and running, and browser cross-origin settings are configured. The hosted site does not host the model.

## Publish with GitHub Pages
1. Create a new public repository named `slow-and-steady-ai`.
2. Upload `index.html` and `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/(root)`, then Save.
5. Wait for the deployment and open the URL shown in the Pages section. It usually looks like `https://YOUR-USERNAME.github.io/slow-and-steady-ai/`.

## Why open innovation matters
The app is designed so the AI can run on a user's own computer through Ollama and an open-weight model. This can keep task text off a third-party AI service, makes the model replaceable, and avoids per-request hosted model fees after the model is downloaded. The trade-off is that users need enough local hardware and must install/configure the model. Smart Mode is a lightweight fallback and is rule-based—not itself a generative AI model.

## Challenge post draft
**Slow & Steady: a tiny-step AI for the tasks I keep putting off 🦥**

I built Slow & Steady, a calm productivity helper that turns a messy to-do list into small, low-pressure next actions. Instead of pushing people to do everything at once, it helps them pick a five-minute starting point.

The app has a browser-only Smart Mode and an optional local AI mode powered by Ollama and an open-weight model. The open approach matters because users can run the model on their own machine, keep task text away from a hosted AI provider, and swap models without rebuilding the whole experience. The trade-off is that local inference needs setup and suitable hardware, so I included a no-key fallback too.

The goal is simple: less overwhelm, one tiny step at a time.
