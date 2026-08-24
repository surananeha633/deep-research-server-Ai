<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:111827,50:7C3AED,100:06B6D4&height=250&section=header&text=Deep%20Research%20MCP%20Server&fontSize=44&fontColor=ffffff&animation=fadeIn"/>

# 🔬 Deep Research MCP Server

### AI-Powered Deep Research Assistant with Gemini & MCP

<p>

<img src="https://img.shields.io/badge/Node.js-22.x-339933?style=for-the-badge&logo=node.js&logoColor=white">
<img src="https://img.shields.io/badge/TypeScript-5.9.2-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
<img src="https://img.shields.io/badge/Gemini-2.5%20Flash-8E75B2?style=for-the-badge&logo=google">
<img src="https://img.shields.io/badge/MCP-Model%20Context%20Protocol-06B6D4?style=for-the-badge">
<img src="https://img.shields.io/badge/License-MIT-success?style=for-the-badge">

</p>

<img src="https://readme-typing-svg.demolab.com?font=Poppins&size=22&pause=1000&color=06B6D4&center=true&width=900&lines=AI-Powered+Deep+Research;Gemini+2.5+Flash+Research+Pipeline;Model+Context+Protocol+Server;Iterative+Research+%26+Analysis;Evidence-Based+Research+Reports"/>

### 🚀 Conduct iterative, evidence-based research using Google Gemini 2.5 Flash.

</div>

---

# 🌍 Overview

**Deep Research MCP Server** is an AI-powered research assistant designed to perform **iterative and structured research** using **Google Gemini 2.5 Flash**.

The system automatically generates research queries, analyzes search results, extracts useful insights, performs additional research based on previous findings, and produces a structured Markdown research report.

It is designed around the **Model Context Protocol (MCP)**, making the research engine usable with MCP-compatible AI agents and clients.

---

# ✨ Key Features

| Feature                    | Description                                          |
| -------------------------- | ---------------------------------------------------- |
| 🤖 Gemini 2.5 Flash        | Advanced AI reasoning and structured research        |
| 🔎 Google Search Grounding | Retrieve current information from the web            |
| 🔄 Iterative Research      | Refine queries based on previous findings            |
| 🧠 Deep Analysis           | Extract meaningful insights from research results    |
| 📊 Depth & Breadth Control | Control how deeply and broadly research is performed |
| 🧩 MCP Integration         | Use research as an MCP tool                          |
| ⚡ Batch Processing         | Process multiple AI requests efficiently             |
| 💾 LRU Caching             | Reduce repeated API calls                            |
| 📝 Professional Reports    | Generate structured Markdown research reports        |
| 🛡️ Zod Validation         | Validate structured AI-generated outputs             |

---

# 🎯 Why This Project?

Traditional research often requires manually searching multiple sources, comparing information, extracting important findings, and organizing everything into a report.

**Deep Research MCP Server automates this workflow.**

Instead of asking an AI model a single question, the system follows an iterative research process:

```text
User Question
      ↓
Research Planning
      ↓
Search Query Generation
      ↓
Web Research
      ↓
Result Analysis
      ↓
Extract Learnings
      ↓
Generate New Research Directions
      ↓
Repeat Research
      ↓
Final Report
```

This approach helps produce more structured and comprehensive research results.

---

# 🧠 AI Research Pipeline

```text
                    ┌──────────────────┐
                    │   User Query     │
                    └────────┬─────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │  Research Planner   │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │ SERP Query Generator│
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │   Google Search     │
                  │     Grounding       │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │ Result Processing   │
                  └──────────┬──────────┘
                             │
                    ┌────────┴────────┐
                    ▼                 ▼
             ┌────────────┐    ┌────────────┐
             │ Learnings  │    │ Directions │
             └─────┬──────┘    └─────┬──────┘
                   │                  │
                   └────────┬─────────┘
                            ▼
                    ┌──────────────┐
                    │ More Research│
                    └──────┬───────┘
                           │
                     Depth > 0?
                      /         \
                    Yes          No
                     │            │
                     ▼            ▼
              Continue Loop   Final Report
                                  │
                                  ▼
                           📑 Markdown Report
```

---

# 🤖 Persona Agents

The project uses **persona-based AI agents** to improve the quality and consistency of different research stages.

### 🔍 Research Strategist

Responsible for generating effective search queries and identifying important research directions.

### 🧠 Research Assistant

Analyzes retrieved information and extracts important findings relevant to the research question.

### 🎯 Query Refiner

Identifies gaps in existing research and generates follow-up questions.

### 🎓 Professional Researcher

Provides the overall research behavior, emphasizing:

* Logical reasoning
* Evidence-based analysis
* Structured writing
* Source evaluation
* Comprehensive investigation

Using specialized personas helps each stage of the pipeline focus on a specific research objective.

---

# ⚙️ How It Works

The research pipeline is divided into several core modules.

### `src/deep-research.ts`

Main research orchestrator responsible for:

* Generating research queries
* Processing research results
* Running analysis passes
* Managing research depth
* Synthesizing the final report

### `src/ai/providers.ts`

Handles Gemini API interaction, including:

* Gemini 2.5 Flash
* Batch requests
* Token management
* Optional Gemini tools
* Caching

### `src/ai/text-splitter.ts`

Provides:

* Recursive text splitting
* Semantic splitting
* Token-aware chunking

### `src/mcp-server.ts`

Provides the MCP server entry point and tool definitions.

### `src/run.ts`

Provides standalone command-line execution.

---

# 🏗️ Project Architecture

```text
User
 │
 ▼
MCP Client / CLI
 │
 ▼
MCP Server
 │
 ▼
Deep Research Engine
 │
 ├── Query Generator
 │
 ├── Google Search Grounding
 │
 ├── Result Processor
 │
 ├── Research Analyzer
 │
 ├── Query Refiner
 │
 ├── Gemini Provider
 │
 ├── Cache Manager
 │
 └── Report Generator
 │
 ▼
Structured Markdown Report
```

---

# 📂 Project Structure

```text
📦 deep-research-mcp-server

├── 📂 src
│   │
│   ├── 📂 ai
│   │   ├── providers.ts
│   │   └── text-splitter.ts
│   │
│   ├── 📄 deep-research.ts
│   ├── 📄 mcp-server.ts
│   ├── 📄 prompt.ts
│   ├── 📄 feedback.ts
│   ├── 📄 output-manager.ts
│   ├── 📄 progress-manager.ts
│   ├── 📄 terminal-utils.ts
│   ├── 📄 types.ts
│   │
│   └── 📂 utils
│       └── JSON / sanitization helpers
│
├── 📂 dist
│   └── Build output
│
├── 📄 .env.example
├── 📄 package.json
├── 📄 README.md
└── 📄 tsconfig.json
```

---

# 💻 Tech Stack

| Technology                 | Purpose                    |
| -------------------------- | -------------------------- |
| 🟢 Node.js 22              | Runtime environment        |
| 🔷 TypeScript 5.9          | Application development    |
| 🧠 Gemini 2.5 Flash        | AI reasoning and research  |
| 🔎 Google Search Grounding | Web research               |
| 🔌 MCP                     | AI tool integration        |
| 🛡️ Zod                    | Schema validation          |
| ⚡ LRU Cache                | Performance optimization   |
| 📝 Markdown                | Research report generation |

---

# 📋 Requirements

Before running the project, make sure you have:

* Node.js **v22.x**
* npm
* Google Gemini API key
* MCP-compatible client (for MCP usage)

---

# 🚀 Getting Started

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/ssdeanx/deep-research-mcp-server.git
```

## 2️⃣ Navigate to the Project

```bash
cd deep-research-mcp-server
```

## 3️⃣ Install Dependencies

```bash
npm install
```

## 4️⃣ Create Environment File

Create a `.env.local` file in the project root.

```env
GEMINI_API_KEY="your_gemini_key"

GEMINI_MODEL=gemini-2.5-flash

GEMINI_MAX_OUTPUT_TOKENS=65536

CONCURRENCY_LIMIT=5

ENABLE_GEMINI_GOOGLE_SEARCH=true

ENABLE_GEMINI_CODE_EXECUTION=false

ENABLE_GEMINI_FUNCTIONS=false
```

## 5️⃣ Build the Project

```bash
npm run build
```

---

# 🔌 Using as an MCP Tool

Start the MCP server:

```bash
node --env-file .env.local dist/mcp-server.js
```

The server exposes the **`deep-research`** MCP tool.

### Parameters

| Parameter           | Type     | Description                |
| ------------------- | -------- | -------------------------- |
| `query`             | string   | Research question          |
| `depth`             | number   | Research depth from 1–5    |
| `breadth`           | number   | Research breadth from 1–5  |
| `existingLearnings` | string[] | Previous research findings |

### Example

```json
{
  "name": "deep-research",
  "arguments": {
    "query": "State of multi-agent research agents in 2025",
    "depth": 3,
    "breadth": 3,
    "existingLearnings": [
      "Tool use improves grounding",
      "Batching reduces latency"
    ]
  }
}
```

---

# 💻 Standalone CLI Usage

You can also run the research assistant directly from the terminal.

```bash
npm run start "your research query"
```

### Example

```bash
npm run start "What are the latest developments in AI research agents?"
```

The system will automatically perform research and generate a structured report.

---

# 🧪 MCP Inspector

Use the MCP Inspector for interactive testing and debugging.

```bash
npx @modelcontextprotocol/inspector node --env-file .env.local dist/mcp-server.js
```

This allows you to inspect the MCP server and test the available research tool.

---

# ⚙️ Configuration

| Variable                       | Description             | Default            |
| ------------------------------ | ----------------------- | ------------------ |
| `GEMINI_API_KEY`               | Google Gemini API key   | Required           |
| `GEMINI_MODEL`                 | Gemini model            | `gemini-2.5-flash` |
| `GEMINI_MAX_OUTPUT_TOKENS`     | Maximum output tokens   | `65536`            |
| `CONCURRENCY_LIMIT`            | Concurrent requests     | `5`                |
| `ENABLE_GEMINI_GOOGLE_SEARCH`  | Google Search Grounding | `true`             |
| `ENABLE_GEMINI_CODE_EXECUTION` | Code execution          | `false`            |
| `ENABLE_GEMINI_FUNCTIONS`      | Function calling        | `false`            |

---

# ⚡ Quickstart

```bash
git clone https://github.com/ssdeanx/deep-research-mcp-server.git

cd deep-research-mcp-server

npm install

npm run build
```

Create `.env.local`, add your Gemini API key, and then run:

```bash
npm run start "state of multi-agent research agents in 2025"
```

Or start the MCP server:

```bash
node --env-file .env.local dist/mcp-server.js
```

---

# 📊 Example Research Output

The generated research report follows a professional structure:

```markdown
# Abstract

Overview of the research objective,
scope, methodology, and findings.

# Table of Contents

Research sections and navigation.

# Introduction

Background and research context.

# Body

Detailed evidence-based analysis.

# Methodology

Research process and source analysis.

# Limitations

Research limitations and assumptions.

# Key Learnings

Important findings and insights.

# References

Normalized citations and sources.
```

---

# 🧪 Research Validation

The latest version introduces additional research-quality checks.

### ✅ Input Validation

Research queries must meet minimum quality requirements.

### 📚 Citation Density

Generated reports are checked for sufficient citation coverage.

### 🔎 Recent Sources

The system checks for recent references where appropriate.

### ⚖️ Conflict Disclosure

Potential conflicts or disagreements between sources are identified and disclosed.

---

# 🚀 Performance Improvements

Recent improvements include:

* ⚡ Concurrent research processing
* 📦 Batched Gemini requests
* 💾 LRU caching
* 🧠 Semantic context management
* 🔄 Recursive research depth
* 🛡️ Improved error handling
* 📊 Research metrics
* 📉 Reduced unnecessary API calls
* 🔧 Improved TypeScript type safety

### Performance Highlights

| Improvement           | Result                            |
| --------------------- | --------------------------------- |
| ⚡ Research processing | Faster research cycles            |
| 🚀 Initial research   | Improved response speed           |
| 📉 API errors         | Reduced through better handling   |
| 🧮 Token usage        | More efficient context management |

---

# 🗺️ Roadmap

* 🔍 Exa search integration
* 🌐 Improved web research providers
* 🤖 Advanced multi-agent research
* 📊 Research analytics
* 🧪 Automated testing
* ⚙️ GitHub Actions CI/CD
* 📑 Sample research reports
* 💬 Improved research prompts
* 🔗 Additional MCP-compatible clients

---

# 🛠️ Troubleshooting

### ❌ Missing API Key

Make sure `GEMINI_API_KEY` exists in `.env.local`.

```env
GEMINI_API_KEY="your_gemini_key"
```

### ❌ Google Search Grounding Not Working

Check:

```env
ENABLE_GEMINI_GOOGLE_SEARCH=true
```

### ❌ High Latency

Reduce the concurrency limit:

```env
CONCURRENCY_LIMIT=3
```

### ❌ Output Too Long

Reduce research depth or breadth.

```bash
npm run start "your query"
```

Use smaller research parameters when invoking the MCP tool.

### ❌ JSON Validation Errors

The pipeline validates and repairs structured JSON responses. If errors continue, try reducing the query complexity or research scope.

---

# 🎯 Skills Demonstrated

* 🤖 Generative AI
* 🧠 LLM Application Development
* 🔎 AI-Powered Research
* 🔌 Model Context Protocol
* 📘 Google Gemini API
* 🔷 TypeScript
* 🟢 Node.js
* 🔄 Agentic AI Workflows
* 📊 Information Retrieval
* 🧩 Prompt Engineering
* 🛡️ Structured Output Validation
* ⚡ API Optimization
* 💾 Caching
* 📝 Automated Report Generation

---

# 🌟 Why Deep Research MCP Server?

Deep Research MCP Server demonstrates how modern AI systems can move beyond simple question answering toward **iterative, tool-assisted research**.

It combines:

**LLMs + Web Search + MCP + Iterative Reasoning + Structured Reports**

into a single research pipeline.

The project is intentionally designed to remain understandable, extensible, and easy for developers to experiment with.

---

# 🤝 Contributing

Contributions are welcome!

### Contribution Steps

```bash
# Fork the repository

# Clone your fork
git clone <your-fork-url>

# Create a branch
git checkout -b feature/new-feature

# Make your changes

# Build and test
npm run build

# Commit your changes
git commit -m "Add new feature"

# Push your branch
git push origin feature/new-feature
```

Then open a Pull Request.

For major changes, please open an issue first to discuss the proposed improvement.

---

# 📄 License

This project is licensed under the **MIT License**.


---

# 👨‍💻 Project

<div align="center">

### 🔬 Deep Research MCP Server

**AI-Powered Research • Gemini • MCP • Agentic AI**

<br>

⭐ **If you found this project useful, consider giving it a Star!**

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:06B6D4,50:7C3AED,100:111827&height=120&section=footer"/>

</div>
