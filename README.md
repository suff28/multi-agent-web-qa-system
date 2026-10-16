# Multi Agent Web Research Assistant

## Overview

This project builds a local multi-agent question answering workflow that searches the web, compares evidence, evaluates source quality, and writes a final answer with supporting references.

The system uses multiple agent roles:

- Researcher Agent 1 creates a broad search query.
- Researcher Agent 2 creates a focused search query.
- Evaluator Agent compares retrieved evidence and selects the strongest sources.
- Writer Agent generates the final answer using the selected evidence.

## Tools And Technologies

- Python
- Jupyter Notebook
- LangGraph
- LangChain Ollama
- Ollama local language models
- DDGS web search
- JSON parsing and evidence ranking

## Project Structure

```text
.
├── docs/
│   ├── multi-agent-web-qa-report.docx
│   └── transcript-project-3.pdf
└── notebooks/
    └── multi-agent-web-qa-system.ipynb
```

## How To Run

1. Install and start Ollama.
2. Pull the local model used by the notebook:

```bash
ollama pull llama3.2:3b
```

3. Install the Python dependencies:

```bash
pip install langgraph langchain-ollama ddgs
```

4. Open the notebook:

```text
notebooks/multi-agent-web-qa-system.ipynb
```

5. Run the notebook cells and edit the demo question as needed.

## Example Use Case

The notebook includes a demo question about retrieval-augmented generation and shows how the agents generate search queries, retrieve sources, evaluate evidence, and write a final response.

## Note On Demo Video

The project demo video was kept outside this browser-upload package to avoid GitHub upload limits. It can be shared separately through Google Drive, YouTube, or GitHub Releases.

## Workflow Structure

The notebook implements **4 agents**: **2 researchers**, **1 evaluator**, and **1 writer**. It uses LangGraph and Llama 3.2 through Ollama to search, deduplicate results, rank evidence, and produce cited answers. Agent count describes the workflow structure, not an accuracy or latency result.
