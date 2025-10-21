# Stock Analysis Agent System (Colab Notebook)

This project is a Google Colab notebook that provides a comprehensive stock analysis tool powered by AI agents. It offers fundamental, technical, and sentiment analysis for stocks using a multi-agent system built with LangChain. The system integrates with APIs for financial data, technical indicators, and market sentiment, and features a Gradio-based web interface for user interaction.

## Features

- **Fundamental Analysis**: Analyzes financial statements (income statements, balance sheets, cash flow statements) using the financialdatasets.ai API.
- **Technical Analysis**: Retrieves stock price data and calculates technical indicators (RSI, MACD, SMA, EMA, Bollinger Bands) using financialdatasets.ai and pandas_ta.
- **Sentiment Analysis**: Fetches options chain data (via yfinance), insider trading data (via financialdatasets.ai), and market news sentiment (via Tavily API).
- **Gradio Interface**: A user-friendly web interface in Colab to input queries and view results, with processing time displayed.
- **Supervisor Agent**: Coordinates the fundamental, technical, and sentiment agents to provide a cohesive investment recommendation (e.g., buy, hold, sell).

## Getting Started

### Prerequisites

- A Google Colab account (free tier is sufficient).
- API keys for:
  - Poe API (`POE_API_KEY`)
  - Financial Datasets API (`FINANCIAL_DATASETS_API_KEY`)
  - Tavily API (`TAVILY_API_KEY`)

### Running in Google Colab

1. **Download the Notebook**:
   - Clone this repository or download the `stock_analysis_colab.ipynb` file:
     ```bash
     git clone https://github.com/your-username/your-repo-name.git
     ```
   - Alternatively, download the `.ipynb` file directly from the repository.

2. **Open in Colab**:
   - Go to [Google Colab](https://colab.research.google.com/).
   - Upload the `stock_analysis_colab.ipynb` file by clicking "File" > "Upload Notebook".

3. **Install Dependencies**:
   - The notebook includes a cell to install required libraries:
     ```bash
     !pip install gradio==4.44.0 pandas==2.2.2 requests==2.32.3 langchain_openai==0.2.1 tavily-python==0.5.0 yfinance==0.2.43 pandas_ta==0.3.14b0
     ```
   - Run this cell first to install dependencies.

4. **Set API Keys**:
   - The notebook includes a cell to input API keys securely using `getpass`. Run the cell and enter your API keys when prompted:
     ```python
     os.environ['POE_API_KEY'] = getpass('Enter your Poe API key: ')
     os.environ['FINANCIAL_DATASETS_API_KEY'] = getpass('Enter your Financial Datasets API key: ')
     os.environ['TAVILY_API_KEY'] = getpass('Enter your Tavily API key: ')
     ```
   - **Note**: Do not hardcode API keys in the notebook for security reasons.

5. **Run the Script**:
   - Execute the main script cell to launch the Gradio interface.
   - Colab will provide a public URL (e.g., `https://*.ngrok.io`) to access the Gradio interface in your browser.

6. **Use the Interface**:
   - In the Gradio interface, enter a query, e.g.:
     ```
     Provide a comprehensive analysis of TSLA stock including fundamental, technical, and sentiment aspects.
     ```
   - Click the "Submit" button to process the query.
   - Results will appear in the "Analysis Results" box, with processing time displayed.

## Example Query





## Notes

- **Colab Environment**: The Colab environment resets after each session, so you need to reinstall dependencies and re-enter API keys each time.
- **Gradio URL**: The Gradio interface runs through a temporary public URL in Colab. Ensure you copy the URL to access it.
- **API Limitations**: The analysis depends on real-time data from financialdatasets.ai, yfinance, and Tavily APIs. Ensure your API keys are valid and your subscription plans allow sufficient requests.
- **Error Handling**: If an API returns a 402 status code (payment required), check your subscription plan. Other errors will be displayed in the output.
- **Output Box**: The results box is sized for readability (20 lines, expandable to 50 lines, 500px height).

## Repository Structure

- `stock_analysis_colab.ipynb`: The main Colab notebook with the stock analysis system.
- `requirements.txt`: Lists the required Python libraries with specific versions for reference.
- `README.md`: This file, providing instructions for running the notebook.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contact

For questions or issues, please open an issue on GitHub or contact [your-email@example.com].
