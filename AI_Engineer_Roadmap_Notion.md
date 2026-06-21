# 🤖 AI Engineer Roadmap — From Full Stack JS Dev to Intermediate AI Engineer

> **Your Profile:** Full Stack JavaScript Engineer (React, Next.js, NestJS, Node.js)
> **Target:** Intermediate AI Engineer — Interview-ready, Job-ready, Product-building capable
> **Time Budget:** 3 hrs/weekday × 5 = 15 hrs/week + 6 hrs/weekend day × 2 = 12 hrs → **~27 hrs/week**
> **Estimated Duration:** 5–6 months to intermediate level
> **Language Stack:** TypeScript/JavaScript first — Python as secondary

---

## 📋 Table of Contents

1. [Why You're Already Ahead](#why-youre-already-ahead)
2. [Roadmap Overview](#roadmap-overview)
3. [Phase 1 — AI Foundations + LLM Basics (Weeks 1–3)](#phase-1)
4. [Phase 2 — Prompt Engineering + APIs Mastery (Weeks 4–6)](#phase-2)
5. [Phase 3 — RAG + Vector Databases + Embeddings (Weeks 7–10)](#phase-3)
6. [Phase 4 — AI Agents + Harness Engineering (Weeks 11–14)](#phase-4)
7. [Phase 5 — Backend + System Design for AI (Weeks 15–17)](#phase-5)
8. [Phase 6 — SaaS AI Integration + Business of AI (Weeks 18–20)](#phase-6)
9. [Phase 7 — Portfolio Projects (Weeks 21–24)](#phase-7)
10. [Interview Prep](#interview-prep)
11. [Resources Master List](#resources-master-list)
12. [Weekly Schedule Template](#weekly-schedule-template)

---

## 🚀 Why You're Already Ahead {#why-youre-already-ahead}

| Your Existing Skill | AI Engineering Equivalent | Gap |
|---|---|---|
| React / Next.js | AI Chat UIs, Streaming responses, Agent frontends | Small — add AI SDK patterns |
| NestJS / Node.js | LLM API integrations, AI microservices, webhook handlers | Small — add LLM client libs |
| REST API design | Tool calling, Function calling, API chains | Small — extend existing knowledge |
| MySQL + Backend | Vector DB concepts, structured + unstructured data | Medium — new paradigm |
| System Design | AI system design (context windows, rate limits, cost) | Medium — AI-specific patterns |

**Your secret weapon:** Most AI Engineer courses are Python-first. You'll build in TypeScript/JavaScript — which is increasingly preferred for production AI apps and Next.js AI products. This is a hiring differentiator.

---

## 🗺️ Roadmap Overview {#roadmap-overview}

```
PHASE 1 (Wk 1–3)     → AI Foundations + LLM Mental Models
PHASE 2 (Wk 4–6)     → Prompt Engineering + OpenAI/Anthropic APIs  
PHASE 3 (Wk 7–10)    → RAG + Embeddings + Vector DBs
PHASE 4 (Wk 11–14)   → AI Agents + Harness Engineering (LangChain/LangGraph)
PHASE 5 (Wk 15–17)   → Backend/MySQL for AI + System Design
PHASE 6 (Wk 18–20)   → SaaS AI + Business of AI
PHASE 7 (Wk 21–24)   → 3 Portfolio Projects + Interview Prep
```

---

## Phase 1 — AI Foundations + LLM Basics {#phase-1}
**Weeks 1–3 | ~81 hrs**

### 🎯 Goal
Understand what LLMs are, how they work at a conceptual level, and the AI Engineer's role vs ML Engineer.

### 📚 Topics

#### 1.1 What is an AI Engineer (vs ML Engineer)?
- AI Engineers use **pre-trained models** to solve product problems — they don't train from scratch
- Your job: integrate, orchestrate, evaluate, and ship AI systems
- ML Engineer: trains and fine-tunes models, heavy math/Python
- You are building the **application layer** on top of models

#### 1.2 LLM Core Concepts
- **Tokens** — what they are, how pricing works, how context windows work
- **Inference** — how a model generates text (autoregressive, temperature, top-p)
- **Training vs Fine-tuning** — conceptual understanding only
- **Embeddings** — turning text into numbers (vectors)
- **Context Window** — GPT-4o: 128k, Claude 3.5: 200k — why this matters for product design
- **Cut-off Dates + Knowledge limits** — how to work around them (RAG, tools)

#### 1.3 Popular Models — Know These Cold
| Provider | Model | Best For |
|---|---|---|
| OpenAI | GPT-4o, o1, o3-mini | General, reasoning, vision |
| Anthropic | Claude 3.5 Sonnet, Claude 3 Haiku | Long context, coding, safety |
| Google | Gemini 1.5 Pro | Multimodal, long doc |
| Meta (Open) | Llama 3.1, Llama 3.3 | Self-hosted, privacy |
| Mistral | Mistral Large | EU-based, open |

#### 1.4 AI Safety + Ethics Basics
- Prompt injection attacks
- Bias and fairness in outputs
- Hallucinations — what they are, how to mitigate
- When NOT to use AI (medical/legal decisions without review)

#### 1.5 Common Terminology Cheat Sheet
- Temperature, Top-p, Top-k
- System prompt, User prompt, Assistant turn
- Few-shot, Zero-shot, Chain of Thought
- RAG, Agent, Tool, Function call
- Hallucination, Grounding, Latency, Throughput

### 📖 Resources

**Read First:**
- 📄 [What is an AI Engineer? — roadmap.sh](https://roadmap.sh/ai-engineer) — skim the full roadmap
- 📄 [AI Engineer vs ML Engineer — DEV.to](https://dev.to/roadmapsh/ai-engineer-roadmap-3n8)
- 📺 [Andrej Karpathy — Intro to LLMs (1 hr)](https://www.youtube.com/watch?v=zjkBMFhNj_g) — **MUST WATCH**
- 📺 [What are Tokens? — 3Blue1Brown Neural Networks series](https://www.youtube.com/watch?v=aircAruvnKk) — optional but builds great intuition

**Books (pick one, skim-read Ch 1–3):**
- 📘 *Designing Machine Learning Systems* — Chip Huyen (Ch 1–2 only for now)
- 📘 *AI Engineering* — Chip Huyen (2024, newest, directly on-topic)

**Hands-on:**
- 🔧 Create OpenAI account + get API key
- 🔧 Create Anthropic account + get API key  
- 🔧 Play in [OpenAI Playground](https://platform.openai.com/playground) — try different models/temperatures
- 🔧 Play in [Claude.ai](https://claude.ai) — notice context window behavior

### ✅ Phase 1 Checklist
- [ ] Can explain tokens, context window, temperature to a non-technical person
- [ ] Know the difference between AI Engineer and ML Engineer
- [ ] Have working API keys for OpenAI and Anthropic
- [ ] Made at least 10 API calls manually via Playground

---

## Phase 2 — Prompt Engineering + APIs Mastery {#phase-2}
**Weeks 4–6 | ~81 hrs**

### 🎯 Goal
Write production-grade prompts. Build your first real API integrations in TypeScript. Understand token management and cost.

### 📚 Topics

#### 2.1 Prompt Engineering Fundamentals
- **Zero-shot prompting** — just ask
- **Few-shot prompting** — give examples in the prompt
- **Chain of Thought (CoT)** — "think step by step"
- **System prompt design** — persona, constraints, output format
- **ReAct prompting** — Reasoning + Acting (used in agents)
- **Structured output** — JSON mode, function calling schemas
- **Prompt injection defense** — sanitizing user input

#### 2.2 OpenAI API (TypeScript)
```typescript
// Basic Chat Completion
import OpenAI from 'openai';
const client = new OpenAI({ apiKey: process.env.OPENAI_API_KEY });

const response = await client.chat.completions.create({
  model: 'gpt-4o',
  messages: [
    { role: 'system', content: 'You are a helpful assistant.' },
    { role: 'user', content: 'Explain RAG in simple terms.' }
  ],
  temperature: 0.7,
  max_tokens: 500
});
```

#### 2.3 Anthropic Claude API (TypeScript)
```typescript
import Anthropic from '@anthropic-ai/sdk';
const client = new Anthropic({ apiKey: process.env.ANTHROPIC_API_KEY });

const message = await client.messages.create({
  model: 'claude-sonnet-4-6',
  max_tokens: 1024,
  messages: [{ role: 'user', content: 'Hello Claude.' }]
});
```

#### 2.4 Streaming Responses (critical for UX)
- Why streaming matters: first token in <1s vs waiting 10s for full response
- How to stream with OpenAI SDK in Next.js (Vercel AI SDK)
- How to handle streaming in NestJS (SSE / EventSource)

#### 2.5 Token Management
- Count tokens before sending (tiktoken for OpenAI)
- Truncate conversation history intelligently
- Cost calculation: input tokens × price + output tokens × price
- Model selection by use case (cheap fast Haiku vs powerful Opus)

#### 2.6 Function Calling / Tool Use
- Define a tool schema (JSON Schema)
- Model decides when to call a tool
- Your code executes the tool and returns results
- This is the foundation of agents

```typescript
// Function Calling Example
const tools = [{
  type: 'function',
  function: {
    name: 'get_weather',
    description: 'Get current weather for a city',
    parameters: {
      type: 'object',
      properties: {
        city: { type: 'string', description: 'City name' }
      },
      required: ['city']
    }
  }
}];
```

### 📖 Resources

**Prompt Engineering:**
- 📄 [OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering) — official, must read
- 📄 [Anthropic Prompt Engineering Docs](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) — excellent for Claude
- 📺 [Advanced Prompt Engineering — Lilian Weng blog](https://lilianweng.github.io/posts/2023-03-15-prompt-engineering/)

**TypeScript API:**
- 📺 [Vercel AI SDK Crash Course — YouTube](https://www.youtube.com/watch?v=O9HSBP0bHNI) — best for Next.js integration
- 📄 [Vercel AI SDK Docs](https://sdk.vercel.ai/docs) — if you use Next.js, use this SDK
- 📺 [LangChain.js for Beginners — Microsoft GitHub](https://developer.microsoft.com/blog/langchainjs-for-beginners)

**Courses:**
- 🎓 [DeepLearning.ai — ChatGPT Prompt Engineering for Developers](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) — FREE, 2 hrs
- 🎓 [DeepLearning.ai — Building Systems with ChatGPT API](https://www.deeplearning.ai/short-courses/building-systems-with-chatgpt/) — FREE

**Prompt Reference:**
```
# Prompt Template for Production Use

System: You are [ROLE]. You [CONSTRAINTS].
Always respond in [FORMAT].
Never [GUARDRAILS].

Context: [RELEVANT BACKGROUND]

Task: [SPECIFIC INSTRUCTION]

Output Format:
{
  "result": "...",
  "confidence": "high|medium|low",
  "sources": []
}
```

### ✅ Phase 2 Checklist
- [ ] Can write zero-shot, few-shot, CoT prompts
- [ ] Built a streaming chat API endpoint in NestJS
- [ ] Built a chat UI in Next.js with streaming
- [ ] Implemented function calling for at least one use case
- [ ] Can calculate API costs for a given use case

---

## Phase 3 — RAG + Embeddings + Vector Databases {#phase-3}
**Weeks 7–10 | ~108 hrs**

### 🎯 Goal
Build Retrieval-Augmented Generation systems. This is the most marketable intermediate skill. Every SaaS company wants "chat with your data."

### 📚 Topics

#### 3.1 What are Embeddings?
- Text → vector (array of numbers like `[0.23, -0.11, 0.85, ...]`)
- Similar meaning = similar vector direction (cosine similarity)
- Used for: semantic search, recommendation, classification, anomaly detection
- Embedding model ≠ language model (different models)

#### 3.2 OpenAI Embeddings API
```typescript
const response = await client.embeddings.create({
  model: 'text-embedding-3-small', // cheaper, good quality
  input: 'Your text here'
});
const vector = response.data[0].embedding; // array of 1536 floats
```

#### 3.3 RAG Architecture (The Full Pipeline)
```
Documents → Chunking → Embedding → Vector DB (index)
                                         ↓
User Query → Embed Query → Similarity Search → Retrieve Top-K Chunks
                                                      ↓
                                          LLM + System Prompt + Chunks → Answer
```

**Chunking Strategies:**
- Fixed-size chunking (by characters)
- Sentence-aware chunking (split on sentence boundaries)
- Semantic chunking (split by topic shift)
- Overlap chunking (e.g., 100 char overlap between chunks)

**Retrieval Strategies:**
- Top-K similarity search
- Hybrid search (keyword + semantic)
- Reranking (use a reranker model to re-score results)
- Metadata filtering (filter by date, source, etc.)

#### 3.4 Vector Databases — Pick One
| DB | Best For | Free Tier | TypeScript SDK |
|---|---|---|---|
| **Pinecone** | Managed, production | Yes | Yes |
| **Supabase pgvector** | If using Postgres already | Yes | Yes |
| **Chroma** | Local development | N/A (open source) | Yes |
| **Qdrant** | Self-hosted, fast | Yes | Yes |
| **Weaviate** | Complex queries, multi-modal | Yes | Yes |

**Recommendation for you:** Start with **Chroma** locally, then **Supabase pgvector** for production (you likely know Postgres, and pgvector adds vectors to regular SQL tables — minimal new infrastructure).

#### 3.5 RAG vs Fine-tuning Decision Framework
| Use RAG When | Fine-tune When |
|---|---|
| Data changes frequently | Data is static and large |
| Need source citations | Need specific output style/format |
| Privacy sensitive data | Core task competence improvement |
| Budget limited | Have training data + budget |

#### 3.6 LlamaIndex + LangChain.js for RAG

**LangChain.js RAG pattern:**
```typescript
import { OpenAIEmbeddings } from '@langchain/openai';
import { Chroma } from '@langchain/community/vectorstores/chroma';
import { ChatOpenAI } from '@langchain/openai';
import { RetrievalQAChain } from 'langchain/chains';

// Ingest
const vectorStore = await Chroma.fromDocuments(docs, new OpenAIEmbeddings());

// Query
const chain = RetrievalQAChain.fromLLM(
  new ChatOpenAI({ model: 'gpt-4o' }),
  vectorStore.asRetriever({ k: 4 })
);
const answer = await chain.call({ query: 'What is the refund policy?' });
```

### 📖 Resources

**Core Understanding:**
- 📺 [RAG from Scratch — LangChain YouTube series (free)](https://youtube.com/playlist?list=PLfaIDFEXuae2LXbO1_PKyVJiQ23ZztA0x)
- 📄 [RAG vs Fine-tuning — Pinecone Blog](https://www.pinecone.io/learn/rag-vs-fine-tuning/)
- 📄 [Building RAG with TypeScript — Medium article](https://medium.com/@anoopp998/building-a-rag-application-using-langchain-and-typescript-4a2fd3def04e)

**Courses:**
- 🎓 [DeepLearning.ai — Building and Evaluating Advanced RAG](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/) — FREE
- 🎓 [LangChain.js for Beginners — Microsoft (GitHub free course)](https://github.com/microsoft/langchainjs-for-beginners) — **TypeScript, FREE**
- 🎓 [Udemy — GenAI LangChain for JavaScript Developers](https://www.udemy.com/course/genai-langchain-for-javascript-developers/) — paid

**Hands-on Projects This Phase:**
- 🔧 Build a "Chat with PDF" app (NestJS backend + Next.js frontend)
- 🔧 Build a semantic search over your own GitHub READMEs
- 🔧 Compare Chroma vs pgvector query performance

### ✅ Phase 3 Checklist
- [ ] Can explain RAG pipeline end-to-end in an interview
- [ ] Built at least one RAG app with a real document
- [ ] Understand chunking tradeoffs
- [ ] Know when to use RAG vs fine-tuning
- [ ] Can implement semantic search in TypeScript

---

## Phase 4 — AI Agents + Harness Engineering {#phase-4}
**Weeks 11–14 | ~108 hrs**

### 🎯 Goal
Build autonomous AI agents that can plan, use tools, and execute multi-step tasks. Harness Engineering = the infrastructure/orchestration layer that makes AI reliable.

### 📚 Topics

#### 4.1 What is an AI Agent?
- LLM + Tools + Memory + Loop
- Agent pattern: **Observe → Think → Act → Observe...**
- ReAct (Reasoning + Acting) is the core pattern
- Agents can call APIs, search the web, write files, query DBs

#### 4.2 Agent Components
| Component | What It Is | Example |
|---|---|---|
| **Brain** | LLM that decides | GPT-4o, Claude Sonnet |
| **Tools** | Functions agent can call | `search_web`, `query_db`, `send_email` |
| **Memory** | What agent remembers | Short-term (context), Long-term (vector store) |
| **Orchestrator** | Controls agent loop | LangGraph, custom loop |
| **Evaluator** | Judges output quality | LLM-as-judge, human feedback |

#### 4.3 Building Agents with LangChain.js

**Simple ReAct Agent:**
```typescript
import { AgentExecutor, createReactAgent } from 'langchain/agents';
import { TavilySearchResults } from '@langchain/community/tools/tavily_search';
import { ChatOpenAI } from '@langchain/openai';
import { pull } from 'langchain/hub';

const tools = [new TavilySearchResults({ maxResults: 3 })];
const llm = new ChatOpenAI({ model: 'gpt-4o', temperature: 0 });
const prompt = await pull('hwchase17/react');

const agent = await createReactAgent({ llm, tools, prompt });
const executor = new AgentExecutor({ agent, tools });

const result = await executor.invoke({
  input: 'What is the latest news about AI in India?'
});
```

#### 4.4 LangGraph (for Complex Agents)
- LangGraph = stateful, graph-based agent orchestration
- Use when you need: branching logic, loops, human-in-the-loop, multi-agent
- Key concepts: **Nodes** (functions), **Edges** (transitions), **State** (shared data)

```typescript
import { StateGraph, END } from '@langchain/langgraph';

const workflow = new StateGraph({ channels: { messages: { value: (x, y) => x.concat(y) } } })
  .addNode('agent', callModel)
  .addNode('tools', callTools)
  .addEdge('tools', 'agent')
  .addConditionalEdges('agent', shouldContinue, { continue: 'tools', end: END });
```

#### 4.5 Harness Engineering (Making AI Reliable in Production)
This is the skill that separates junior from senior AI Engineers.

**Evaluation:**
- LLM-as-judge: use an LLM to evaluate another LLM's output
- Golden dataset: curated question-answer pairs to test against
- Metrics: faithfulness, answer relevancy, context precision (RAGAs framework)

**Observability:**
- LangSmith (LangChain's tracing tool) — logs every agent step
- Helicone — cost tracking, logging for OpenAI calls
- OpenTelemetry + custom logging

**Reliability Patterns:**
- Retry with exponential backoff (OpenAI rate limits)
- Fallback models (GPT-4o fails → Claude as fallback)
- Output validation (Zod schema to validate LLM JSON responses)
- Cost guardrails (max token budget per user per day)

**Prompt Management:**
- Version your prompts like code (LangSmith Hub, Promptlayer)
- A/B test prompts in production
- Never hardcode prompts in code — store in DB or config

#### 4.6 MCP (Model Context Protocol)
- Anthropic's open standard for connecting AI to external services
- Think of it as: USB-C for AI tools
- Build MCP servers that expose your APIs to AI agents
- Increasingly required knowledge for 2025+ AI roles

### 📖 Resources

**Core:**
- 📺 [LangGraph Tutorial — LangChain YouTube](https://www.youtube.com/watch?v=R8KB-Zcynxc)
- 📄 [LangChain.js Agents Docs](https://js.langchain.com/docs/modules/agents/)
- 📄 [LangSmith Evaluation Guide](https://docs.smith.langchain.com/)

**Courses:**
- 🎓 [Udemy — Production AI Agents with JS: LangChain & LangGraph](https://www.udemy.com/course/production-ai-agents-with-javascript-langchain-langgraph/) — TypeScript, highly recommended
- 🎓 [DeepLearning.ai — AI Agents in LangGraph](https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/) — FREE
- 🎓 [DeepLearning.ai — Building Your Own Database Agent](https://www.deeplearning.ai/short-courses/building-your-own-database-agent/) — FREE

**Books:**
- 📘 *Prompt Engineering for LLMs* — John Berryman & Albert Webson (O'Reilly)

**Harness/Eval:**
- 📄 [RAGAs — RAG Evaluation Framework](https://docs.ragas.io/en/stable/)
- 📄 [Helicone Docs](https://docs.helicone.ai/)

### ✅ Phase 4 Checklist
- [ ] Built a multi-tool agent that can search + answer questions
- [ ] Set up LangSmith tracing on an agent
- [ ] Implemented output validation with Zod
- [ ] Understand LangGraph state management
- [ ] Can explain agent failure modes in an interview

---

## Phase 5 — Backend + MySQL for AI + System Design {#phase-5}
**Weeks 15–17 | ~81 hrs**

### 🎯 Goal
Design AI systems at scale. Know how to architect an AI feature into an existing product. MySQL + AI integration patterns.

### 📚 Topics

#### 5.1 MySQL for AI Systems
- **Structured data + AI**: Use MySQL for metadata, user data, audit logs
- **pgvector in Postgres** (or MySQL 9's built-in vector type) for hybrid storage
- **Conversation history storage** — store chat history in MySQL, retrieve by session ID
- **Prompt logging** — always log prompts + responses for debugging + compliance

```sql
-- Conversation history table
CREATE TABLE ai_conversations (
  id VARCHAR(36) PRIMARY KEY,
  user_id VARCHAR(36) NOT NULL,
  session_id VARCHAR(36) NOT NULL,
  role ENUM('user', 'assistant', 'system') NOT NULL,
  content TEXT NOT NULL,
  model VARCHAR(50),
  tokens_used INT,
  cost_usd DECIMAL(10,6),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  INDEX idx_session (session_id),
  INDEX idx_user (user_id)
);
```

#### 5.2 AI System Design Patterns

**Pattern 1: Chat with Knowledge Base**
```
User → Next.js → NestJS API → [RAG Pipeline] → LLM → Streaming Response
                     ↓
              [MySQL: log conversation]
              [Pinecone: semantic search]
```

**Pattern 2: Async AI Processing (for long tasks)**
```
User submits task → NestJS → Queue (BullMQ/Redis) → Worker → AI Processing → Webhook/Polling
```

**Pattern 3: AI Gateway (for multiple models)**
```
Client → AI Gateway (NestJS) → Route by: cost/latency/capability → OpenAI | Claude | Llama
                             → Log all calls → MySQL
                             → Cache common queries → Redis
```

#### 5.3 Performance + Cost Optimization
- **Caching**: Cache identical prompts (Redis) — 60-70% of LLM calls in production are duplicates
- **Model routing**: Use cheap models (Haiku, GPT-4o-mini) for simple tasks, expensive for complex
- **Batch processing**: Embeddings can be batched (100 texts per call)
- **Streaming**: Always stream for user-facing features (reduces perceived latency)
- **Context pruning**: Remove old messages beyond recent N turns

#### 5.4 AI System Design Interview Topics
- How would you build a "chat with documents" feature for 1M users?
- How do you handle LLM rate limits in production?
- How do you ensure data privacy when using third-party LLM APIs?
- How do you evaluate output quality at scale?
- How do you handle prompt injection in a multi-tenant SaaS?

#### 5.5 Security for AI Systems
- **Prompt injection**: User input that overrides system prompt
- **Data leakage**: PII in prompts going to external APIs (use Azure OpenAI for GDPR compliance)
- **Output sanitization**: Never render raw LLM output as HTML (XSS risk)
- **Rate limiting**: Per-user AI usage limits
- **Audit logging**: GDPR requires logging who accessed what

### 📖 Resources

- 📺 [System Design for AI Applications — Chip Huyen talk](https://www.youtube.com/watch?v=wh5REdBlKOc)
- 📘 *Designing Machine Learning Systems* — Chip Huyen (Ch 3, 7, 10)
- 📄 [LLM App Deployment Patterns — a16z blog](https://a16z.com/emerging-architectures-for-llm-applications/)
- 📄 [NestJS + OpenAI Integration Guide](https://docs.nestjs.com/techniques/http-module) + official OpenAI SDK

### ✅ Phase 5 Checklist
- [ ] Designed a conversation history schema in MySQL
- [ ] Implemented Redis caching for LLM responses
- [ ] Can whiteboard an AI system design in 30 minutes
- [ ] Know 3+ AI security failure modes

---

## Phase 6 — SaaS AI Integration + Business of AI {#phase-6}
**Weeks 18–20 | ~81 hrs**

### 🎯 Goal
Understand how to add AI to existing SaaS products, how to manage AI as a business function, and how to communicate AI value to stakeholders.

### 📚 Topics

#### 6.1 How Existing SaaS Products Leverage AI
Every SaaS category has an AI opportunity:

| SaaS Category | AI Feature to Add |
|---|---|
| CRM | AI email composer, lead scoring, call summary |
| Project Management | Sprint planning assistant, auto-prioritization |
| HR / ATS | Resume screening, job description generator |
| E-commerce | Product description generator, chatbot support |
| Finance | Invoice extraction, anomaly detection |
| Healthcare | Note summarization, coding assistant |
| Education | Personalized quiz generator, essay feedback |

#### 6.2 AI Feature Prioritization Framework
Before building any AI feature, ask:
1. **Does AI solve a real user pain?** (not just "cool to have")
2. **What's the blast radius if AI is wrong?** (low risk: summarization; high risk: financial advice)
3. **Can we evaluate output quality systematically?**
4. **What's the cost per user per month?** (GPT-4o: ~$0.01-0.05 per interaction)
5. **Is latency acceptable?** (3-5s for AI responses is often OK if streamed)

#### 6.3 AI Product Patterns That Convert
- **"Ask anything" search** — replaces rigid filter-based search
- **Content generation** — emails, descriptions, reports
- **Document Q&A** — upload and chat with your own data
- **Smart notifications** — AI determines what to surface
- **Auto-classification** — tag, categorize, route incoming data
- **Summary + insights** — turn data into narrative

#### 6.4 Managing AI in Business
- **Make vs Buy**: OpenAI API vs self-hosted Llama (cost vs control vs compliance)
- **SLAs for AI**: Define acceptable hallucination rates, latency budgets
- **AI Governance**: Who approves prompt changes? How do you handle model deprecations?
- **Cost forecasting**: Token usage × price × growth projection
- **Stakeholder communication**: "AI confidence" vs "accuracy" terminology

#### 6.5 Prompt → Product Thinking
```
Problem Statement
→ What information does AI need? (context design)
→ What should AI output? (schema design)
→ What can go wrong? (failure mode analysis)
→ How do we evaluate? (success metrics)
→ How do we improve? (feedback loop design)
```

### 📖 Resources

- 📘 *The AI Product Manager's Handbook* — concept, read blog summaries
- 📺 [How to Build AI Products — Y Combinator talks (YouTube)](https://www.youtube.com/results?search_query=y+combinator+ai+product+2024)
- 📄 [a16z — The New Language Model Stack](https://a16z.com/emerging-architectures-for-llm-applications/)
- 📄 [Lenny's Newsletter — AI in Product Development](https://www.lennysnewsletter.com/)

### ✅ Phase 6 Checklist
- [ ] Can identify 3 AI features to add to any given SaaS
- [ ] Know how to estimate cost per user for an AI feature
- [ ] Can explain build vs buy tradeoffs for LLMs
- [ ] Built a simple AI feature addition to an existing Next.js project

---

## Phase 7 — Portfolio Projects {#phase-7}
**Weeks 21–24 | ~108 hrs**

### 🎯 Goal
3 projects that demonstrate the full AI Engineer skillset. Each project solves a real problem, is deployed, and is documented.

---

### 🏗️ Project 1: AI-Powered Document Intelligence SaaS
**Timeline: Weeks 21–22 | Demonstrates: RAG + Embeddings + Full Stack + SaaS**

**What it does:**
- Upload PDFs/docs → AI extracts, indexes, and enables natural language Q&A
- Multi-document support with source citations
- Chat history per user
- Usage tracking (tokens used, cost)

**Tech Stack:**
- Frontend: Next.js 14 (App Router) + Vercel AI SDK
- Backend: NestJS + MySQL (conversations, users) + Supabase pgvector (embeddings)
- AI: LangChain.js + OpenAI (embeddings + GPT-4o)
- Deployment: Vercel (frontend) + Railway/Render (backend)

**Key Features to Build:**
1. File upload → chunking → embedding → storage pipeline
2. Streaming Q&A with source citations
3. Conversation history (stored in MySQL)
4. Usage dashboard (tokens, cost per user)
5. Auth (NextAuth.js or Clerk)

**Interview Talking Points:**
- "I built a RAG pipeline handling [X] documents with [Y] chunks"
- "I optimized retrieval by implementing hybrid search"
- "I reduced cost by 40% by caching embeddings and using smaller models for simple queries"

---

### 🏗️ Project 2: AI Agent for SaaS Workflow Automation
**Timeline: Weeks 22–23 | Demonstrates: Agents + Tool Use + LangGraph + Harness Engineering**

**What it does:**
- Natural language → automated multi-step workflow
- Example: "Find all leads from India in my CRM who haven't been contacted in 30 days and draft personalized follow-up emails"
- Connects to: email API (Resend), mock CRM data (MySQL), web search (Tavily)

**Tech Stack:**
- Backend: NestJS + LangGraph.js
- LLM: Claude Sonnet (better for multi-step reasoning)
- Tools: MySQL query tool, email send tool, web search tool
- Observability: LangSmith
- Frontend: Next.js (simple chat interface)

**Key Features:**
1. Custom tool definitions (MySQL, Email, Search)
2. LangGraph state machine for multi-step execution
3. Human-in-the-loop checkpoint (confirm before sending emails)
4. Full audit log of agent actions (LangSmith + MySQL)
5. Error handling + retry logic

**Interview Talking Points:**
- "I implemented human-in-the-loop approval for high-risk actions"
- "I used LangSmith to trace and debug agent reasoning"
- "I handled 3 common failure modes: tool timeout, malformed output, context overflow"

---

### 🏗️ Project 3: AI Feature Addition to a Real SaaS App
**Timeline: Weeks 23–24 | Demonstrates: SaaS AI integration + Business thinking**

**Option A (if you have a side project or work project):**
Add an AI feature to an existing app. Examples:
- Add "smart search" to an e-commerce app (semantic product search)
- Add "AI writer" to a blog CMS
- Add "contract analyzer" to a legal document tool

**Option B (build a mini SaaS with AI core):**
**DevLog AI** — an AI-powered developer journal:
- Daily standup generator (summarizes your GitHub commits)
- Weekly progress report (turns notes into narrative)
- PR description auto-writer (from diff → description)
- Connects to GitHub API + LLM + Next.js

**Why this project:**
- Shows you understand AI ROI for businesses
- Shows product thinking not just engineering
- GitHub integration resonates with technical hiring managers

**Interview Talking Points:**
- "I integrated AI into an existing product with zero downtime"
- "I measured the impact: [metric] improved by [X] after adding AI feature"
- "I designed the feature with graceful degradation — if AI fails, user experience still works"

---

## 💼 Interview Prep {#interview-prep}

### Technical Questions You WILL Be Asked

**Conceptual:**
1. What is the difference between an AI Engineer and ML Engineer?
2. Explain RAG and when you'd use it vs fine-tuning
3. What is prompt injection and how do you prevent it?
4. How do you evaluate LLM output quality at scale?
5. Explain the agent loop (observe-think-act)
6. What is the context window and why does it matter for product design?
7. How do you handle LLM hallucinations in production?
8. Explain embeddings and why they're useful for search

**System Design:**
1. Design a "chat with your documents" feature for a SaaS with 100k users
2. Design a rate-limited AI API gateway
3. Design an evaluation system for an AI chatbot
4. How would you migrate from OpenAI to a self-hosted model?

**Coding:**
1. Implement a simple RAG pipeline from scratch (TypeScript)
2. Write a retry wrapper for LLM API calls with exponential backoff
3. Implement streaming chat completions in NestJS
4. Design a token counting middleware for an Express/NestJS app

### Your Answers Should Always Include
- The architecture you used
- A tradeoff you faced and why you chose your approach
- How you evaluated/measured success
- What you'd do differently or what's next

### Portfolio Presentation Tips
- GitHub README for each project: problem → solution → architecture diagram → demo link
- Deploy everything (Vercel + Railway free tiers work fine)
- Record a 2-min Loom walkthrough of each project
- Write a blog post (Dev.to or Hashnode) for at least one project

---

## 📚 Resources Master List {#resources-master-list}

### Free Courses (Do These)
| Course | Provider | Duration | Priority |
|---|---|---|---|
| [Prompt Engineering for Devs](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) | DeepLearning.ai | 2 hrs | 🔴 Must |
| [Building Systems with LLMs](https://www.deeplearning.ai/short-courses/building-systems-with-chatgpt/) | DeepLearning.ai | 3 hrs | 🔴 Must |
| [Building + Evaluating RAG](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/) | DeepLearning.ai | 3 hrs | 🔴 Must |
| [AI Agents in LangGraph](https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/) | DeepLearning.ai | 4 hrs | 🔴 Must |
| [LangChain.js for Beginners](https://github.com/microsoft/langchainjs-for-beginners) | Microsoft | 10 hrs | 🔴 Must |
| [Intro to LLMs — Karpathy](https://www.youtube.com/watch?v=zjkBMFhNj_g) | YouTube | 1 hr | 🔴 Must |

### Paid Courses (Worth It)
| Course | Platform | Cost | Why |
|---|---|---|---|
| [Production AI Agents with JS: LangChain & LangGraph](https://www.udemy.com/course/production-ai-agents-with-javascript-langchain-langgraph/) | Udemy | ~$15 | TypeScript-first, production patterns |
| [GenAI + LangChain for JS Developers](https://www.udemy.com/course/genai-langchain-for-javascript-developers/) | Udemy | ~$15 | JS/TS RAG course, updated Nov 2025 |

### Books
| Book | Author | Use |
|---|---|---|
| *AI Engineering* | Chip Huyen | Best overview of the field, 2024 |
| *Designing ML Systems* | Chip Huyen | System design foundation, Ch 1-3, 7, 10 |
| *Prompt Engineering for LLMs* | Berryman & Webson | Deep prompt engineering reference |

### Key Documentation
- [OpenAI API Docs](https://platform.openai.com/docs) — your daily reference
- [Anthropic Claude Docs](https://docs.anthropic.com) — prompt engineering is excellent here
- [LangChain.js Docs](https://js.langchain.com/docs) — agent + RAG patterns
- [Vercel AI SDK Docs](https://sdk.vercel.ai/docs) — Next.js streaming, best for your stack
- [LangSmith Docs](https://docs.smith.langchain.com) — observability

### Blogs to Follow
- [Lilian Weng (OpenAI)](https://lilianweng.github.io) — technical deep dives
- [Chip Huyen's Blog](https://huyenchip.com/blog/) — AI engineering perspective
- [Simon Willison's Blog](https://simonwillison.net/) — practical AI engineering
- [Eugene Yan's Blog](https://eugeneyan.com/) — applied ML/AI in production
- [The Batch — Andrew Ng](https://www.deeplearning.ai/the-batch/) — weekly AI news

### YouTube Channels
- [Andrej Karpathy](https://www.youtube.com/@AndrejKarpathy) — deep LLM understanding
- [LangChain Official](https://www.youtube.com/@LangChain) — framework tutorials
- [Matt Williams (Ollama)](https://www.youtube.com/@mattwilliams) — local models
- [Sam Witteveen](https://www.youtube.com/@samwitteveenai) — practical AI apps

---

## 📅 Weekly Schedule Template {#weekly-schedule-template}

### Weekday (3 hours/day)
```
6:00–7:00 PM  →  Learn (watch video / read docs / take notes)
7:00–8:30 PM  →  Build (hands-on coding / projects)
8:30–9:00 PM  →  Review + write notes in Notion
```

### Weekend (6+ hours/day)
```
Morning (3 hrs): Deep work on project or course
Afternoon (2 hrs): Research / read blog posts / watch longer content
Evening (1 hr): Write about what you learned (blog/notes) — this is how you solidify knowledge
```

### Monthly Milestones
| Month | Milestone |
|---|---|
| Month 1 | First LLM API call → First streaming chat UI live |
| Month 2 | First RAG app deployed ("chat with PDF") |
| Month 3 | First agent with 3+ tools working end-to-end |
| Month 4 | All system design patterns understood + MySQL AI schema |
| Month 5 | 3 portfolio projects deployed + documented |
| Month 6 | Interview prep complete → Applying for jobs |

---

## 🧠 Prompt Templates to Bookmark

### For Learning Any New AI Concept
```
I am a senior JavaScript/TypeScript engineer learning [TOPIC].
Explain [CONCEPT] to me as if I already know:
- React, Next.js, NestJS, Node.js
- REST APIs, MySQL
- Basic system design

Give me:
1. A one-paragraph mental model
2. A TypeScript code example
3. The most common mistake beginners make
4. When NOT to use this approach
```

### For Designing an AI Feature
```
I want to add an AI feature to a SaaS app with this description: [APP DESCRIPTION]

The feature I'm considering: [FEATURE IDEA]

Help me think through:
1. User pain this solves (is it real?)
2. Technical architecture (RAG? Agent? Simple completion?)
3. Failure modes and how to handle them
4. How to evaluate output quality
5. Cost estimate per user per month
6. What data I need to collect to improve it over time
```

### For Debugging an AI System
```
My AI system is producing bad outputs. Here is context:
- System prompt: [PROMPT]
- User input: [INPUT]
- Current output: [BAD OUTPUT]
- Expected output: [EXPECTED]

Diagnose the likely cause and suggest 3 specific fixes to my prompt.
Also suggest how I can test these fixes systematically.
```

### For System Design Interview Prep
```
Give me a mock AI system design interview question at the level of a 
mid-level AI Engineer (2-4 years). After I answer, evaluate my response 
on: completeness, technical depth, awareness of failure modes, and 
ability to communicate tradeoffs clearly.

Focus area: [RAG / Agents / Evaluation / Cost optimization]
```

---

## 🗓️ 24-Week Timeline at a Glance

| Week | Phase | Focus | Deliverable |
|---|---|---|---|
| 1–3 | Foundation | LLMs, models, tokens, ethics | ✅ API keys working, playground explored |
| 4–6 | Prompts + APIs | Prompt engineering, TypeScript APIs, streaming | ✅ Streaming chat endpoint in NestJS |
| 7–10 | RAG | Embeddings, chunking, vector DBs, LangChain.js | ✅ "Chat with PDF" mini-project |
| 11–14 | Agents | LangChain agents, LangGraph, harness/eval | ✅ Multi-tool agent with LangSmith tracing |
| 15–17 | Backend + System Design | MySQL for AI, caching, AI system patterns | ✅ System design diagram for portfolio |
| 18–20 | SaaS AI + Business | AI feature thinking, cost, governance | ✅ AI feature added to existing project |
| 21–22 | Project 1 | Document Intelligence SaaS | ✅ Deployed + documented |
| 22–23 | Project 2 | AI Workflow Automation Agent | ✅ Deployed + documented |
| 23–24 | Project 3 | SaaS AI Integration | ✅ Deployed + documented |
| 25–26 | Interview | System design mock, coding, portfolio polish | ✅ Interview-ready |

---

*Roadmap built for a Full Stack JS Engineer (React/Next.js/NestJS) targeting Intermediate AI Engineer. Updated June 2026.*
