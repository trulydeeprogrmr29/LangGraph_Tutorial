🧠 LangGraph Learning Repository (Developer Notes)

This repository is my personal learning workspace while following the LangGraph Complete Course (freeCodeCamp) and experimenting as a developer.

The goal is not a finished product, but to:

Understand LangGraph internals

Practice agent orchestration

Build intuition for stateful AI workflows

Prepare for real-world AI engineering & interviews

🎯 Why I’m Learning LangGraph

Traditional LLM apps use linear chains.
LangGraph allows:

✅ Stateful execution

✅ Conditional branching

✅ Loops & retries

✅ Multi-agent workflows

As a developer, this is critical for:

Autonomous agents

Tool-using assistants

RAG (Retrieval-Augmented Generation)

Production-grade AI systems

📦 Tech Stack Used
Library	Why I Use It
LangGraph	Core framework for graph-based agents
LangChain	LLM abstractions, tools, prompts
langchain_openai	OpenAI model integration
langchain_community	Loaders, vector stores, OSS tools
ChromaDB	Local vector database for RAG
python-dotenv	Secure API key handling
typing / typing_extensions	Type safety & clarity
IPython	Interactive experimentation
📁 Project Structure (Learning-Oriented)
LangGraph_Tutorial/
│
├── graphs/                # LangGraph workflows (core learning)
│   ├── basic_graph.py
│   ├── conditional_graph.py
│   └── agent_graph.py
│
├── experiments/           # Scratch & exploration code
│
├── utils/                 # Helper functions (LLM, state, tools)
│
├── main.py                # Run graphs from here
├── requirements.txt
├── pyproject.toml
├── .env                   # API keys (ignored in git)
└── README.md

🚀 Setup Instructions (Developer Friendly)
1️⃣ Create Virtual Environment
python -m venv venv


Activate:

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate

2️⃣ Install Dependencies
pip install -r requirements.txt


Or using uv:

uv add -r requirements.txt

3️⃣ Environment Variables

Create a .env file:

OPENAI_API_KEY=your_api_key_here


Load it in Python:

from dotenv import load_dotenv
load_dotenv()

🧩 How I Use This Repo

This repo is used to:

🔬 Rebuild examples from the tutorial

✍️ Rewrite code in my own way

🧠 Add comments explaining why something works

🧪 Break things intentionally to understand errors

This is developer-first learning, not copy-paste.

🧠 Key LangGraph Concepts I’m Practicing
🔹 State

Shared object passed across nodes
(usually a TypedDict)

🔹 Node

A Python function that:

Takes state

Returns state updates

🔹 Edge

Defines control flow

Static edge

Conditional edge

🔹 Graph

The full workflow connecting nodes + edges

🧪 Example (Conceptual)
def node_a(state):
    return {"count": state["count"] + 1}


Edges decide:

where execution goes next

whether to stop or loop

📚 Learning Strategy

First → Understand graph flow

Then → Add tools

Then → Add memory

Then → RAG

Finally → Multi-agent setups

I focus on:

“Can I explain this without code?”

⚠️ Notes to Future Me

LangGraph ≠ LangChain chains

Graphs shine when logic is non-linear

Types matter a LOT

Debug graphs step-by-step

Don’t over-engineer early

📌 Status

🚧 Work in Progress
This repository will evolve as my understanding deepens.

📺 Learning Resource

LangGraph Complete Course – freeCodeCamp

YouTube: https://youtu.be/jGg_1h0qzaM

🧑‍💻 About Me

I’m learning LangGraph as a developer, focusing on:

AI Engineering

Agentic Systems

Practical, production-ready understanding

