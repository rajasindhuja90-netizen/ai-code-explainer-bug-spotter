# AI Code Explainer & Bug Spotter

A simple AI-powered web app that explains any code snippet in plain English and flags potential bugs or issues — built with Streamlit and the OpenAI API.

## Why I built this

This project is part of an "AI Tools & Mini Project" learning module, exploring how AI tools like ChatGPT/GPT models can assist with coding, research, and productivity. Instead of just using ChatGPT in a browser, I wanted to build a small tool that uses the API directly to solve a real, everyday problem: understanding and debugging unfamiliar code faster.

## Features

- Paste any code snippet (any language)
- Choose to: explain the code, find bugs, or both
- Optional language hint for more accurate analysis
- Clean, simple Streamlit UI
- Uses OpenAI's chat completion API under the hood

## Tech Stack

- Python
- [Streamlit](https://streamlit.io/) — UI
- [OpenAI API](https://platform.openai.com/) — code explanation & bug detection
- python-dotenv — local environment variable management

## Setup

1. **Clone the repo**
   ```bash
   git clone https://github.com/<your-username>/ai-code-explainer.git
   cd ai-code-explainer
   ```

2. **Create a virtual environment (optional but recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Add your OpenAI API key**

   Copy `.env.example` to `.env` and add your key:
   ```bash
   cp .env.example .env
   ```
   Or just paste your API key directly into the app's sidebar at runtime — it's never stored.

5. **Run the app**
   ```bash
   streamlit run app.py
   ```

   The app will open at `http://localhost:8501`.

## How it works

1. You paste a code snippet into the text area.
2. You choose whether you want an explanation, a bug report, or both.
3. The app builds a prompt and sends it to the OpenAI Chat Completions API.
4. The model's response (explanation and/or bug list with fixes) is displayed in the app.

## What I learned

- How to integrate an LLM API into a real application, not just chat with it
- Prompt design for two distinct tasks (explaining vs. debugging) using the same underlying model
- How AI tools can meaningfully speed up code comprehension and review

## Possible future improvements

- Syntax highlighting for the input code
- Support for multiple AI providers (Gemini, Claude) with a dropdown
- Save/export analysis history
- File upload instead of paste-only

---
