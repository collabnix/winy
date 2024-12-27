# Winy 🍷

A smart wine recommendation system that suggests perfect wine pairings for your dishes using AI. The application leverages Large Language Models and vector search to provide personalized wine recommendations along with educational information about wine pairings.

## Features

- Interactive chat interface for wine recommendations
- AI-powered sommelier responses using Mistral LLM
- Semantic search for wine pairings using Qdrant
- Direct links to purchase recommended wines
- Docker support for easy deployment

## Prerequisites

- Python 3.10 or higher
- Docker (optional)
- Ollama server running with Mistral model
- Qdrant server instance

## Environment Variables

The following environment variables need to be set:

- `QDRANT_CLIENT`: URL for your Qdrant server
- `OLLAMA`: URL for your Ollama server

## Installation

### Local Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/winy.git
cd winy
```

2. Install dependencies:
```bash
pip install -r app/requirements.txt
```

3. Run the application:
```bash
streamlit run app/main.py
```

### Docker Setup

1. Build the Docker image:
```bash
docker build -t winy ./app
```

2. Run the container:
```bash
docker run -p 8501:8501 \
  -e QDRANT_CLIENT=your_qdrant_url \
  -e OLLAMA=your_ollama_url \
  winy
```

## Usage

1. Access the application at `http://localhost:8501`
2. Enter a dish or cuisine in the chat interface
3. Receive personalized wine recommendations with educational information
4. Click on wine names to view purchase options
