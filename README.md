# LangChain from Scratch

A structured, step-by-step learning journey through LangChain and LangGraph, built on top of [ai-agents-from-scratch](https://github.com/zara-shahid/ai-agents-from-scratch). Every notebook is rewritten using **Groq + LLaMA 3.3-70B** and **free HuggingFace embeddings** as a deliberate alternative to OpenAI.

> This repo is Phase 2 of my AI Agents learning journey. Phase 1 (building agents from scratch without any framework) lives in [ai-agents-from-scratch](https://github.com/zara-shahid/ai-agents-from-scratch).

---

## Stack

- **LLM:** `llama-3.3-70b-versatile` via [Groq](https://groq.com/) (free tier)
- **Framework:** LangChain + LangGraph
- **Embeddings:** `all-MiniLM-L6-v2` via HuggingFaceEmbeddings (free, local)
- **Vector Store:** ChromaDB
- **Environment:** Python + Jupyter Notebooks

---

## Repo Structure

```
langchain-from-scratch/
│
├── step-01-basics-and-lcel/
│   └── basics_and_lcel.ipynb
│
├── step-02-memory-conversation-chains/
│   └── memory_conversation_chains.ipynb
│
├── step-03-tools-and-agents/
│   └── tools_and_agents.ipynb
│
├── step-04-rag/
│   └── rag.ipynb
│
├── step-05-langgraph/
│   └── langgraph_agents.ipynb
│
└── README.md
```

---

## Learning Path

| Step | Topic | Key Concepts |
|------|-------|-------------|
| 01 | Basics & LCEL | ChatGroq, ChatPromptTemplate, StrOutputParser, pipe syntax, .invoke() .stream() .batch(), RunnablePassthrough, RunnableLambda |
| 02 | Memory & Conversation Chains | RunnableWithMessageHistory, InMemoryChatMessageHistory, MessagesPlaceholder, session-based memory, ConversationBufferMemory, ConversationBufferWindowMemory |
| 03 | Tools & Agents | @tool decorator, bind_tools(), create_tool_calling_agent, AgentExecutor, agent_scratchpad, multi-tool agents |
| 04 | RAG | WebBaseLoader, RecursiveCharacterTextSplitter, HuggingFaceEmbeddings, Chroma, create_retrieval_chain, create_stuff_documents_chain |
| 05 | LangGraph | StateGraph, TypedDict state, nodes, fixed and conditional edges, ToolNode, ReAct agent pattern, InMemorySaver checkpointer |

---

## Setup

**1. Clone the repo**
```bash
git clone https://github.com/zara-shahid/langchain-from-scratch.git
cd langchain-from-scratch
```

**2. Install dependencies**
```bash
pip install langchain langchain-groq langchain-community langgraph chromadb sentence-transformers python-dotenv
```

**3. Set up your `.env` file**
```
GROQ_API_KEY=your_groq_api_key_here
```

Get a free Groq API key at [console.groq.com](https://console.groq.com).

**4. Run any notebook**
```bash
jupyter notebook
```

---

## Key Design Decisions

**Groq instead of OpenAI** -- `llama-3.3-70b-versatile` via Groq is used throughout instead of GPT models. This keeps the entire repo free to run with no paid API keys required.

**HuggingFace embeddings instead of OpenAI embeddings** -- `all-MiniLM-L6-v2` runs locally and requires no API key, making Step 4 (RAG) fully free to run.

**Modern patterns only** -- All notebooks use the current LangChain v0.3+ patterns. Deprecated classes like `ConversationChain`, `ConversationBufferMemory`, and `initialize_agent` are not used anywhere.

---

## Resources Used

| Step | Resource |
|------|----------|
| 01 | [Greg Kamradt LangChain Tutorials](https://github.com/gkamradt/langchain-tutorials) |
| 02 | [Aurelio AI -- Conversational Memory](https://www.aurelio.ai/learn/langchain-conversational-memory) |
| 03 | [Aurelio AI -- Agents Intro](https://www.aurelio.ai/learn/langchain-agents-intro) |
| 04 | [LangChain Official Docs -- RAG Tutorial](https://python.langchain.com/docs/tutorials/rag/) |
| 05 | [DataCamp -- LangGraph Agents](https://www.datacamp.com/tutorial/langgraph-agents) |

---

## Related

- [ai-agents-from-scratch](https://github.com/zara-shahid/ai-agents-from-scratch) -- Phase 1: building LLM tools, RAG, and agents without any framework
- [LinkedIn](https://linkedin.com/in/zarashahid123)
