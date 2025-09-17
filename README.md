# AI Chat Interface

A lightweight, multi‑model chat interface built with **Gradio**, **OpenAI**, **Anthropic**, and **Google Gemini**.  
Run the Jupyter notebook to launch a web UI where you can converse with any of the supported LLMs.

## 🚀 Quick Start

1. **Clone the repo**

   ```bash
   git clone https://github.com/AsutoshaNanda/AI-Chat-Interface.git
   cd AI-Chat-Interface
   ```

2. **Create a virtual environment & install dependencies**

   ```bash
   python -m venv .venv
   source .venv/bin/activate   # on Windows: .venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Add your API keys**

   Create a `.env` file in the project root:

   ```dotenv
   OPENAI_API_KEY=sk-...
   ANTHROPIC_API_KEY=sk-ant-...
   GOOGLE_API_KEY=AIzaSy...
   ```

4. **Launch the interface**

   Open the notebook `Chat Interface.ipynb` and run all cells, or execute the helper script:

   ```bash
   jupyter notebook "Chat Interface.ipynb"
   ```

   The notebook will start a Gradio app and provide a public shareable link.

## 📚 What’s Inside?

- **`Chat Interface.ipynb`** – The main notebook containing:
  - Environment loading (`python-dotenv`)
  - Client setup for OpenAI, Anthropic Claude, and Google Gemini
  - A streaming chat function that preserves conversation history
  - Gradio UI (`gr.ChatInterface`) for real‑time interaction
- **`README.md`** – This guide (high‑level overview, setup, usage).

## ✨ Features

- **Multi‑model support** – Switch between GPT‑4o‑mini, Claude, and Gemini with the same UI.
- **Streaming responses** – See the assistant’s answer appear token‑by‑token.
- **Conversation history** – Context is preserved across turns.
- **Shareable UI** – Gradio’s `share=True` gives you a public URL for demos.

## 🛠️ Prerequisites

- Python 3.11 or newer
- API keys for the services you intend to use (OpenAI, Anthropic, Google Gemini)
- Internet connection (the models are accessed via their respective APIs)

## 📦 Installation Details

The notebook installs the following key libraries (included in `requirements.txt`):

| Library | Purpose |
|---------|---------|
| `python-dotenv` | Load `.env` variables |
| `openai` | OpenAI API client |
| `anthropic` | Claude API client |
| `google-generativeai` | Gemini API client |
| `gradio` | Web UI |
| `beautifulsoup4` & `requests` | (optional) future web‑scraping extensions |

If you need to add more dependencies, update `requirements.txt` and run:

```bash
pip install -r requirements.txt
```

## 🖥️ Running the App

1. Start the notebook.
2. Execute all cells in order.
3. The final cell runs:

   ```python
   gr.ChatInterface(fn=chat).launch(share=True)
   ```

   This opens a local Gradio interface (e.g., `http://127.0.0.1:7860`) and prints a public link.

### Command‑line alternative

If you prefer a pure Python script, create `run_chat.py` with the same logic as the notebook and run:

```bash
python run_chat.py
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

- Add support for additional LLM providers.
- Improve the UI/UX (e.g., custom styling, system prompt editing).
- Write tests or CI pipelines.
- Update documentation.

Fork the repo, create a feature branch, and submit a pull request.

---

*Happy chatting! 🎉*
