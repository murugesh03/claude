# 🧠 Claude — Full Feature Setup Guide
### Beginner to Super Advanced

> A complete reference for every surface of Claude: claude.ai, Claude Code, Claude API, MCP, and Agentic Workflows.

---

## Table of Contents

1. [What is Claude?](#what-is-claude)
2. [Plans & Access Tiers](#plans--access-tiers)
3. [Beginner — claude.ai Essentials](#beginner--claudeai-essentials)
4. [Intermediate — Power Features on claude.ai](#intermediate--power-features-on-claudeai)
5. [Advanced — Claude Code](#advanced--claude-code)
6. [Advanced — Claude API](#advanced--claude-api)
7. [Super Advanced — Extended Thinking & Tool Use](#super-advanced--extended-thinking--tool-use)
8. [Super Advanced — Agents & Agentic Workflows](#super-advanced--agents--agentic-workflows)
9. [Super Advanced — MCP (Model Context Protocol)](#super-advanced--mcp-model-context-protocol)
10. [Prompt Engineering Mastery](#prompt-engineering-mastery)
11. [Quick Reference Card](#quick-reference-card)

---

## What is Claude?

Claude is a family of AI models built by Anthropic, designed to be helpful, harmless, and honest. Unlike many AI tools, Claude is built with a Constitutional AI foundation — prioritizing safety, reasoning accuracy, and controllable behavior at every level.

### The Claude Ecosystem

| Surface | Who It's For | Access |
|---|---|---|
| **claude.ai** | Everyone — chat, projects, artifacts | Free / Paid plans |
| **Claude Code** | Developers — terminal & VS Code | Pro+ or API key |
| **Claude API** | Developers — integrate into apps | API key via console.anthropic.com |
| **Claude Agent SDK** | Engineers — build autonomous agents | API key |
| **AWS Bedrock / GCP Vertex** | Enterprise cloud teams | Cloud account |

### Current Model Family (2025–2026)

| Model | Best For | Context |
|---|---|---|
| **Claude Opus 4.6** | Most intelligent — coding, enterprise agents | 200K tokens |
| **Claude Sonnet 4.6** | Frontier intelligence at scale, coding & agents | 200K (1M beta) |
| **Claude Haiku 4.5** | Fastest, near-frontier, high-volume tasks | 200K tokens |

> **API model strings:** `claude-opus-4-6` · `claude-sonnet-4-6` · `claude-haiku-4-5-20251001`

---

## Plans & Access Tiers

### claude.ai Plans

| Feature | Free | Pro (~$17/mo) | Team | Enterprise |
|---|---|---|---|---|
| Access to Claude | ✅ | ✅ | ✅ | ✅ |
| Claude Sonnet & Haiku | ✅ | ✅ | ✅ | ✅ |
| Claude Opus | Limited | ✅ | ✅ | ✅ |
| Projects | ❌ | ✅ | ✅ | ✅ |
| Artifacts | ✅ | ✅ | ✅ | ✅ |
| Artifact persistent storage | ❌ | ✅ | ✅ | ✅ |
| MCP integrations | ❌ | ✅ | ✅ | ✅ |
| Claude Code | ❌ | ✅ | ✅ | ✅ |
| Extended Thinking | Limited | ✅ | ✅ | ✅ |
| Web search | ✅ | ✅ | ✅ | ✅ |
| Memory (cross-session) | Limited | ✅ | ✅ | ✅ |
| Admin controls | ❌ | ❌ | ✅ | ✅ |
| SSO / SCIM | ❌ | ❌ | ❌ | ✅ |
| Data residency | ❌ | ❌ | ❌ | ✅ |

---

## Beginner — claude.ai Essentials

### 1. Creating an Account

```
1. Go to https://claude.ai
2. Sign up with email, Google, or Apple
3. Choose Free plan to start
4. Optionally upgrade to Pro for higher limits and advanced features
```

### 2. Starting a Conversation

Just type naturally in the chat box. Claude understands context, nuance, and multi-part questions.

**Good first prompts to try:**

```
Explain React hooks like I'm a junior developer.
Write a professional email declining a meeting.
Summarize this article: [paste text]
Debug this code: [paste code]
Help me plan a workout routine for 3 days a week.
```

### 3. Attaching Files

Claude can read and analyze files you upload directly in chat.

**Supported file types:**
- PDFs, Word docs, text files
- Images (PNG, JPG, WEBP, GIF)
- CSV, code files
- Spreadsheets

**How to upload:**
```
Click the 📎 paperclip icon → Select file → Ask your question about it

Example: [upload resume.pdf] → "Rewrite this for a Senior Frontend Developer role"
Example: [upload screenshot.png] → "What's wrong with this UI layout?"
```

### 4. Selecting a Model

In the chat input area, click the model selector dropdown:

```
Claude Opus 4.6     → Most powerful, for complex/important tasks
Claude Sonnet 4.6   → Best balance (recommended default)
Claude Haiku 4.5    → Fastest, great for simple tasks
```

### 5. Chat History & Search

```
Left sidebar → All your past conversations
Search bar   → Search across all previous chats
Star ⭐       → Bookmark important conversations
```

### 6. Settings Panel

```
Profile icon (top right) → Settings

Key settings to configure:
- Appearance (dark/light mode)
- Language preference
- Memory (on/off)
- Notification preferences
- Feature flags (Artifacts, web search, etc.)
```

---

## Intermediate — Power Features on claude.ai

### 7. Artifacts

Artifacts are standalone outputs that render in a live panel beside your chat. They're not just text — they're editable, shareable, and interactive.

**What Artifacts can contain:**

| Type | Examples |
|---|---|
| **Code** | React components, Python scripts, HTML pages |
| **Markdown** | Reports, documentation, READMEs |
| **SVG** | Diagrams, icons, illustrations |
| **HTML** | Interactive web tools, forms, dashboards |
| **React** | Live UI components with state |
| **Mermaid** | Flowcharts, sequence diagrams |

**How to trigger Artifacts:**

```
Build me a React component for a user profile card.
Create an HTML dashboard with charts for sales data.
Generate an SVG diagram of the OAuth 2.0 flow.
Write a markdown report on Web3 trends.
Make an interactive quiz about JavaScript.
```

**Artifact Actions Panel:**

```
Preview   → See rendered output
Code      → See raw source
Copy      → Copy to clipboard
Download  → Save as file
Publish   → Generate a shareable public link
Remix     → Let others fork and modify
```

**Persistent Storage in Artifacts (Pro+):**

```javascript
// Artifacts on Pro+ can store and retrieve data across sessions
await window.storage.set('user-prefs', JSON.stringify(data));
const prefs = await window.storage.get('user-prefs');
```

### 8. Projects

Projects are persistent workspaces where Claude remembers your documents, instructions, and conversation history — solving the "cold start" problem.

**Setting up a Project:**

```
Left sidebar → "New Project" button
1. Name your project (e.g., "Frontend Dev Work")
2. Add project instructions (system prompt for the project)
3. Upload knowledge files (style guides, docs, codebase context)
4. Start conversations — Claude remembers everything across sessions
```

**Project Instructions example (for a developer):**

```
You are my senior frontend developer assistant.

Tech stack: React 18, TypeScript, Zustand, React Query, Tailwind CSS.
Always use functional components with hooks.
Prefer named exports. Always add TypeScript return types.
Use Zod for validation. Follow the project's ESLint config.
When writing tests, use Vitest + React Testing Library.
My codebase uses the feature-folder structure under src/features/.
```

**What to upload to a Project:**

```
✅ Your style guide or brand guidelines
✅ Architecture decision records (ADRs)
✅ API documentation
✅ Resume / portfolio (for career help)
✅ Previous Claude outputs you want to build on
✅ Company knowledge base exports
```

**Project organization tips:**

```
Create separate projects per domain:
  📁 "Client Work - ProjectX"
  📁 "Personal Dev — Side Projects"
  📁 "Job Search"
  📁 "Learning — AI Engineering"
  📁 "Finance & Budget"
```

### 9. Memory

Claude's memory system generates summaries from your past conversations and applies them to future chats — personalizing responses automatically.

**Enabling / Managing Memory:**

```
Settings → Feature Flags → Memory → Toggle ON

To view what Claude remembers:
Profile → "Memory" → Review stored facts

To add something:
"Remember that I prefer simplified code patterns in React."

To remove something:
"Forget what you know about my previous job."

To exclude a topic:
"Don't store anything about [topic] in your memory."
```

**Memory works best for:**

```
- Your tech stack preferences
- Communication style (formal vs casual)
- Recurring project context
- Personal preferences (diet, hobbies, goals)
- Career context (role, experience level)
```

> **Note:** Memory is disabled in Incognito mode and is separate from Project knowledge.

### 10. Web Search

Claude can search the web in real-time to answer questions about current events, prices, documentation, and more.

```
Settings → Feature Flags → Web Search → Toggle ON

Example prompts:
"What's the latest version of React Router?"
"Search for recent updates to the Anthropic API."
"Find pricing for AWS Lambda in Mumbai region."
"What's trending in AI engineering this week?"
```

### 11. Extended Thinking (Hybrid Reasoning)

Claude can switch between fast responses and deep step-by-step reasoning — controllable by you.

```
For complex prompts, trigger extended thinking:

"Think step by step before answering."
"Use extended thinking to solve this algorithm problem."
"Reason through all the trade-offs before recommending."

Best for:
- Architecture decisions
- Complex debugging
- Math and logic problems
- Legal, financial, or multi-constraint planning
- Competitive analysis
```

### 12. Deep Research Mode

On Pro+, Claude can conduct multi-step research across the web before synthesizing an answer.

```
"Use deep research to compare React state management libraries in 2025."
"Research the top 5 AI engineering roadmaps and compare them."
"Deep research: best practices for RAG pipeline optimization."
```

### 13. Voice Mode

Available in the Claude mobile app (iOS & Android):

```
Mobile App → Microphone icon → Speak your prompt
Supports: Real-time voice conversation, voice to text input
```

### 14. Claude in Chrome (Beta)

Claude can browse alongside you in Chrome and assist with what's on screen.

```
Install: Chrome Web Store → "Claude in Chrome"
Usage: Highlight text on any webpage → Ask Claude about it
       Summarize the current page
       Fill forms intelligently
       Draft replies to emails in Gmail
```

### 15. Sharing & Publishing

```
Individual conversation:
  Share icon → Generate a shareable link (read-only)

Artifacts:
  Artifact panel → Publish → Get public link
  Recipients don't need a Claude account to view

Projects (Team/Enterprise):
  Share project with team members
  Sharing stays within your organization
```

---

## Advanced — Claude Code

Claude Code is a terminal-native and VS Code-embedded agentic coding assistant that can read, edit, run, and reason about your entire codebase.

### 16. Installation

```bash
# Prerequisites: Node.js 18+, npm

# Install Claude Code globally
npm install -g @anthropic-ai/claude-code

# Authenticate (login on first run)
claude

# Verify
claude --version
```

**Alternative installs:**

```bash
# macOS via Homebrew
brew install claude-code

# Windows via WinGet
winget install Anthropic.ClaudeCode

# Note: Homebrew/WinGet do NOT auto-update
# Run: brew upgrade claude-code  OR  winget upgrade Anthropic.ClaudeCode
```

### 17. VS Code Extension

```
1. Open VS Code
2. Extensions panel (Cmd+Shift+X / Ctrl+Shift+X)
3. Search "Claude Code"
4. Install
5. Command Palette → "Claude Code: Open in New Tab"

Also works with: Cursor, JetBrains IDEs
```

### 18. Claude Code — Core Commands

```bash
# Start Claude Code in your project
cd my-project
claude

# Common in-session commands
/help                  → Show all slash commands
/init                  → Auto-generate CLAUDE.md for your project
/clear                 → Clear context and start fresh
/status                → Show current session info
/cost                  → Show token usage and cost for session
/model                 → Switch model mid-session
/permissions           → Review what Claude is allowed to do
/undo                  → Undo last file change
/diff                  → Show pending file changes
/review                → Ask Claude to review proposed changes
/pr_comments           → Fetch and address PR review comments
/release_notes         → Generate release notes from recent changes
/bug                   → Report a bug in Claude Code itself
/login                 → Switch accounts
/logout                → Log out
/exit or /quit         → End session
```

### 19. CLAUDE.md — Persistent Project Instructions

`CLAUDE.md` is the most powerful Claude Code feature. It's a Markdown file in your project root that Claude reads at the start of every session.

**Auto-generate it:**

```bash
/init
# Claude analyzes your codebase and creates CLAUDE.md automatically
```

**Manual CLAUDE.md example:**

```markdown
# Project: My SaaS App

## Stack
- Frontend: React 18, TypeScript, Vite
- State: Zustand
- Styling: Tailwind CSS
- Backend: Node.js + Express + MongoDB
- Testing: Vitest + React Testing Library

## Commands
- Dev server: `npm run dev`
- Tests: `npm test`
- Build: `npm run build`
- Lint: `npm run lint`
- Type check: `npm run typecheck`

## Coding Standards
- Functional components only, no class components
- Named exports over default exports
- Always add TypeScript return types
- Zod for all form and API validation
- React Query for all data fetching
- No direct DOM manipulation

## File Structure
src/
  features/        ← Feature-specific components, hooks, stores
  shared/          ← Reusable UI components
  services/        ← API calls
  store/           ← Global Zustand stores
  types/           ← Shared TypeScript types

## Review Checklist
Before committing:
1. Run tests and typecheck
2. No console.log in production code
3. Add JSDoc to all exported functions
4. Check for memory leaks in useEffect
```

**CLAUDE.md hierarchy:**

```
~/.claude/CLAUDE.md          → Global instructions (all projects)
~/projects/CLAUDE.md         → Folder-level instructions
~/projects/myapp/CLAUDE.md   → Project-level instructions (most specific)
```

### 20. Permission Modes

```bash
# Default: asks before every action
claude

# Auto-approve edits (still asks for commands)
claude --permission-mode acceptEdits

# Fully autonomous (use with caution)
claude --permission-mode autoApprove

# Read-only mode (no file changes)
claude --permission-mode bypassPermissions --read-only
```

### 21. Claude Code Power Workflows

```bash
# Explore and understand a new codebase
"Give me an architectural overview of this codebase."
"Map out the data flow from API call to UI render."
"Which files handle authentication?"

# Bug fixing
"Find and fix the null reference error in the cart module."
"Why does the pagination break on the last page?"

# Feature development
"Add dark mode support using Tailwind's dark: prefix."
"Build a reusable Modal component with accessibility support."

# Testing
"Write tests for all exported functions in src/utils/."
"Add edge case tests for the login form validation."

# Refactoring
"Refactor this class component to a functional component."
"Split this 400-line file into focused modules."
"Remove all circular dependencies from src/features/."

# Git workflow
"Write a commit message for these changes."
"Create a pull request description for this feature."
```

### 22. Custom Slash Commands

Create `.claude/commands/` in your project root:

```bash
mkdir -p .claude/commands

# Create a reusable command
cat > .claude/commands/review-pr.md << 'EOF'
Review the current git diff and:
1. Check for TypeScript errors
2. Look for missing error handling
3. Identify performance issues
4. Suggest test cases for new code
5. Write a PR description
EOF
```

Use it:

```
/project:review-pr
```

### 23. Hooks — Automation Triggers

Hooks let you run shell commands automatically before or after Claude Code actions.

```json
// .claude/settings.json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Edit",
        "hooks": [
          {
            "type": "command",
            "command": "npm run lint --fix && npm run typecheck"
          }
        ]
      }
    ],
    "PreToolUse": [
      {
        "matcher": "Bash",
        "hooks": [
          {
            "type": "command",
            "command": "echo 'About to run a bash command'"
          }
        ]
      }
    ]
  }
}
```

---

## Advanced — Claude API

### 24. API Setup

```bash
# Get your API key
# Go to: https://console.anthropic.com → API Keys → Create Key

# Store as environment variable
export ANTHROPIC_API_KEY="sk-ant-..."

# Install SDK
npm install @anthropic-ai/sdk        # Node.js
pip install anthropic                # Python
```

### 25. First API Call

```typescript
// TypeScript / Node.js
import Anthropic from "@anthropic-ai/sdk";

const client = new Anthropic(); // reads ANTHROPIC_API_KEY from env

const message = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 1024,
  messages: [{ role: "user", content: "Hello, Claude!" }],
});

console.log(message.content[0].text);
```

```python
# Python
import anthropic

client = anthropic.Anthropic()

message = client.messages.create(
    model="claude-sonnet-4-6",
    max_tokens=1024,
    messages=[{"role": "user", "content": "Hello, Claude!"}]
)

print(message.content[0].text)
```

### 26. System Prompts

```typescript
const response = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 1024,
  system: `You are a senior TypeScript developer. 
    Always return clean, well-typed code.
    Add JSDoc to exported functions.
    Prefer functional patterns over class-based.`,
  messages: [{ role: "user", content: "Write a debounce hook for React." }],
});
```

### 27. Multi-Turn Conversations

```typescript
const messages = [];

// Turn 1
messages.push({ role: "user", content: "What is React Query?" });
const response1 = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 1024,
  messages,
});
messages.push({ role: "assistant", content: response1.content[0].text });

// Turn 2
messages.push({ role: "user", content: "Show me a basic example." });
const response2 = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 1024,
  messages,
});
```

### 28. Streaming Responses

```typescript
const stream = client.messages.stream({
  model: "claude-sonnet-4-6",
  max_tokens: 1024,
  messages: [{ role: "user", content: "Write a detailed article on RAG." }],
});

for await (const chunk of stream) {
  if (chunk.type === "content_block_delta" && chunk.delta.type === "text_delta") {
    process.stdout.write(chunk.delta.text);
  }
}

const finalMessage = await stream.finalMessage();
console.log("\nTotal tokens:", finalMessage.usage.output_tokens);
```

### 29. Vision — Image Input

```typescript
import fs from "fs";

const imageData = fs.readFileSync("./screenshot.png").toString("base64");

const response = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 1024,
  messages: [
    {
      role: "user",
      content: [
        {
          type: "image",
          source: {
            type: "base64",
            media_type: "image/png",
            data: imageData,
          },
        },
        { type: "text", text: "What UI issues do you see in this screenshot?" },
      ],
    },
  ],
});
```

### 30. Tool Use (Function Calling)

```typescript
const tools = [
  {
    name: "get_weather",
    description: "Get current weather for a given city",
    input_schema: {
      type: "object",
      properties: {
        city: { type: "string", description: "City name" },
        unit: { type: "string", enum: ["celsius", "fahrenheit"] },
      },
      required: ["city"],
    },
  },
];

const response = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 1024,
  tools,
  messages: [{ role: "user", content: "What's the weather in Chennai?" }],
});

if (response.stop_reason === "tool_use") {
  const toolUse = response.content.find((b) => b.type === "tool_use");
  console.log("Claude wants to call:", toolUse.name);
  console.log("With inputs:", toolUse.input);

  // Execute the tool, then send result back
  const toolResult = { temperature: 34, condition: "Sunny" };

  const finalResponse = await client.messages.create({
    model: "claude-sonnet-4-6",
    max_tokens: 1024,
    tools,
    messages: [
      { role: "user", content: "What's the weather in Chennai?" },
      { role: "assistant", content: response.content },
      {
        role: "user",
        content: [
          {
            type: "tool_result",
            tool_use_id: toolUse.id,
            content: JSON.stringify(toolResult),
          },
        ],
      },
    ],
  });

  console.log(finalResponse.content[0].text);
}
```

### 31. Structured Outputs (JSON Mode)

```typescript
const response = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 1024,
  system: "Always respond with valid JSON only. No markdown, no explanation.",
  messages: [
    {
      role: "user",
      content: `Extract user info from: "Hi, I'm Murugesh, a frontend dev from Chennai."
      Return: { "name": string, "role": string, "city": string }`,
    },
  ],
});

const data = JSON.parse(response.content[0].text);
console.log(data); // { name: "Murugesh", role: "frontend dev", city: "Chennai" }
```

### 32. Prompt Caching (Performance & Cost)

Cache static parts of your prompt to dramatically reduce latency and cost on repeated calls.

```typescript
const response = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 1024,
  system: [
    {
      type: "text",
      text: "You are an expert React developer. Always use TypeScript...",
      cache_control: { type: "ephemeral" }, // cache this part
    },
  ],
  messages: [
    {
      role: "user",
      content: [
        {
          type: "text",
          text: largeCodebaseContext, // large, reused context
          cache_control: { type: "ephemeral" },
        },
        { type: "text", text: "Fix the bug in the auth module." },
      ],
    },
  ],
});

// cache_read_input_tokens vs cache_creation_input_tokens in usage
console.log(response.usage);
```

### 33. Batch API (Async Bulk Processing)

Process thousands of requests asynchronously at 50% cost:

```typescript
const batch = await client.messages.batches.create({
  requests: [
    {
      custom_id: "req-001",
      params: {
        model: "claude-sonnet-4-6",
        max_tokens: 1024,
        messages: [{ role: "user", content: "Summarize: [article 1]" }],
      },
    },
    {
      custom_id: "req-002",
      params: {
        model: "claude-sonnet-4-6",
        max_tokens: 1024,
        messages: [{ role: "user", content: "Summarize: [article 2]" }],
      },
    },
  ],
});

console.log("Batch ID:", batch.id);

// Poll for results
const result = await client.messages.batches.retrieve(batch.id);
console.log("Status:", result.processing_status); // "ended" when done
```

---

## Super Advanced — Extended Thinking & Tool Use

### 34. Extended Thinking via API

```typescript
const response = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 16000,
  thinking: {
    type: "enabled",
    budget_tokens: 10000, // how much thinking to allow
  },
  messages: [
    {
      role: "user",
      content: "Design a scalable multi-tenant SaaS architecture for a fintech app.",
    },
  ],
});

for (const block of response.content) {
  if (block.type === "thinking") {
    console.log("Claude's reasoning:\n", block.thinking);
  } else if (block.type === "text") {
    console.log("Final answer:\n", block.text);
  }
}
```

**When to use high thinking budgets:**

```
✅ Architecture design decisions
✅ Complex algorithm optimization
✅ Multi-constraint problem solving
✅ Security threat modeling
✅ Legal or financial analysis
✅ PhD-level reasoning tasks
```

### 35. Parallel Tool Use

Claude can call multiple tools simultaneously:

```typescript
// Claude may return multiple tool_use blocks in one response
const tools = [searchTool, calculatorTool, weatherTool];

const response = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 2048,
  tools,
  tool_choice: { type: "auto" }, // let Claude decide
  messages: [
    { role: "user", content: "Compare today's weather in Chennai vs Mumbai and calculate the temperature difference in Fahrenheit." },
  ],
});

// Handle multiple tool calls
const toolUseBlocks = response.content.filter((b) => b.type === "tool_use");
const results = await Promise.all(toolUseBlocks.map(executeToolCall));
```

### 36. Computer Use (Experimental)

Claude can control a computer UI — clicking, typing, and navigating like a human.

```typescript
import Anthropic from "@anthropic-ai/sdk";

const client = new Anthropic();

const response = await client.messages.create({
  model: "claude-sonnet-4-6",
  max_tokens: 4096,
  tools: [
    {
      type: "computer_20241022",
      name: "computer",
      display_width_px: 1920,
      display_height_px: 1080,
      display_number: 1,
    },
  ],
  messages: [
    {
      role: "user",
      content: "Open VS Code, create a new file called index.ts, and write a hello world function.",
    },
  ],
});
```

> **Real-world use:** Multi-step form filling, cross-app workflows, QA automation, RPA-style tasks.

---

## Super Advanced — Agents & Agentic Workflows

### 37. Claude Agent SDK

The Agent SDK handles the full tool-use loop automatically — Claude plans, executes tools, and iterates until the task is done.

```python
# Install
pip install anthropic[agent]

from anthropic import Anthropic
from anthropic.agents import ClaudeAgent, ClaudeAgentOptions

client = Anthropic()

options = ClaudeAgentOptions(
    allowed_tools=["Read", "Edit", "Bash", "Glob", "WebSearch"],
    permission_mode="acceptEdits",
    system_prompt="You are a senior Python developer. Follow PEP 8."
)

agent = ClaudeAgent(client=client, options=options)

result = agent.run("Find and fix all bugs in src/utils.py, then write tests for it.")
print(result)
```

### 38. Multi-Agent Architecture

Build networks of Claude agents for parallelism and specialization:

```
Orchestrator Agent
  ├── Research Agent    → gathers information
  ├── Code Agent        → writes implementation
  ├── Test Agent        → writes and runs tests
  └── Review Agent      → reviews and suggests improvements
```

```typescript
// Orchestrator pattern
async function runMultiAgentPipeline(task: string) {
  // Step 1: Research agent breaks down the task
  const plan = await callClaude({
    system: "You are a planning agent. Break down tasks into subtasks.",
    prompt: `Break this task into parallel subtasks: ${task}`,
  });

  // Step 2: Specialized agents execute in parallel
  const [researchResult, codeResult] = await Promise.all([
    callClaude({ system: "You are a research agent.", prompt: plan.research }),
    callClaude({ system: "You are a code agent.", prompt: plan.code }),
  ]);

  // Step 3: Synthesis agent combines results
  const finalOutput = await callClaude({
    system: "You are a synthesis agent.",
    prompt: `Combine these results:\n${researchResult}\n${codeResult}`,
  });

  return finalOutput;
}
```

### 39. RAG — Retrieval Augmented Generation

Combine Claude with a vector database to answer questions over large private knowledge bases.

```typescript
import { Anthropic } from "@anthropic-ai/sdk";
import { ChromaClient } from "chromadb"; // or Pinecone, Weaviate, pgvector

const claude = new Anthropic();
const chroma = new ChromaClient();

async function ragQuery(userQuestion: string) {
  // 1. Embed the user question
  const collection = await chroma.getCollection({ name: "my-docs" });
  const results = await collection.query({
    queryTexts: [userQuestion],
    nResults: 5, // top 5 most relevant chunks
  });

  // 2. Build context from retrieved chunks
  const context = results.documents[0].join("\n\n---\n\n");

  // 3. Ask Claude with the retrieved context
  const response = await claude.messages.create({
    model: "claude-sonnet-4-6",
    max_tokens: 2048,
    system: "Answer questions based only on the provided context. If the answer is not in the context, say so.",
    messages: [
      {
        role: "user",
        content: `Context:\n${context}\n\nQuestion: ${userQuestion}`,
      },
    ],
  });

  return response.content[0].text;
}
```

### 40. Prompt Chaining

Break complex tasks into a sequence of focused prompts:

```typescript
// Chain: Extract → Analyze → Generate
async function contentPipeline(rawArticle: string) {
  // Step 1: Extract key facts
  const facts = await callClaude(
    "Extract 5 key facts as JSON array.",
    rawArticle
  );

  // Step 2: Analyze sentiment and tone
  const analysis = await callClaude(
    "Analyze the tone and sentiment of these facts.",
    facts
  );

  // Step 3: Generate a social media post
  const post = await callClaude(
    "Write a LinkedIn post based on these insights.",
    `Facts: ${facts}\nAnalysis: ${analysis}`
  );

  return post;
}
```

---

## Super Advanced — MCP (Model Context Protocol)

MCP is an open standard that lets Claude connect to external tools, databases, services, and APIs.

### 41. Enable MCP in claude.ai

```
Settings → Integrations → Add MCP Server

Anthropic-provided MCP servers (available on Pro+):
  ✅ Gmail
  ✅ Google Calendar
  ✅ Google Drive
  ✅ Slack
  ✅ Jira
  ✅ Asana
  ✅ GitHub
  ✅ Notion
```

**Using connected MCP tools in chat:**

```
"Summarize my unread emails from today."
"Schedule a meeting with the team for next Tuesday at 2pm."
"Find the Q3 report in my Google Drive."
"Create a Jira ticket for this bug: [description]"
"Post a message to #dev-team on Slack."
```

### 42. MCP in Claude Code

```json
// ~/.claude/settings.json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "/home/user/projects"]
    },
    "postgres": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres"],
      "env": {
        "POSTGRES_CONNECTION_STRING": "postgresql://user:pass@localhost/mydb"
      }
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "ghp_..."
      }
    }
  }
}
```

### 43. Building a Custom MCP Server

```typescript
import { Server } from "@modelcontextprotocol/sdk/server/index.js";
import { StdioServerTransport } from "@modelcontextprotocol/sdk/server/stdio.js";

const server = new Server(
  { name: "my-company-mcp", version: "1.0.0" },
  { capabilities: { tools: {} } }
);

// Define a tool
server.setRequestHandler("tools/list", async () => ({
  tools: [
    {
      name: "get_employee",
      description: "Fetch employee data from internal HR system",
      inputSchema: {
        type: "object",
        properties: {
          employee_id: { type: "string" },
        },
        required: ["employee_id"],
      },
    },
  ],
}));

// Handle tool execution
server.setRequestHandler("tools/call", async (request) => {
  if (request.params.name === "get_employee") {
    const { employee_id } = request.params.arguments;
    const data = await fetchFromHRSystem(employee_id); // your internal API
    return { content: [{ type: "text", text: JSON.stringify(data) }] };
  }
});

const transport = new StdioServerTransport();
await server.connect(transport);
```

### 44. MCP in Artifacts (AI-powered apps)

```javascript
// Inside an Artifact (React/HTML), call MCP-connected APIs
const response = await fetch("https://api.anthropic.com/v1/messages", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({
    model: "claude-sonnet-4-20250514",
    max_tokens: 1000,
    messages: [{ role: "user", content: "Fetch my calendar events for today." }],
    mcp_servers: [
      {
        type: "url",
        url: "https://gcal.mcp.claude.com/mcp",
        name: "google-calendar",
      },
    ],
  }),
});
```

---

## Prompt Engineering Mastery

### 45. The Claude Prompt Stack

```
┌─────────────────────────────────┐
│        System Prompt            │  ← Role, rules, output format
├─────────────────────────────────┤
│      Cached Context             │  ← Large docs, codebase, knowledge base
├─────────────────────────────────┤
│      User Message               │  ← The actual task
├─────────────────────────────────┤
│      Examples (Few-shot)        │  ← 1-3 worked examples
├─────────────────────────────────┤
│      Constraints                │  ← Format, length, style rules
└─────────────────────────────────┘
```

### 46. Core Prompt Patterns

**Role + Task + Format:**
```
You are a senior React developer. 
Review this code for performance issues.
Return a JSON array of issues: [{file, line, issue, suggestion}]
```

**Chain of Thought:**
```
Think step by step before answering.
First, analyze the problem.
Then, consider 3 approaches.
Finally, recommend the best one with trade-offs.
```

**Constraint-based:**
```
Refactor this function:
- No external libraries
- O(n) time complexity
- Pure function (no side effects)
- Handle null, undefined, and empty arrays
- Add TypeScript generics
```

**Few-shot learning:**
```
Convert these to JSDoc:

Input: function add(a, b) { return a + b; }
Output:
/**
 * Adds two numbers.
 * @param {number} a - First number
 * @param {number} b - Second number
 * @returns {number} Sum of a and b
 */
function add(a, b) { return a + b; }

Now convert: function getUserById(id) { ... }
```

**XML for structured output:**
```
Analyze this PR diff and return:
<review>
  <bugs>[list any bugs]</bugs>
  <performance>[performance issues]</performance>
  <security>[security concerns]</security>
  <suggestion>[overall recommendation]</suggestion>
</review>
```

### 47. Advanced Prompt Patterns

**Map-Reduce for large documents:**
```
// Map phase (per chunk)
"Summarize the key technical claims in this section: [chunk]"

// Reduce phase (combine)
"Merge these summaries into a single coherent analysis, 
 noting any contradictions: [all summaries]"
```

**Self-consistency check:**
```
Answer this question 3 times independently, then identify 
which answer you're most confident in and explain why.

Question: What's the best database for a high-write, 
low-read SaaS application with multi-tenancy?
```

**Critique + Refine loop:**
```
Turn 1: "Write a system design for a real-time notification service."
Turn 2: "Critique the design you just wrote. List 5 weaknesses."
Turn 3: "Now rewrite the design addressing all 5 weaknesses."
```

---

## Quick Reference Card

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CLAUDE.AI SURFACES
  Artifacts       → Live panel: code, HTML, React, SVG, docs
  Projects        → Persistent workspace with memory + files
  Memory          → Cross-session personalization
  Web Search      → Real-time web access
  Deep Research   → Multi-step research synthesis
  Extended Think  → Deep step-by-step reasoning
  Computer Use    → UI automation (experimental)
  MCP Tools       → Gmail, Calendar, Drive, Slack, Jira, GitHub

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CLAUDE CODE CLI
  claude          → Start session in terminal
  /init           → Auto-generate CLAUDE.md
  /clear          → Clear context
  /model          → Switch model
  /undo           → Undo last file change
  /diff           → Show file changes
  /review         → Review pending changes
  /cost           → Check token usage
  /help           → All commands

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CLAUDE API
  Messages API    → Single/multi-turn conversations
  Streaming       → Real-time token streaming
  Vision          → Image + text input
  Tool Use        → Function calling
  Batch API       → Async bulk requests (50% cost)
  Prompt Caching  → Cache static context (cost savings)
  Extended Think  → thinking: { type: "enabled", budget_tokens: N }

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
MODELS
  claude-opus-4-6         → Most intelligent
  claude-sonnet-4-6       → Best balance (default)
  claude-haiku-4-5-...    → Fastest, cheapest

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
AGENTIC STACK
  Agent SDK       → Autonomous loop with built-in tools
  MCP             → Connect to any external service
  RAG             → Claude + vector DB for private knowledge
  Multi-Agent     → Orchestrator + specialized sub-agents
  Prompt Chains   → Extract → Analyze → Generate pipelines
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Useful Links

| Resource | URL |
|---|---|
| Claude.ai | https://claude.ai |
| API Docs | https://docs.claude.com |
| Console (API Keys) | https://console.anthropic.com |
| Claude Code Docs | https://code.claude.com/docs |
| Anthropic Courses | https://anthropic.skilljar.com |
| MCP Documentation | https://modelcontextprotocol.io |
| Prompt Library | https://docs.anthropic.com/en/prompt-library |
| Status Page | https://status.anthropic.com |

---

> **Guide Version:** April 2026  
> **Covers:** Claude Opus 4.6, Sonnet 4.6, Haiku 4.5 · Claude Code · MCP · Agent SDK
