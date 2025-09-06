# QuantitativeProjects

A modular Python-based platform for extracting financial data, performing fundamental and technical analysis via API, and simulating algorithmic trading strategies.

## 🚀 Features

This repository is a comprehensive suite of tools for quantitative finance and algorithmic trading. It includes:

*   **RESTful APIs (Built with FastAPI):**
    *   **DCF Valuation API:** Calculates the intrinsic value of a publicly traded company using a Discounted Cash Flow model. Inputs a ticker symbol and returns a detailed valuation breakdown.
    *   **Fundamental Analysis API:** Fetches balance sheet, income statement, and cash flow data from Yahoo Finance to calculate and analyze key financial ratios (P/E, P/B, ROE, Debt/Equity, etc.).
    *   **Technical Analysis API:** Processes historical price data to generate and interpret popular technical indicators (SMA, EMA, RSI, MACD) for a given security.
*   **Market Simulator:** A virtual trading environment that uses historical market data to backtest trading strategies without risking real capital. Tracks portfolio value, cash balance, and trade history (stored in SQLite).
*   **Algorithmic Trading Bots:** A collection of bots with varying risk profiles (e.g., Conservative, Moderate, Aggressive) designed to execute trades within the simulated market based on predefined logic and signals from the APIs.

## 🛠️ Tech Stack

*   **Language:** Python 3.8+
*   **APIs & Web Framework:** FastAPI, Pydantic
*   **Data Processing & Analysis:** Pandas, NumPy
*   **Financial Data:** yfinance
*   **Database:** SQLite
*   **Visualization:** (Planned) Matplotlib/Seaborn
*   **Deployment:** (Planned) Docker

## 📁 Project Structure

QuantitativeProjects/

|-- apis/
│   |-- dcf_valuation/ # DCF Valuation API
│   |-- fundamental_analysis/ # Fundamental Analysis API
│   -- **technical_analysis/** # Technical Analysis API │   |-- main.py # FastAPI app instance │   |-- routers.py # API endpoint definitions │   |-- models.py # Pydantic models for request/response │   |-- calculator.py # Core logic for indicator calculations │   -- README.md # Specific setup & usage
|
|-- market_simulator/ # Market simulation engine
│   |-- engine.py
│   |-- portfolio.py
│   -- database.py # SQLite interaction | |-- **trading_bots/** # Trading strategy algorithms │   |-- **options/** # Options trading strategies │   |   |-- bot_conservative_options.py │   |   |-- bot_moderate_options.py │   |   -- bot_aggressive_options.py
│   |-- stocks/ # Stock trading strategies
│   |   |-- bot_conservative_stocks.py
│   |   |-- bot_moderate_stocks.py
│   |   -- bot_aggressive_stocks.py │   -- base_bot.py # Abstract base class for bots
|
|-- tests/ # Unit and integration tests
|
|-- .gitignore
|-- requirements.txt
|-- LICENSE
|-- README.md # This file


## ⚡ Getting Started

### Prerequisites
- Python 3.8 or higher
- `pip` (Python package installer)

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Niccolo-Bal/QuantitativeProjects.git
    cd QuantitativeProjects
    ```

2.  **(Recommended) Create a virtual environment:**
    ```bash
    python -m venv venv
    # On Windows:
    .\venv\Scripts\activate
    # On macOS/Linux:
    source venv/bin/activate
    ```

3.  **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

### Usage

#### Running the APIs
Navigate to the API directory and start the Uvicorn server. For example, to run the Technical Analysis API:

```bash
cd apis/technical_analysis
uvicorn main:app --reload
```
📌 Project Status

    Current Phase: 🚧 Planning & Initial Development

    Next Steps: Development of the core Technical Analysis API module.

🤝 Contributing

This is a personal portfolio project. While primarily for my own learning, ideas, constructive feedback, and suggestions are always welcome. Please feel free to fork the repository and submit Pull Requests for any improvements.
📜 License

This project is licensed under the MIT License. See the LICENSE file for details.
👨‍💻 Author

Niccolò Balestriere

    Email: niccolo.balestriere@gmail.com

    LinkedIn: https://www.linkedin.com/in/niccol%C3%B2-balestriere-7b9459295/

    GitHub: https://github.com/Niccolo-Bal
