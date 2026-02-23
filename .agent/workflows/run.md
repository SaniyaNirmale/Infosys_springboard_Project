---
description: Run the LangGraph development server
---

## Steps

// turbo
1. Start the LangGraph dev server:
```
uvx --from "langgraph-cli[inmem]" --with-editable . --python 3.11 langgraph dev --host 127.0.0.1 --port 2024 --allow-blocking
```

2. Open LangSmith Studio in your browser:
   - URL: https://smith.langchain.com/studio/?baseUrl=http://127.0.0.1:2024
   - If this is your first time connecting, click "Add to allowed domains" when prompted

## Notes
- The server auto-reloads when source files change
- All 7 graphs are available: `scope_research`, `research_agent`, `research_agent_mcp`, `research_agent_supervisor`, `research_agent_full`, `learning_agent`, `deep_researcher`
- Tool-calling models use `groq:openai/gpt-oss-20b`
- Text-only models use `groq:llama-3.3-70b-versatile`
