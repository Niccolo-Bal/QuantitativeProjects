# QuantitativeProjects

A modular Python-based platform for extracting financial data, performing fundamental and technical analysis, and simulating algorithmic trading strategies through local financial modeling tools.

## 🚀 Features

This repository is a comprehensive suite of tools for quantitative finance and algorithmic trading. It includes:

*   **Financial Modeling Tools:**
    *   **DCF Valuation Model:** Calculates the intrinsic value of a publicly traded company using a Discounted Cash Flow model. Inputs a ticker symbol and returns a detailed valuation breakdown.
    *   **Fundamental Analysis Model:** Fetches balance sheet, income statement, and cash flow data from Yahoo Finance to calculate and analyze key financial ratios (P/E, P/B, ROE, Debt/Equity, etc.).
    *   **Technical Analysis Model:** Processes historical price data to generate and interpret popular technical indicators (SMA, EMA, RSI, MACD) for a given security.
*   **Market Simulator:** A virtual trading environment that tracks portfolio value, cash balance, and trade history (stored in SQLite). Uses historical market data to backtest trading strategies without risking real capital.
*   **Algorithmic Trading Bots:** A collection of bots with varying risk profiles (e.g., Conservative, Moderate, Aggressive) designed to execute trades within a simulated market based on predefined logic and signals from the financial models.

## 🛠️ Tech Stack

*   **Language:** Python 3.8+
*   **Data Processing & Analysis:** Pandas, NumPy
*   **Financial Data:** yfinance
*   **Database:** (Planned) SQLite
*   **Visualization:** (Planned) Matplotlib/Seaborn
*   **Deployment:** (Planned) Docker


## 📁 Project Structure


```text
QuantitativeProjects/
├── models/                       # Finance models
│   ├── dcf_valuation/            
│   │   ├── dcf_model.py          # DCF valuation calculations
│   │   ├── data_fetcher.py       # Financial data retrieval
│   │   ├── models.py             # Data models and structures
│   │   └── README.md             
│   ├── fundamental_analysis/     
│   │   ├── fundamental_model.py  # Fundamental ratio calculations
│   │   ├── data_fetcher.py       # Financial statement data
│   │   ├── models.py             # Data models and structures
│   │   └── README.md             
│   └── technical_analysis/       
│       ├── technical_model.py    # Technical indicator calculations
│       ├── data_fetcher.py       # Fetches and cleans data from yfinance
│       ├── models.py             # Data models for indicators
│       ├── calculator.py         # Core logic for indicator calculations
│       ├── test.py               # Test file for models (all commented out)
│       └── README.md             
│
├── market_simulator/             # Market simulation engine
│   ├── engine.py
│   ├── portfolio.py
│   ├── database.py               # SQLite interaction
│   └── trading_bots/             # Trading strategy algorithms
│       ├── options/              # Options trading strategies
│       │   ├── bot_conservative_options.py
│       │   ├── bot_moderate_options.py
│       │   └── bot_aggressive_options.py
│       ├── stocks/               # Stock trading strategies
│       │   ├── bot_conservative_stocks.py
│       │   ├── bot_moderate_stocks.py
│       │   └── bot_aggressive_stocks.py
│       └── README.md
│
├── tests/                        # Unit and integration tests
│
├── .gitignore
├── requirements.txt
├── LICENSE
└── README.md                     # This file
```

## ⚡ Set Up

### Prerequisites
- Python 3.8 or higher
- `pip` (Python package installer)

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Niccolo-Bal/QuantitativeProjects.git
    cd QuantitativeProjects
    ```

2.  **(Optional) Create a virtual environment:**
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

#### Running the Financial Models
Navigate to the specific model directory and run the Python scripts directly. For example, to use the Technical Analysis model:

```bash
cd models/technical_analysis
python technical_model.py
```

#### Running Market Simulations
To start the market simulator:

```bash
cd market_simulator
python engine.py
```

## 📌 Project Status

__Last Completed ✅:__ Planning, Initial Development & primary README.md file.

__Current Phase 🚧:__ Development of DCF calculations and core logic.

__Next Steps 📝:__ Integration of assumptions and initial testing of DCF model.

## 🤝 Contributing

This is a personal portfolio project. While primarily for my own learning and to showcase my skills, I am new to both finance and data science, so ideas, constructive feedback, and suggestions are always welcome. Feel free to fork the repository and submit Pull Requests for any improvements.

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for details.

## 👨‍💻 Author

Niccolò Balestriere

Email: niccolo.balestriere@gmail.com

LinkedIn: https://www.linkedin.com/in/niccol%C3%B2-balestriere-7b9459295/

GitHub: https://github.com/Niccolo-Bal

Website: Soon to come
