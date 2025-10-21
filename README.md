Stock Analysis Agent System (Colab Notebook)
This Google Colab notebook provides a comprehensive stock analysis tool powered by AI agents, offering fundamental, technical, and sentiment analysis for stocks. Built with LangChain, it integrates with APIs for financial data, technical indicators, and market sentiment, and features a Gradio-based web interface for user interaction.
Features

Fundamental Analysis: Analyzes financial statements (income statements, balance sheets, cash flow statements) using the financialdatasets.ai API.
Technical Analysis: Retrieves stock price data and calculates technical indicators (RSI, MACD, SMA, EMA, Bollinger Bands) using financialdatasets.ai and pandas_ta.
Sentiment Analysis: Fetches options chain data (via yfinance), insider trading data (via financialdatasets.ai), and market news sentiment (via Tavily API).
Gradio Interface: A user-friendly web interface in Colab to input queries and view results, with processing time displayed.
Supervisor Agent: Coordinates the fundamental, technical, and sentiment agents to provide a cohesive investment recommendation (e.g., buy, hold, sell).

Getting Started
Prerequisites

A Google Colab account (free tier is sufficient).
API keys for:
Poe API (POE_API_KEY)
Financial Datasets API (FINANCIAL_DATASETS_API_KEY)
Tavily API (TAVILY_API_KEY)



Setup Instructions

Clone or Download the Repository:
git clone https://github.com/your-username/your-repo-name.git

Alternatively, download stock_analysis_colab.ipynb directly from the repository.

Open in Google Colab:

Navigate to Google Colab.
Click File > Upload Notebook and select stock_analysis_colab.ipynb.


Install Dependencies:

The notebook includes a cell to install required libraries. Run the following cell in Colab:!pip install gradio==4.44.0 pandas==2.2.2 requests==2.32.3 langchain_openai==0.2.1 tavily-python==0.5.0 yfinance==0.2.43 pandas_ta==0.3.14b0




Set API Keys:

Run the cell provided in the notebook to input API keys securely using getpass:import os
from getpass import getpass
os.environ['POE_API_KEY'] = getpass('Enter your Poe API key: ')
os.environ['FINANCIAL_DATASETS_API_KEY'] = getpass('Enter your Financial Datasets API key: ')
os.environ['TAVILY_API_KEY'] = getpass('Enter your Tavily API key: ')


Note: Avoid hardcoding API keys in the notebook for security reasons.


Run the Notebook:

Execute the main script cell to launch the Gradio interface.
Colab will provide a public URL (e.g., https://*.ngrok.io) to access the interface in your browser.



Usage

Access the Gradio Interface:

Copy the public URL provided by Colab and open it in your browser.
The interface includes instructions, an input box for queries, and an output box for results.


Enter a Query:

Input a stock analysis query, such as:Provide a comprehensive analysis of TSLA stock including fundamental, technical, and sentiment aspects.


Specify a stock ticker, technical indicators (e.g., RSI, MACD), or specific financial data as needed.


View Results:

Click the Submit button to process the query.
Results, including fundamental, technical, and sentiment analyses with an investment recommendation, will appear in the Analysis Results box.
Processing time (in seconds) is displayed at the end.



Example
Query:
Provide a comprehensive analysis of AAPL stock including fundamental, technical, and sentiment aspects.

Sample Output (simplified):
### Fundamental Analysis
- Data retrieved from financialdatasets.ai
- Revenue growth: X% over the past 5 years
- Debt-to-equity ratio: Y
...

### Technical Analysis
- Current price: $Z (USD)
- RSI: 65.2 (neutral, close to overbought)
...

### Sentiment Analysis
- Recent insider trades: 3 buys, 2 sells
- News sentiment: Positive due to recent product launches
...

### Recommendation
Based on strong fundamentals and positive sentiment, consider a "Buy" for AAPL.

Processing time: 5.23 seconds

Repository Structure

stock_analysis_colab.ipynb: The main Colab notebook with the stock analysis system.
requirements.txt: Lists required Python libraries with specific versions for reference.
README.md: This file, providing instructions for running the notebook.
LICENSE: MIT License file (if included).

Notes

Colab Environment: Colab sessions reset after inactivity or a set time (e.g., 12 hours on free tier). Re-run all cells to restart.
Gradio URL: Ensure you’re connected to the internet. If the URL fails, rerun the demo.launch() cell.
API Limitations: Verify that your API keys are valid and your subscription plans allow sufficient requests. A 402 status code indicates a payment issue with the API.
Output Box: The results box is sized for readability (20 lines, expandable to 50 lines, 500px height).
Dependency Versions: The requirements.txt lists specific versions. If you encounter issues, check for version conflicts or update versions as needed.

Contributing
Contributions are welcome! To contribute:

Fork the repository.
Create a feature branch:git checkout -b feature/your-feature


Commit your changes:git commit -m "Add your feature"


Push to the branch:git push origin feature/your-feature


Open a pull request.

Please ensure your changes are tested in a fresh Colab environment.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For questions or issues, open a GitHub issue or contact [your-email@example.com].
