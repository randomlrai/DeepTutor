# DeepTutor

> An intelligent tutoring system powered by deep learning — Fork of [HKUDS/DeepTutor](https://github.com/HKUDS/DeepTutor)

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.10%2B-blue)](https://www.python.org/)
[![Issues](https://img.shields.io/github/issues/your-org/DeepTutor)](https://github.com/your-org/DeepTutor/issues)

## Overview

DeepTutor is an AI-powered tutoring assistant that helps learners understand complex documents, papers, and educational material through interactive Q&A, summarization, and guided explanations.

## Features

- 📄 **Document Understanding** — Upload PDFs or paste text for deep comprehension
- 💬 **Interactive Q&A** — Ask questions and receive context-aware answers
- 🧠 **Adaptive Explanations** — Responses tailored to the learner's level
- 🔍 **Source Grounding** — Answers linked back to source material
- 🗂️ **Session Memory** — Maintains context across a tutoring session

## Getting Started

### Prerequisites

- Python 3.10+
- [pip](https://pip.pypa.io/en/stable/) or [uv](https://github.com/astral-sh/uv)
- An OpenAI-compatible API key (or local model endpoint)

### Installation

```bash
# Clone the repository
git clone https://github.com/your-org/DeepTutor.git
cd DeepTutor

# Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Configuration

Copy the example environment file and fill in your credentials:

```bash
cp .env.example .env
```

Edit `.env`:

```env
OPENAI_API_KEY=your_api_key_here
OPENAI_BASE_URL=https://api.openai.com/v1   # or your local endpoint
MODEL_NAME=gpt-4o
```

### Running the App

```bash
python app.py
```

Then open your browser at `http://localhost:7860`.

### Docker

```bash
docker build -t deeptutor .
docker run -p 7860:7860 --env-file .env deeptutor
```

## Project Structure

```
DeepTutor/
├── app.py               # Main application entry point
├── core/
│   ├── tutor.py         # Core tutoring logic
│   ├── retriever.py     # Document retrieval pipeline
│   └── llm.py           # LLM client wrapper
├── ui/
│   └── gradio_app.py    # Gradio-based user interface
├── utils/
│   └── document.py      # Document parsing utilities
├── requirements.txt
├── Dockerfile
└── .env.example
```

## Contributing

Contributions are welcome! Please read our [contributing guidelines](.github/pull_request_template.md) and open an issue before submitting large changes.

1. Fork the repository
2. Create your feature branch (`git checkout -b feat/amazing-feature`)
3. Commit your changes following [Conventional Commits](https://www.conventionalcommits.org/)
4. Push to the branch and open a Pull Request

## Bug Reports & Feature Requests

Use the GitHub Issues templates provided:
- 🐛 [Bug Report](.github/ISSUE_TEMPLATE/bug_report.yml)
- ✨ [Feature Request](.github/ISSUE_TEMPLATE/feature_request.yml)
- ❓ [Question](.github/ISSUE_TEMPLATE/question.yml)
- 📖 [Documentation](.github/ISSUE_TEMPLATE/docs.yml)

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Original project: [HKUDS/DeepTutor](https://github.com/HKUDS/DeepTutor)
- Built with [LangChain](https://github.com/langchain-ai/langchain), [Gradio](https://github.com/gradio-app/gradio), and [FAISS](https://github.com/facebookresearch/faiss)
