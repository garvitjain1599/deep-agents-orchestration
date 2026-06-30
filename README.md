# 🧠 Deep Agents Orchestration

A production-style implementation of the **Deep Agents** framework showcasing autonomous planning, context engineering, reusable skills, specialized subagents, multiple storage backends, conversation memory, and tool integration through an interactive Streamlit application.

This project explores how modern AI agents can solve complex, multi-step tasks by combining reasoning, planning, persistent memory, delegated execution, and external tools.

---

## 🚀 Features

### 📝 Autonomous Task Planning

- Automatically breaks complex requests into smaller actionable tasks
- Generates dynamic TODO lists during execution
- Displays intermediate planning steps in the UI

---

### 🌐 Web Research

- Integrated Tavily Search for internet access
- Performs research when required
- Returns responses with source citations

---

### 🧠 Context Engineering

The agent supports multiple techniques for providing long-term context:

- AGENTS.md for persistent instructions
- Custom system prompts
- Memory loading during initialization
- Thread-aware conversation history

---

### 🛠️ Reusable Skills

The project demonstrates how Deep Agents can be extended using modular skills.

The demo notebooks include skills such as:

- Python programming
- AWS-related tasks
- LangGraph workflows
- Report writing

Skills are automatically selected and executed whenever they best match the user's request.

---

### 🤖 Specialized Subagents

Supports delegation to dedicated AI subagents for specialized tasks.

Examples include:

- Research Agent
- Structured Research Agent

The structured researcher returns validated Pydantic outputs including:

- Summary
- Confidence score
- Sources

---

### 💾 Multiple Storage Backends

The application demonstrates three Deep Agents storage backends.

#### StateBackend

- In-memory virtual filesystem
- Per-thread state
- Fast and ephemeral

#### FilesystemBackend

- Uses a real project directory
- Virtual sandbox mode
- File read/write capabilities

#### StoreBackend

- Persistent shared storage
- Cross-thread memory
- Long-lived agent knowledge

The backend can be switched directly from the Streamlit interface.

---

### 🧠 Conversation Memory

Built using LangGraph checkpointing.

Supports:

- Multi-turn conversations
- Thread-based memory
- Persistent storage through StoreBackend

---

### 📂 Virtual File System

Demonstrates Deep Agents' virtual filesystem capabilities.

The agent can:

- Read files
- Write files
- Edit files
- Search directories
- Generate temporary working files

Generated files are displayed directly inside the Streamlit interface.

---

### 🔍 Agent Transparency

Unlike a traditional chatbot, the application exposes the agent's internal workflow, including:

- Planning
- Tool calls
- Internet searches
- Subagent delegation
- File operations
- Tool outputs

This makes the project useful for both learning and debugging agentic workflows.

---

## 🖥️ Streamlit Interface

The UI allows you to configure the agent without changing any code.

Available options include:

- LLM Provider / Model
- Storage Backend
- AGENTS.md Context
- Skills
- Subagents
- Custom System Prompt
- Conversation Threads

---

## 🏗️ Tech Stack

- Python
- Deep Agents
- LangGraph
- LangChain
- Streamlit
- OpenAI
- Groq
- Tavily Search
- Pydantic

---

## 📁 Project Structure

```
.
├── streamlit_app.py          # Interactive Streamlit application
├── main.py
├── pyproject.toml
├── requirements.txt
├── .env
└── deepagentsdemo/
    ├── notebooks/
    ├── skills/
    ├── projects/
    └── ...
```

> The `deepagentsdemo` directory contains the notebooks and custom skills used to demonstrate Deep Agents features. These notebooks are not included in this repository.

---

## ⚙️ Installation

Clone the repository.

```bash
git clone https://github.com/<your-username>/<your-repository>.git
cd <your-repository>
```

Install dependencies.

```bash
pip install -r requirements.txt
```

Create a `.env` file.

```env
OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

Run the application.

```bash
streamlit run streamlit_app.py
```

---

## 💡 What This Project Demonstrates

This project showcases many of the core concepts behind modern agentic AI systems.

- Autonomous task planning
- Context engineering
- Tool calling
- Internet research
- Conversation memory
- Multi-agent delegation
- Structured outputs
- Multiple storage backends
- Virtual file systems
- Reusable skills
- Human-readable execution traces

---

## 📌 Future Improvements

Potential extensions include:

- Additional LLM providers
- More reusable skills
- Vector database integration
- Human-in-the-loop approval workflows
- Multi-agent collaboration
- Authentication and deployment support

---

## ⭐ Acknowledgements

This project was built to explore the capabilities of the **Deep Agents** framework along with **LangGraph**, **LangChain**, and modern LLM-powered agent architectures.

If you found this project useful, consider giving the repository a ⭐.
