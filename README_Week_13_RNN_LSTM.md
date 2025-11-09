# Week 13: Recurrent Neural Networks (RNNs) and LSTMs

## 📘 Summary

This project explores **Recurrent Neural Networks (RNNs)** and **Long
Short-Term Memory (LSTM)** models for sequence and time-series
prediction tasks.\
It includes theoretical understanding, hands-on implementation using
synthetic data, and a client project predicting real stock prices
(**Netflix - NFLX.csv**) using LSTM.

------------------------------------------------------------------------

## 🧠 Theory Overview

### Recurrent Neural Networks (RNNs)

-   Designed to handle **sequential or time-dependent data**.
-   Uses **loops** to retain information from previous steps.
-   Suitable for text, speech, and stock price prediction.

### Long Short-Term Memory (LSTM)

-   A type of RNN that solves the **vanishing gradient problem**.
-   Uses gates (Forget, Input, Output) to control memory flow.
-   Effective for long-term dependencies in sequences.

------------------------------------------------------------------------

## 🧩 Model Overview

-   **Model Used:** LSTM Neural Network\
-   **Dataset:** Netflix stock price data (`Close` column)\
-   **Training Ratio:** 80% training, 20% testing\
-   **Input Window:** Previous 60 days → predict next day price

------------------------------------------------------------------------

## 🏗 Model Architecture

  Layer       Details
  ----------- ---------------------------------
  LSTM        50 units, return_sequences=True
  LSTM        50 units
  Dense       25 neurons
  Dense       1 neuron (output)
  Optimizer   Adam
  Loss        Mean Squared Error

------------------------------------------------------------------------

## 📊 Results

-   **Root Mean Squared Error (RMSE):** \~2--3 depending on run.\
-   **Visualization:** Displays training, validation, and predicted
    stock prices.\
-   The model captures stock price trends effectively using temporal
    dependencies.

------------------------------------------------------------------------

## ⚙️ How to Run

1.  Place your dataset file (e.g., `NFLX.csv`) in the same directory.

2.  Run the Python script:

    ``` bash
    python week_13_recurrent_neural_networks_(rnns)_and_lstms.py
    ```

3.  View the output plot and RMSE value in the console.

------------------------------------------------------------------------

## 🗂 Files Included

1.  `week_13_recurrent_neural_networks_(rnns)_and_lstms.py` -- Main
    Python script\
2.  `Week_13_RNN_LSTM_Summary.pdf` -- Summary report\
3.  `README.md` -- This file

------------------------------------------------------------------------

## 🧾 License

This project is for **educational purposes** only as part of the Data
Science learning series.
