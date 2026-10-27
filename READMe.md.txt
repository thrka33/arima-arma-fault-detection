# Predictive Fault Detection in Smart Embedded Communication (ARIMA vs ARMA)

![Python](https://img.shields.io/badge/Python-3.x-blue)

## Problem
Smart embedded communication systems produce continuous sensor time-series
data. Faults must be predicted early to keep systems reliable.

## Result (TL;DR)
| Model | Mean accuracy (10 runs) |
|-------|------------------------|
| ARIMA | 98.7% |
| ARMA  | 94.4% |

ARIMA improved accuracy by +4.3 points (independent-samples t-test, p < 0.05).

![Accuracy comparison](results/accuracy_comparison.png)

## Approach
1. **Data acquisition:** sensor signals from smart embedded communication data
2. **Preprocessing:** [describe: cleaning, differencing / stationarity handling]
3. **Models:** ARIMA vs ARMA
4. **Evaluation:** accuracy over 10 iterations, error analysis, t-test
   (α = 0.05, 80% power; SPSS and ClinCalc)

## Dataset
[Source, size, number of features. If synthetic or simulated, say so.]

## How to run
```bash
git clone https://github.com/thrka33/arima-arma-fault-detection
cd arima-arma-fault-detection
pip install -r requirements.txt
jupyter notebook notebooks/01_eda_and_modeling.ipynb
```

## Limitations and next steps
- [e.g. small number of runs; try LSTM / Prophet; test on real device data]

## Author
Tharika S, B.E. ECE, Saveetha School of Engineering