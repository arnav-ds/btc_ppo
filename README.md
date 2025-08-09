project:
  name: "PPO Bitcoin Trading Bot"
  description: >
    This project implements a Proximal Policy Optimization (PPO) reinforcement learning
    agent to trade Bitcoin against a Buy & Hold benchmark. The bot is trained on historical
    BTC price data and evaluated with key performance metrics.

structure:
  - folder: "Data/"
    description: "Dataset (not included in repo due to size limit)"
  - folder: "Results/"
    description: "Output graphs and reports"
  - file: "ppo_real_btc.zip"
    description: "Trained PPO model weights"
  - file: "einforcement_Learning_BTC_Trading_vs_BuyHold.ipynb"
    description: "Main Jupyter Notebook"
  - file: "README.md"
    description: "Project documentation"

features:
  - "Uses Stable-Baselines3 PPO for training"
  - "Custom Bitcoin trading environment"
  - "Benchmark comparison with Buy & Hold"
  - "Risk-adjusted performance metrics"
  - "Equity curve visualization"

metrics:
  - Sharpe Ratio
  - Sortino Ratio
  - Max Drawdown
  - Win Rate
  - Profit Factor

sample_performance_report:
  final_portfolio_value: "$100,168.48"
  total_return: "0.17%"
  CAGR: "0.01%"
  sharpe_ratio: 0.98
  sortino_ratio: 0.82
  volatility_annualized: "0.01%"
  max_drawdown: "-0.01%"
  win_rate: "12.77%"
  profit_factor: 1.42

installation:
  commands:
    - "git clone https://github.com/arnav-ds/btc_ppo.git"
    - "cd btc_ppo"
    - "pip install -r requirements.txt"

dataset:
  source: "https://www.kaggle.com/datasets/mczielinski/bitcoin-historical-data"
  download_code: |
    import kagglehub
    path = kagglehub.dataset_download("mczielinski/bitcoin-historical-data")
    print("Path to dataset files:", path)
  move_to: "E:/BTC_PPO_Trading/Data"

usage:
  train:
    description: "Run the notebook to train the PPO agent"
    command: "jupyter notebook einforcement_Learning_BTC_Trading_vs_BuyHold.ipynb"
  evaluate:
    description: "Run evaluation cells in the notebook to simulate agent, compare to Buy & Hold, and generate metrics/graphs"

example_output:
  description: "Equity curves comparing PPO Agent vs Buy & Hold strategy"
  includes_graphs: true

license: "MIT License — feel free to use and modify"
author: "Arnav — Data Science & AI Enthusiast"
