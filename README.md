# 🤖 Investment Research Agent with LangChain & Gemini

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![LangChain](https://img.shields.io/badge/LangChain-0.1.16-green.svg)](https://github.com/langchain-ai/langchain)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **A comprehensive Jupyter notebook implementing a multi-agent AI system for autonomous investment research and portfolio optimization using LangChain and Google's Gemini LLM.**

**AAI 520 - Final Team Project**  
**Team Members:** Tirthankar Sen, Kesavan Rangaswamy, Rajendra Warke  
**Date:** October 2025

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [What's Inside the Notebook](#whats-inside-the-notebook)
- [Installation & Setup](#installation--setup)
- [Running the Notebook](#running-the-notebook)
- [Key Components](#key-components)
- [Results](#results)
- [Project Files](#project-files)
- [Troubleshooting](#troubleshooting)
- [Customization Guide](#customization-guide)
- [Citation](#citation)
- [License](#license)

---

## 🎯 Overview

This Jupyter notebook demonstrates a complete **multi-agent AI system** for investment research and portfolio optimization. The system showcases advanced agentic AI capabilities including:

- 🧠 **Autonomous Planning** - Dynamic research strategy generation
- 🔧 **Tool Orchestration** - Real-time financial data integration via APIs
- 🔍 **Self-Reflection** - Quality assessment and iterative refinement
- 📚 **Continuous Learning** - Memory storage and pattern recognition

### Key Achievement
📊 **59% improvement in portfolio Sharpe ratio** (0.74 → 1.18) through AI-driven optimization

### Technologies Used

- **LangChain** - Agent orchestration framework
- **Google Gemini Pro** - Large language model for reasoning
- **Yahoo Finance API** - Real-time market data (via `yfinance`)
- **NewsAPI** (Optional) - Financial news sentiment analysis
- **Pydantic** - Type-safe tool schemas

---

## ✨ Features

### 🤖 Four Agent Functions

1. **Research Planner** - Decomposes investment research into actionable steps
2. **Tool Executor** - Orchestrates external APIs (prices, financials, news)
3. **Self-Reflector** - Evaluates research quality and identifies gaps
4. **Memory System** - Stores experiences and learns patterns across sessions

### 🔄 Three Workflow Patterns

1. **Prompt Chaining** - 5-step sequential pipeline (Ingest → Preprocess → Classify → Extract → Summarize)
2. **Routing** - Dynamic routing to specialist analysts (Price, Fundamental, Sentiment)
3. **Evaluator-Optimizer** - Iterative refinement for quality improvement

### 📊 Capabilities

- ✅ Comprehensive stock research (price trends, financials, news sentiment)
- ✅ Portfolio optimization with risk-adjusted allocation
- ✅ Multi-stock comparative analysis
- ✅ Real-time data integration
- ✅ Interpretable AI-generated reports
- ✅ Quality assurance and self-correction

---

## 📓 What's Inside the Notebook

The notebook is organized into **10 major sections** with approximately **50 code cells**:

### **Section 1: Installation and Setup**
- Package installation commands
- API key configuration
- LLM initialization and testing

### **Section 2: Custom LangChain Tools**
- `StockPriceTool` - Historical prices, returns, volatility
- `StockFinancialsTool` - P/E ratios, ROE, margins, debt metrics
- `StockNewsTool` - Recent news for sentiment analysis

### **Section 3: Agent Functions (The Core)**
- **3.1 Research Planner Agent** - Creates dynamic research plans
- **3.2 Tool Execution Agent** - Executes tools and aggregates data
- **3.3 Self-Reflection Agent** - Evaluates quality scores
- **3.4 Memory & Learning System** - Stores sessions and extracts patterns

### **Section 4: Workflow Patterns**
- **4.1 Prompt Chaining Workflow** - Multi-step news processing
- **4.2 Routing Workflow** - Specialist analyst routing
- **4.3 Evaluator-Optimizer Workflow** - Iterative refinement

### **Section 5: Complete Investment Research Agent**
- Integration of all 4 agents + 3 workflows
- Full 8-step research pipeline
- End-to-end execution

### **Section 6: Demonstration**
- Comprehensive research on AAPL
- Execution metrics and quality scores
- Detailed report output

### **Section 7: Multi-Stock Comparison**
- Comparative analysis (AAPL vs MSFT)
- Side-by-side metrics and recommendations

### **Section 8: Learning Demonstration**
- Memory system pattern extraction
- Quality improvement over repeated sessions

### **Section 9: Project Validation**
- Requirements checklist verification
- Technology stack confirmation

### **Section 10: Portfolio Optimization Extension**
- Upload portfolio (CSV/Excel)
- Filter stocks by allocation threshold
- Fetch metrics with Sharpe ratio calculation
- AI-driven portfolio rebalancing

---

## 🚀 Installation & Setup

### Prerequisites

- **Python 3.8+** installed
- **Jupyter Notebook or JupyterLab** installed
- **Google Gemini API key** (free) - [Get it here](https://makersuite.google.com/app/apikey)
- **(Optional) NewsAPI key** - [Get it here](https://newsapi.org/)

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/investment-research-agent.git
cd investment-research-agent
```

### Step 2: Install Jupyter (if not already installed)

```bash
pip install jupyter
```

### Step 3: Install Dependencies

**Option A: Install from requirements.txt**
```bash
pip install -r requirements.txt
```

**Option B: Install manually**
```bash
pip install langchain==0.1.16 \
            langchain-core==0.1.42 \
            langchain-community==0.0.32 \
            langchain-google-genai==0.0.11 \
            google-generativeai==0.4.1 \
            yfinance \
            pandas \
            numpy \
            pydantic \
            requests
```

**Option C: Install directly in notebook**
The notebook includes installation cells that you can run directly - just execute them!

### Step 4: Configure API Keys

Open the notebook and find the configuration cell (Section 1), then add your API key:

```python
import os
os.environ["GOOGLE_API_KEY"] = "YOUR_GEMINI_API_KEY_HERE"
os.environ["NEWS_API_KEY"] = "your_news_api_key_here"  # Optional
```

---

## 🏃 Running the Notebook

### Step 1: Launch Jupyter Notebook

```bash
# From the project directory
jupyter notebook
```

Or with JupyterLab:
```bash
jupyter lab
```

Your browser will open automatically at `http://localhost:8888`

### Step 2: Open the Notebook

In the Jupyter interface, click on:
```
investment_research_agent.ipynb
```

### Step 3: Run All Cells

**⚠️ IMPORTANT:** Run cells **sequentially from top to bottom**!

**Method 1: Run All Cells at Once**
```
Menu: Cell → Run All
```

**Method 2: Run Cell by Cell**
- Click on a cell
- Press `Shift + Enter` to run and move to next cell
- Or press `Ctrl + Enter` to run and stay on current cell

### Step 4: Monitor Execution

Watch the output under each cell. You'll see:
```
[OK] Packages installed
[OK] Gemini LLM initialized
[OK] Custom LangChain tools created
...
[COMPLETE] RESEARCH COMPLETE
```

### Expected Runtime

- **Full notebook (all cells)**: ~5-8 minutes
- **Single stock research**: ~30 seconds
- **Portfolio optimization**: ~2-3 minutes

---

## 🔑 Key Components

### System Architecture

```
┌─────────────────────────────────────────────────────────┐
│              USER INPUT (Stock Symbol)                  │
└────────────────────┬────────────────────────────────────┘
                     │
        ┌────────────┴────────────┐
        │                         │
        ▼                         ▼
┌──────────────┐          ┌──────────────┐
│   AGENT      │          │  WORKFLOW    │
│  FUNCTIONS   │◄────────►│  PATTERNS    │
├──────────────┤          ├──────────────┤
│ • Planner    │          │ • Chaining   │
│ • Executor   │          │ • Routing    │
│ • Reflector  │          │ • Optimizer  │
│ • Memory     │          │              │
└──────┬───────┘          └──────┬───────┘
       │                         │
       └────────────┬────────────┘
                    ▼
            ┌───────────────┐
            │  TOOLS LAYER  │
            ├───────────────┤
            │ • Prices      │
            │ • Financials  │
            │ • News        │
            └───────┬───────┘
                    ▼
            ┌───────────────┐
            │ GEMINI LLM    │
            └───────┬───────┘
                    ▼
            ┌───────────────┐
            │ FINAL REPORT  │
            └───────────────┘
```

### Complete Workflow (8 Steps)

When you run `agent.research('AAPL', 'comprehensive')`, the system executes:

1. **Research Planning** - Planner creates task list
2. **Tool Execution** - Executor fetches data from APIs
3. **Prompt Chaining** - News processed through 5-step pipeline
4. **Routing** - Data sent to specialist analysts
5. **Report Generation** - Findings synthesized
6. **Self-Reflection** - Quality evaluated
7. **Evaluator-Optimizer** - Report refined if needed
8. **Memory Storage** - Session stored for learning

---

## 📊 Results

### Experiment 1: Single Stock Research (AAPL)

**Execution Summary:**
```
[COMPLETE] RESEARCH COMPLETE
Duration: 27.9s | Quality: 85.00%
Agent Functions: 4/4 [OK]
Workflow Patterns: 3/3 [OK]
```

**Key Outputs:**
- Current Price: $178.45
- 1-Year Return: +23.7%
- Volatility: 22.3%
- P/E Ratio: 29.8
- ROE: 147.3%
- Sentiment Score: 7.2/10
- **Recommendation: HOLD**

### Experiment 2: Multi-Stock Comparison

| Metric | AAPL | MSFT | Winner |
|--------|------|------|--------|
| 1-Year Return | +23.7% | +31.4% | MSFT |
| Volatility | 22.3% | 19.8% | MSFT ✓ |
| Sharpe Ratio | 0.99 | 1.42 | MSFT ✓ |
| P/E Ratio | 29.8 | 33.2 | AAPL ✓ |
| ROE | 147.3% | 43.7% | AAPL ✓ |
| **Recommendation** | **HOLD** | **BUY** | - |

### Experiment 3: Portfolio Optimization

**Before vs After:**

| Metric | Original Portfolio | Optimized Portfolio | Improvement |
|--------|-------------------|---------------------|-------------|
| Expected Return | 18.3% | 22.7% | **+4.4%** |
| Volatility | 24.6% | 19.2% | **-5.4%** |
| **Sharpe Ratio** | **0.74** | **1.18** | **+59.5%** |

**Top Allocation Changes:**
- **MSFT**: 12% → 25% (+13%) - "High Sharpe, low vol"
- **TSM**: 5% → 18% (+13%) - "Strategic semiconductor"
- **JNJ**: 4% → 15% (+11%) - "Defensive healthcare"
- **NVDA**: 8% → 15% (+7%) - "AI growth leader"

### Experiment 4: Learning Over Time

5 repeated sessions on AAPL:
- Quality Score: 0.73 → 0.91 (**+24%**)
- Execution Time: 31.2s → 24.3s (**-22%**)
- Demonstrates autonomous improvement!

---

## 📁 Project Files

```
investment-research-agent/
│
├── README.md                           # This file
├── investment_research_agent.ipynb     # 🎯 Main Jupyter notebook
├── requirements.txt                    # Python dependencies
├── .gitignore                          # Git ignore rules
├── LICENSE                             # MIT License
│
├── data/
│   ├── sample_portfolio.csv            # Example portfolio for testing
│   └── research_memory.json            # Auto-generated (memory storage)
│
└── docs/
    ├── research_paper.md               # Full academic paper
    └── Manuscript_Draft_1.docx         # Original draft
```

### File Descriptions

**Main Files:**
- `investment_research_agent.ipynb` - The complete notebook with all code
- `requirements.txt` - All Python package dependencies
- `README.md` - This documentation

**Data Files:**
- `sample_portfolio.csv` - Example portfolio with 11 stocks
- `research_memory.json` - Generated automatically by the memory system

**Documentation:**
- `research_paper.md` - Full academic paper (8-10 pages)
- Original manuscript draft

---

## 🐛 Troubleshooting

### Issue: "ModuleNotFoundError: No module named 'langchain'"

**Solution:**
Run the installation cells in Section 1 of the notebook, or:
```bash
pip install --upgrade langchain langchain-google-genai
```

### Issue: "Invalid API key" or "API key not found"

**Solution:**
1. Get API key from https://makersuite.google.com/app/apikey
2. In notebook, find the configuration cell and set:
   ```python
   os.environ["GOOGLE_API_KEY"] = "AIzaSyB..."  # Your actual key
   ```
3. Re-run the LLM initialization cell

### Issue: Notebook kernel dies or crashes

**Causes:**
- Out of memory (large datasets)
- Package version conflicts

**Solution:**
```bash
# Restart Jupyter kernel
# Menu: Kernel → Restart & Clear Output

# Or reinstall packages
pip install --upgrade --force-reinstall langchain google-generativeai
```

### Issue: "No data found" for stock symbol

**Causes:**
- Invalid ticker (use uppercase: AAPL not aapl)
- Market closed
- Network issues

**Solution:**
```python
# Try different stock or period
result = agent.research('MSFT', research_type='comprehensive')
```

### Issue: Cells taking very long to execute

**Causes:**
- Normal for comprehensive research (multiple API calls)
- Network latency

**Solution:**
- Use `research_type='quick'` for faster results
- Check internet connection
- Reduce number of stocks analyzed

### Issue: "Rate limit exceeded"

**Solution:**
- Wait a few minutes
- Reduce frequency of API calls
- Check API quota at https://console.cloud.google.com

### Issue: Memory file corrupted

**Solution:**
In a notebook cell, run:
```python
import os
if os.path.exists('data/research_memory.json'):
    os.remove('data/research_memory.json')
print("Memory file deleted. Will be recreated on next run.")
```

---

## ✏️ Customization Guide

### Change Stock Symbol

Find cells with `'AAPL'` and replace:

```python
# Original
results = complete_agent.research('AAPL', research_type='comprehensive')

# Your stock
results = complete_agent.research('TSLA', research_type='comprehensive')
```

### Adjust Research Type

```python
# Quick (faster, less comprehensive)
results = agent.research('AAPL', research_type='quick')

# Comprehensive (slower, detailed)
results = agent.research('AAPL', research_type='comprehensive')
```

### Modify Temperature (Creativity)

Find the CONFIG section:
```python
CONFIG = {
    'TEMPERATURE': 0.7,  # Higher = more creative (0.0-1.0)
    'GEMINI_MODEL': 'gemini-pro-latest',
    ...
}
```

### Change Portfolio Allocation Threshold

In Section 10:
```python
# Original: Filter stocks with >2% allocation
filtered = portfolio_df[portfolio_df['allocation'] > 0.02]

# Modified: Filter stocks with >5% allocation
filtered = portfolio_df[portfolio_df['allocation'] > 0.05]
```

### Adjust Risk-Free Rate

```python
CONFIG['RISK_FREE_RATE'] = 0.05  # 5% instead of 4%
```

### Add More Stocks to Comparison

```python
symbols = ['AAPL', 'MSFT', 'NVDA', 'GOOGL', 'AMZN']  # Add more!
for symbol in symbols:
    result = agent.research(symbol)
```

---

## 🎓 Educational Use

This notebook demonstrates key concepts for:

### AI/ML Students:
✅ Multi-agent system design  
✅ LangChain framework patterns  
✅ LLM tool integration  
✅ Prompt engineering  
✅ Self-reflection mechanisms  
✅ Memory and learning systems  

### Finance Students:
✅ Modern Portfolio Theory  
✅ Sharpe ratio optimization  
✅ Quantitative analysis  
✅ Risk-return tradeoffs  
✅ Fundamental analysis  
✅ Sentiment analysis  

### Computer Science Students:
✅ API integration  
✅ Workflow orchestration  
✅ Error handling  
✅ Data validation (Pydantic)  
✅ Software architecture  
✅ Design patterns  

---

## 📖 Citation

If you use this notebook in your research or coursework:

### BibTeX
```bibtex
@misc{investment_agent_2025,
  title = {Investment Research Agent with LangChain and Gemini},
  author = {Sen, Tirthankar and Rangaswamy, Kesavan and Warke, Rajendra},
  year = {2025},
  month = {10},
  howpublished = {Jupyter Notebook},
  url = {https://github.com/yourusername/investment-research-agent},
  note = {AAI 520 Final Project}
}
```

### Academic Citation
```
Sen, T., Rangaswamy, K., & Warke, R. (2025). Investment Research Agent 
with LangChain and Gemini: A Multi-Agent AI System for Portfolio 
Optimization [Jupyter Notebook]. AAI 520 Final Project.
```

---

## 📄 License

MIT License - See LICENSE file for details.

```
Copyright (c) 2025 Tirthankar Sen, Kesavan Rangaswamy, Rajendra Warke

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## 🙏 Acknowledgments

- **LangChain Team** - Agent framework
- **Google AI** - Gemini API
- **Yahoo Finance** - Financial data
- **USD AAI Staff** - Project guidance
- **Open Source Community** - Supporting libraries

---

## 📞 Contact

**Team Members:**
- Tirthankar Sen - [email@example.com]
- Kesavan Rangaswamy - [email@example.com]
- Rajendra Warke - [email@example.com]

**Repository:** [https://github.com/yourusername/investment-research-agent](https://github.com/yourusername/investment-research-agent)

---

## 🚀 Quick Start Checklist

Before running the notebook, ensure:

- [ ] Python 3.8+ installed
- [ ] Jupyter installed (`pip install jupyter`)
- [ ] Repository cloned
- [ ] Dependencies installed (`pip install -r requirements.txt`)
- [ ] Gemini API key obtained
- [ ] API key set in notebook configuration cell
- [ ] Internet connection active

✅ **Ready?** Open notebook and run all cells!

---

## 🌟 Give us a Star!

If this project helps you learn about multi-agent AI or portfolio optimization, please star the repository! ⭐

---

**Built with ❤️ for AAI 551 | October 2025**
