# Discrete Graph Structure Learning for Forecasting Multiple Time Series

This is a PyTorch implementation of the paper "[Discrete Graph Structure Learning for Forecasting Multiple Time Series](https://openreview.net/pdf?id=WEHSlH5mOk)", ICLR 2021.
Variables considered- Voltage (V), Charge Capacity (Ah), Battery Level

## Installation

Install the dependency using the following command:

```bash
pip install -r requirements.txt
```

* torch
* scipy>=0.19.0
* numpy>=1.12.1
* pandas>=0.19.2
* pyyaml
* statsmodels
* tensorflow>=1.3.0
* tables
* future


## Data Preparation


Run the following commands to generate train/test/val dataset at  `data/{METR-LA}/{train,val,test}.npz`.
```bash



# METR-LA
python -m scripts.generate_training_data --output_dir=data/METR-LA --traffic_df_filename=data/metr-la.h5



## Train Model

When you train the model, you can run:

```bash
# Use METR-LA dataset
python train.py --config_filename=data/model/para_la.yaml --temperature=0.5




@article{shang2021discrete,
  title={Discrete Graph Structure Learning for Forecasting Multiple Time Series},
  author={Shang, Chao and Chen, Jie and Bi, Jinbo},
  journal={arXiv preprint arXiv:2101.06861},
  year={2021}
}
```

## Acknowledgments

[DCRNN-PyTorch](https://github.com/chnsh/DCRNN_PyTorch), [GCN](https://github.com/tkipf/gcn), [NRI](https://github.com/ethanfetaya/NRI) and [LDS-GNN](https://github.com/lucfra/LDS-GNN).
