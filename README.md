# Agentic Core  

### AI Agent Framework for Java

**Agentic Core** is a lightweight, modular framework for building **autonomous AI agents** in Java.  
It provides an extensible architecture for integrating LLMs, managing memory, and orchestrating tools — enabling developers to create intelligent, context-aware systems.

---

## Key Features

- **LangChain4j Integration**  
  Connect easily with LLMs using the LangChain4j ecosystem.

- **RAG (Retrieval-Augmented Generation)**  
  Built-in support for **Pinecone** and **Weaviate** vector stores.

- **Function Calling**  
  Unified interface for invoking functions across multiple LLM backends.

- **Memory Management**  
  Short-term and long-term memory components for contextual continuity.

- **Tool Orchestration**  
  Define, register, and compose tools dynamically for autonomous decision-making.

- **Real-time Communication**  
  WebSocket integration for streaming responses and agent interaction.

---

## Architecture Overview

```
Client ↔ WebSocket ↔ Agent Core ↔ Memory ↔ LLM ↔ Vector Store
```

- **Agent Core** – The orchestrator connecting tools, memory, and LLMs.  
- **Memory** – Manages state and contextual persistence.  
- **LLM** – Communicates through LangChain4j with supported providers.  
- **Vector Store** – Handles retrieval via Pinecone or Weaviate.

---

## Getting Started

### Requirements
- Java 17+
- Maven or Gradle
- Access to LLM API keys (e.g., OpenAI, Anthropic)

### Installation
```bash
git clone https://github.com/<your-org>/6-agentic-core.git
cd 6-agentic-core
mvn clean install
```

### Example Usage
```java
Agent agent = AgentBuilder.create()
    .withMemory(new LongTermMemory(...))
    .withLLM(new OpenAIModel(...))
    .withVectorStore(new PineconeStore(...))
    .build();

agent.run("Plan a trip to Tokyo for next week.");
```

---

## Roadmap

- [ ] Multi-agent collaboration  
- [ ] Improved memory persistence  
- [ ] REST API interface  
- [ ] Plugin system for custom tools  

---

## License

Distributed under the **MIT License**.  
See [`LICENSE`](./LICENSE) for details.

---

## Contributing

Contributions, issues, and feature requests are welcome!  
Please open a pull request or issue to discuss changes.

---

## Related Projects

- [LangChain4j](https://github.com/langchain4j/langchain4j)  
- [Pinecone](https://www.pinecone.io/)  
- [Weaviate](https://weaviate.io/)

---