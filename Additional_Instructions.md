Act as an expert data scientist and Python developer. We are building a game-theory optimization script for the "Southwest Monsoon Fantasy Forecasts" game. 

Phase 1 Goal: Write a Python script that models the game's exact scoring math and fits historical data.

Requirements:
1. Define a function `calculate_score(p_est, p_act)` that mirrors the game's exact percentile logic:
   - Error = abs(p_est - p_act)
   - Accuracy Loss (AL) = min(Error / 15, 1)
   - Accuracy Score (AS) = 4 * (1 - AL)
   - If p_est >= 85: IP = p_est - 85
   - Elif p_est < 15: IP = 15 - p_est
   - Else: IP = 0
   - RIF = 1 + (IP / 15)
   - Return AS * RIF

2. Include a mock simulation where you generate a synthetic historical rainfall dataset for a city, fit it to a Scipy Gamma distribution, and demonstrate how to find the optimal 'p_est' that maximizes Expected Value given a probabilistic forecast curve.

Output clean, modular, and well-commented code.
