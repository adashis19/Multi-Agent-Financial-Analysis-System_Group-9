# Multi-Agent-Financial-Analysis-System_Group-9
Build a real-world financial analysis system powered by agentic AI.

# 📈 Multi-Agent Financial Analysis System (MAFAS)

## Overview
This notebook implements a **real-world financial research agentic system** that can **plan, research, evaluate, and refine** investment analysis autonomously.

Unlike traditional scripted pipelines, this system uses **Agentic AI** — specialized reasoning agents that plan, critique, and improve each other’s work.  
Each agent performs a distinct cognitive function and interacts dynamically to produce a refined, high-quality **Research Report** for a given stock symbol.

---

## 🎯 Objectives
- Build an **autonomous Investment Research Agent** that:
  - Plans research steps for a stock symbol.
  - Dynamically uses tools (APIs, datasets, retrieval).
  - Self-reflects on the quality of outputs.
  - Learns from memory between runs.
- Demonstrate three **workflow patterns**:
  - **Prompt Chaining**: News → Preprocess → Classify → Extract → Summarize.
  - **Routing**: Direct content to the right specialist.
  - **Evaluator–Optimizer**: Evaluate quality → Refine using feedback.

---

## 🧩 Architecture

### 1. **Core Components**
| Agent | Role | Key Function |
|--------|------|---------------|
| **PlannerAgent** | Defines research goals and steps | Plans scope, data, and deliverables |
| **NewsPipelineAgent** | Handles Prompt Chaining | Fetch → Clean → Classify → Extract → Summarize |
| **RouterAgent** | Implements Routing | Chooses which specialist to engage |
| **EarningsAnalyzer** | Specialist | Analyzes fundamentals and valuations |
| **MacroAnalyzer** | Specialist | Interprets macroeconomic indicators |
| **MarketAnalyzer** | Specialist | Examines technical and market trends |
| **EvaluatorOptimizer** | Evaluator–Optimizer | Scores, critiques, and refines the research note |
| **Orchestrator** | Conductor | Coordinates agents, integrates results, saves artifacts |

### 2. **Tools & Data**
- **Yahoo Finance API** – stock prices, financials, fundamentals  
- **NewsAPI** – latest company and market news  
- **Alpha Vantage (fallback)** – news sentiment & market data  
- **FRED API** – economic indicators (CPI, unemployment)  
- **OpenAI GPT model** – reasoning, summarization, evaluation  
- **Memory module** – stores past route and score for adaptive learning  


