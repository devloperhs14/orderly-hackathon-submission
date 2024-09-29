# Orderly Hackathon

This repository contains the code and resources for the Orderly Hackathon project. The primary focus is to develop and backtest trading strategies using the `emp_orderly` library.

## Project Structure

- `strategy.ipynb`: Jupyter Notebook containing the setup and execution of a trading strategy.
- `README.md`: This file, providing an overview of the project.
- `requirements.txt`: Contains the dependencies needed to run the project.

## Key Components

### 1. Imports and Environment Setup

- Loading necessary libraries such as:
  - `dotenv`
  - `pandas`
  - `matplotlib`
  - `emp_orderly`
  
- Setting up environment variables for secure access to sensitive information like private keys and account details.

### 2. Wallet and SDK Initialization

- **Wallet Creation:** A new wallet is created using `PrivateKeyWallet.create_new()`.
- **SDK Initialization:** The `EmpyrealOrderlySDK` is initialized with the wallet's private key and account ID for managing and executing trades on the Orderly network.

### 3. Strategy Definition

- **SMA Crossover Strategy:** 
  - A class `SmaCross` is implemented, utilizing two Simple Moving Averages (SMA) to determine buy/sell signals.
  - This crossover strategy triggers buy signals when the shorter SMA crosses above the longer SMA, and sell signals when it crosses below.

### 4. Backtesting Setup

- **Tester Initialization:** 
  - An `EmpOrderly` backtester is set up with parameters such as initial cash, commission, and the initialized SDK.
  - The strategy is set, historical data is loaded, and backtests are executed.
  
- **Results Plotting:** 
  - After running the backtests, performance metrics and the equity curve are plotted for easy visualization and analysis.

## Usage

To run this project, follow these steps:

### 1. Clone the Repository

```bash
git clone https://github.com/devloperhs14/orderly-hackathon.git

cd orderly-hackathon
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```
### 3. Run Jupyter Notebook

```bash
jupyter notebook strategy.ipynb
```

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements
The emp_orderly library and its contributors.

The Orderly Hackathon organizers and participants.

For more information, visit the repository.


