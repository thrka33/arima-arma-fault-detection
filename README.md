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


## Approach
1. **Data acquisition:** sensor signals from smart embedded communication data
2. **Preprocessing:** [describe: cleaning, differencing / stationarity handling]
3. **Models:** ARIMA vs ARMA
4. **Evaluation:** accuracy over 10 iterations, error analysis, t-test
   (α = 0.05, 80% power; SPSS and ClinCalc)

## Dataset
Dataset has been collected from kaggle website 
dataset link : https://www.kaggle.com/datasets/ziya07/industrial-iot-fault-detection-dataset

## How to run
```bash
git clone https://github.com/thrka33/arima-arma-fault-detection
cd arima-arma-fault-detection
pip install -r requirements.txt
jupyter notebook SPIC_2.ipynb
```

## Limitations and next steps
- Unfair baseline. ARMA assumes stationary data, and your slides say the data is non-stationary. ARIMA includes differencing, so it winning is partly expected rather than a surprise.
Small, possibly non-independent samples. The t-test uses 10 iterations per model. If those runs reuse the same dataset, the p-value can overstate how significant the result is.
-No hardware test. Prediction speed and memory use weren’t measured on an embedded device, which matters for real-time monitoring.
Test assumptions. The t-test assumes roughly normal scores. Accuracies near 100% bunch up against the ceiling, and 10 points can’t confirm normality.

## Author
Tharika S, B.E. ECE, Saveetha School of Engineering
