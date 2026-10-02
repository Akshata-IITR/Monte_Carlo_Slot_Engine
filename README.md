# Vectorized Monte Carlo Slot Engine & Volatility Analytics

A high-performance **Monte Carlo Simulation Engine** built in Python (NumPy) to model, evaluate and optimize slot machine game math models over **10,000,000 (10M) spins**.

## Business & Mathematical Overview
Designing casino slot machines requires balancing **Return to Player (RTP)**, **Hit Frequency**, and **Volatility** to maintain house edge while providing engaging gameplay. This engine simulates complex reel configurations, variable payouts, and multi-tier respin mechanics using vectorized arrays for high statistical precision.

## Performance & Statistical Results

| Metric | Simulated Value | Industry Target Benchmark | Status |
| :--- | :--- | :--- | :--- |
| **Total Simulated Spins** | `10,000,000` | ≥ 1,000,000 | ✅ Statistically Significant |
| **Simulated RTP** | **`90.2060%`** | `90.0% - 96.0%` | ✅ Industry Standard Pass |
| **Hit Frequency** | **`18.60%`** | `15.0% - 25.0%` | ✅ Optimal Hit Rate |
| **Volatility (Std Dev)** | **`6.8904`** | `5.0 - 10.0` | ✅ Medium-High Volatility |
| **95% Confidence Margin** | **`±0.4271%`** | `< ±0.5%` | ✅ High Precision |

---

## Optimization & Iteration Process

1. **Baseline Model:** Initial random stop evaluation yielded an unviable RTP (~50%) due to sparse high-tier symbol hits and excess non-paying blank stops.
2. **Reel Strip Optimization:** Adjusted symbol distribution matrix by increasing mid-tier symbol counts (`Cherry` & `Bar`) while optimizing blank ratio across reels.
3. **Respin Mechanics & Multipliers:** Integrated conditional respin logic with a 3.0x multiplier on specific trigger masks, lifting the overall RTP to **~90.2%**.
4. **Vectorization:** Replaced Python loops with NumPy mask arrays, accelerating execution time for 10M iterations to ~1.2 seconds.

---

## Tech Stack & Methods
* **Language:** Python 3.x
* **Core Libraries:** NumPy (Vectorized Array Operations), Matplotlib (Distribution Plotting)
* **Statistical Methods:** Monte Carlo Method, Standard Deviation Analysis, Confidence Interval Modeling
