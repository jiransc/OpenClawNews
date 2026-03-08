# 🧠 Dynamic Context & Thinking Levels (The Cost Cutter)

> **Warning**: These settings are powerful. Use with care.

---

## 💸 Thinking Levels (省钱秘籍)

### Low Budget Config (穷鬼模式)
Don't use GPT-4 for "Hi". Use cheaper models for default tasks.

`openclaw.json`:
```json
"thinking": {
  "default": "low",    // Haiku / Gemini Flash (Cheap)
  "code": "high",      // Opus / GPT-4 (Expensive but smart)
  "creative": "medium" // Sonnet (Balanced)
}
```
*   **Effect**: 50% API Cost Reduction.

---

## 🧠 Dynamic Context (Context Window Magic)

### Auto-Scaling (自动伸缩)
Keep context small for chats, but allow it to grow for big tasks.

`openclaw.json`:
```json
"llm": {
  "context_limit": 8000,   // Watermark (Default)
  "provider_config": {
    "num_ctx": 32000       // Max Ceiling (Ollama)
  }
}
```
*   **Effect**: Fast response usually, but handles 100-page PDF when needed.

---

## 🤖 Agent Orchestration (多特工协同)

### The "Company" Setup (老板模式)
Create a `manager` agent that delegates tasks.

`workspace/agents.json`:
```json
{
  "manager": {
    "role": "Product Manager",
    "skills": ["subagents"],  // Can spawn others
    "prompt": "Break down tasks for Coder and Reviewer."
  },
  "coder": {
    "role": "Senior Dev",
    "skills": ["exec", "git"],
    "prompt": "Write code only. No fluff."
  },
  "reviewer": {
    "role": "QA Lead",
    "skills": ["read", "web_search"],
    "prompt": "Find bugs and security holes."
  }
}
```
*   **Result**: You talk to Manager. They do the work. You profit.
