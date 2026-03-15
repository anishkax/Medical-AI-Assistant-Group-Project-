Medical Research Assistant is a multi-agent system designed to answer complex medical queries with accuracy, depth, and up-to-date information. It achieves this by dynamically orchestrating specialized AI agents based on the user query and any subsequent feedback. This project is written in TypeScript, runs on Deno v2.1.6, and uses LangGraph for the agent workflow, LangChain for prompt-based pipelines, Ollama for local LLM usage, and Tavily for searching up-to-date medical sources.

Disclaimer The system is intended for research and educational purposes. Its outputs are not professional medical advice.

Key Components

LangGraph: Orchestrates the agents via a directed graph, allowing for conditional transitions (e.g., if a check fails, the flow returns to a previous node).
LangChain: Provides modular prompt templates and structured output parsing for each agent.
Deno v2.1.6: Offers native TypeScript support and built-in utilities (like streaming).
Groq Llama 3.3 70B (LLM): Used for orchestrating tasks, web search summarization, and final response compilation.
LightEternal-Llama3-Merge-Biomed-8B-GGUF:Q8_0 (Medical SLM): Used by the MedILlama Agent for domain-specific medical knowledge and by the Reflection Agent for quality checks.
Tavily: Web search API that retrieves and summarizes relevant, reputable medical information.
RAG Agent (Work in Progress): Will search research paper abstracts from PubMed, storing them in a vector DB for later retrieval and filtering.
