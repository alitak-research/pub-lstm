CONUS Streamflow with CAMELS — LSTM for Gauged & Pseudo-Ungauged Basins

Daily streamflow forecasting across 531 CONUS basins with an LSTM that generalizes to pseudo-ungauged sites. Built with PyTorch + NeuralHydrology and trained on UAHPC GPUs.


<img width="1469" height="841" alt="image" src="https://github.com/user-attachments/assets/451f009c-0a71-495a-8663-52afbdfb5c4d" />


Why this matters

Hydrologic models often struggle to transfer learning to ungauged basins. This repo shows a simple, reproducible LSTM pipeline that:

Learns basin-invariant representations from CAMELS forcings + attributes

Generalizes to basins with no discharge seen in training

Beats a calibrated hydrologic baseline on CONUS‐scale evaluation

Highlights

Context window: 365 days • Lead time: +1 day

Splits: 480 train/val basins, 51 pseudo-ungauged test basins

Train: 1980–2008 • Validation: 2009–2014 • Test: 1980–2014

Results: NSE = 0.90 (gauged) • NSE = 0.70 (pseudo-ungauged)

Baseline: surpasses calibrated hydrologic model (NSE > 0.65)

Stack: PyTorch + NeuralHydrology
, pandas, xarray, numpy
