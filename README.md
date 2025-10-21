# Stock Analysis Agent System (Colab Notebook)

This project is a Google Colab notebook that provides a comprehensive stock analysis tool powered by AI agents. It offers fundamental, technical, and sentiment analysis for stocks using a multi-agent system built with LangChain. The system integrates with APIs for financial data, technical indicators, and market sentiment, and features a Gradio-based web interface for user interaction.

## Features

- **Fundamental Analysis**: Analyzes financial statements (income statements, balance sheets, cash flow statements) using the [financialdatasets.ai](https://financialdatasets.ai) API.
- **Technical Analysis**: Retrieves stock price data and calculates technical indicators (RSI, MACD, SMA, EMA, Bollinger Bands) using [financialdatasets.ai](https://financialdatasets.ai) and [pandas_ta](https://github.com/twopirllc/pandas-ta).
- **Sentiment Analysis**: Fetches options chain data (via [yfinance](https://github.com/ranaroussi/yfinance)), insider trading data (via [financialdatasets.ai](https://financialdatasets.ai)), and market news sentiment (via [Tavily API](https://tavily.com)).
- **Gradio Interface**: A user-friendly web interface in Colab to input queries and view results, with processing time displayed.
- **Supervisor Agent**: Coordinates the fundamental, technical, and sentiment agents to provide a cohesive investment recommendation (e.g., buy, hold, sell).

## Getting Started

### Prerequisites

- A Google Colab account (free tier is sufficient).
- API keys for:
  - [Poe API](https://poe.com) (`POE_API_KEY`)
  - [Financial Datasets API](https://financialdatasets.ai) (`FINANCIAL_DATASETS_API_KEY`)
  - [Tavily API](https://tavily.com) (`TAVILY_API_KEY`)

### Running in Google Colab

1. **Download the Notebook**:
   - Clone this repository or download the `stock_analysis_colab.ipynb` file:
     ```bash
     git clone https://github.com/your-username/your-repo-name.git
  - Alternatively, download the `stock_analysis_colab.ipynb` file directly from the repository.

2. **Open in Colab**:
   - Go to [Google Colab](https://colab.research.google.com).
   - Upload the `stock_analysis_colab.ipynb` file by clicking "File" > "Upload Notebook".

3. **Install Dependencies**:
   - The notebook includes a cell to install required libraries:
     ```bash
     !pip install gradio==4.44.0 pandas==2.2.2 requests==2.32.3 langchain_openai==0.2.1 tavily-python==0.5.0 yfinance==0.2.43 pandas_ta==0.3.14b0
