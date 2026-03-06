## MegaCRN Results

This repository contains a trained MegaCRN model and test results. 

### Implementation notes
We use the publicly available MegaCRN (https://github.com/deepkashiwa20/MegaCRN) codebase as our training framework. No changes were made to model architectures, loss functions, or optimisation procedures. Pretrained checkpoints are hosted externally due to size constraints.

### Repo structure
Coming soon. 

### Environment
- Python: 3.8.8
- Device: NVIDIA GeForce GTX1060 3GB (Windows 11 Enterprise x64, Intel i7)
- Conda environment: exported in `environment.yaml`
- Python dependencies: listed in `requirements.txt`
  
### Results

#### Model: MegaCRN (Jiang et al., 2023)
- Dataset: PEMSBAY
- Epochs/Run: 200
- Patience: 10
- Criterion: validation loss

Early stopping reached at epoch 70.

| Benchmark| MAE | RMSE | MAPE |
|-----------|-----------------------------|------------------------------|-------------------------------|
| METR-LA   | 1.5495          |   3.6234        |  0.0352         |

#### Model: MegaCRN (Jiang et al., 2023)
- Dataset: METR-LA
- Epochs/Run: 200
- Patience: 10
- Criterion: validation loss

Early stopping reached at epoch 71.

| Benchmark| MAE | RMSE | MAPE |
|-----------|-----------------------------|------------------------------|-------------------------------|
| METR-LA   | 2.8982          |   6.0406        |  0.0791         |



### Reference

The implementation is based on the AAAI 2023 paper “Spatio-Temporal Meta-Graph Learning for Traffic Forecasting”, with the following citation:

```bibtex
@inproceedings{jiang2023spatio,
  title={Spatio-temporal meta-graph learning for traffic forecasting},
  author={Jiang, Renhe and Wang, Zhaonan and Yong, Jiawei and Jeph, Puneet and Chen, Quanjun and Kobayashi, Yasumasa and Song, Xuan and Fukushima, Shintaro and Suzumura, Toyotaro},
  booktitle={Proceedings of the AAAI conference on artificial intelligence},
  volume={37},
  number={7},
  pages={8078--8086},
  year={2023}
}
```
