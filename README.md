# Reservoir Network — Quantization Results

This repository holds the results of quantization experiments on an Echo State Network (ESN) trained on NARMA time series tasks.

---

## What's in here

All files live under `attention/Result/Regression/`.

### Notebooks
- `model.ipynb` — the main model: builds and trains the ESN on NARMA10 and NARMA20
- `comparison.ipynb` — compares performance across different quantization levels

### Plots
Visual comparisons of predictions vs ground truth for each task and bit-width:
- NARMA10 and NARMA20 at **4-bit**, **6-bit**, and **8-bit** quantization

### Weights
Saved quantized weights for the reservoir, input, bias, and readout layers — organized by bit-width (4, 6, 8):
- `quantized_reservoir_weights_Wr_*` — reservoir connectivity matrix
- `quantized_input_weights_Win_*` — input weights
- `quantized_bias_weights_*` — bias
- `readout_weights_Wout_*` and `readout_bias_*` — trained readout layer
- `scale_*` — quantization scale factors

### States & Data
- `states_train_*.npy` / `states_test_*.npy` — reservoir states at each bit-width
- `y_train.npy` / `y_test.npy` — target outputs
- `u_NARMA10.npy` / `u_NARMA20.npy` — input signals
