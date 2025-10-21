# Stock Analysis Agent System

This repository contains a Google Colab notebook for a Stock Analysis Agent System that leverages AI agents to provide comprehensive stock analysis. Built with Python and LangChain, it integrates financial APIs for fundamental, technical, and sentiment analysis, delivering investment recommendations through a Gradio-based web interface.

## Features

- **Fundamental Analysis**: Processes financial statements (income statements, balance sheets, cash flows) using the [financialdatasets.ai](https://financialdatasets.ai) API.
- **Technical Analysis**: Computes technical indicators (RSI, MACD, SMA, EMA, Bollinger Bands) with `financialdatasets.ai` and `pandas_ta` for market trend insights.
- **Sentiment Analysis**: Collects options chain data (via `yfinance`), insider trading data (via `financialdatasets.ai`), and news sentiment (via [Tavily API](https://tavily.com)).
- **Supervisor Agent**: Coordinates fundamental, technical, and sentiment agents for cohesive investment recommendations (e.g., buy, hold, sell).
- **Gradio Interface**: Provides a user-friendly web interface in Colab for querying stocks and viewing results with processing time.
- **Performance Tracking**: Displays query processing time to monitor efficiency.

## Prerequisites

- Python 3.8 or higher (provided by Google Colab)
- Access to the following APIs (API keys required):
  - [Poe API](https://poe.com) for GPT-4o-mini
  - [Financial Datasets API](https://financialdatasets.ai) for financial data
  - [Tavily API](https://tavily.com) for news sentiment
- Internet connection for API calls and library downloads
- A Google Colab account (free tier is sufficient)

## Installation

1. **Clone or Download the Repository**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
