# 📊 AI-Powered Stock Research Analyst (n8n Workflow)

## 🚀 Overview

This project is an AI-powered multi-agent stock analysis system built using n8n and OpenRouter LLM integration.

It simulates a real-world financial research pipeline that collects stock data, analyzes news sentiment, evaluates risk, and generates an investment recommendation directly via email.

The system demonstrates how AI agents, APIs, and deterministic logic can be combined to automate financial decision-making workflows.

---

## 🎯 Problem Statement

Manual stock research requires:
- Financial data analysis
- News sentiment tracking
- Risk evaluation
- Decision-making

This process is slow and inconsistent.

This workflow automates the entire pipeline using AI agents and structured logic.

---

## 🧠 Architecture

Manual Trigger  
→ Ticker Input  
→ Financial Data Collector (Alpha Vantage API)  
→ News Research Agent (NewsAPI)  
→ Risk Analysis Agent (Qwen 32B via OpenRouter)  
→ Deterministic Scoring Engine  
→ Conditional Routing (BUY / WATCHLIST / AVOID)  
→ Human Approval Node  
→ Email Final Report  

---

## 🤖 AI Agents Used

### 1. Financial Data Collector Agent
Uses Alpha Vantage API to fetch:
- Market Cap  
- PE Ratio  
- EPS  
- Revenue Growth  
- Profit Margins  
- Debt-to-Equity Ratio  

---

### 2. News Research Agent
Uses NewsAPI to collect latest news and perform sentiment analysis:
- Positive / Neutral / Negative sentiment  
- Key market events  
- Risk signals  

---

### 3. Risk Analysis Agent
Uses Qwen 32B model via OpenRouter API to evaluate:
- Financial risk  
- Market volatility  
- News impact  
- Sector risk  
- Overall risk score (0–100)  

---

## 📊 Deterministic Scoring Engine

A rule-based scoring system ensures consistent outputs (no AI bias).

Scoring factors:
- Financial Health  
- Revenue Growth  
- News Sentiment  
- Risk Level  
- Profitability  

Final Output:
```json
{
  "final_score": 85,
  "recommendation": "BUY"
}
```

---


---

## ✉️ Output System

Instead of generating PDFs, the system directly sends an email report containing:

- Company overview  
- Financial summary  
- News sentiment analysis  
- Risk assessment  
- Final recommendation  

---

## 🛠️ Tech Stack

- n8n (Automation Workflow)
- OpenRouter API
- Qwen 32B LLM
- Alpha Vantage API
- NewsAPI
- SMTP / Gmail Email Node

---

## 🔐 Environment Variables

Create a `.env` file:

```
OPENROUTER_API_KEY=your_openrouter_key
ALPHAVANTAGE_API_KEY=your_alpha_vantage_key
NEWSAPI_API_KEY=your_newsapi_key
EMAIL_USER=your_email
```

---

## 📥 How to Use

1. Import workflow JSON into n8n  
2. Add API credentials (OpenRouter, Alpha Vantage, NewsAPI, Email)  
3. Enter a stock ticker (e.g., AAPL, TSLA, INFY)  
4. Run workflow manually  
5. Receive analysis via email  

---

## ⚙️ Key Features

- Multi-agent AI architecture  
- Real-time financial data integration  
- News sentiment analysis  
- Deterministic scoring engine  
- Conditional routing logic  
- Fully automated email reporting  
- Human approval checkpoint  

---

## 📌 Future Improvements

- PDF report generation  
- Database storage for historical analysis  
- Slack/Telegram notifications  
- Analytics dashboard  
- Confidence scoring per agent  

---

## 🧾 Author

Built as part of an AI workflow automation assignment using n8n + LLM agents + financial APIs.

---

## ⭐ Outcome

This project demonstrates:
- Real-world AI system design  
- Multi-agent orchestration  
- API integration  
- Deterministic + AI hybrid decision-making  
- Production-style automation workflow  
```
