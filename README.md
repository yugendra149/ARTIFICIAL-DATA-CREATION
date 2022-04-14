# Discrete Graph Structure Learning for Forecasting Multiple Time Series

This is a PyTorch implementation of the paper "[Discrete Graph Structure Learning for Forecasting Multiple Time Series](https://openreview.net/pdf?id=WEHSlH5mOk)", ICLR 2021.
Variables considered- Voltage (V), Charge Capacity (Ah), Battery Level

## Installation

Install the dependency using the following command:

```bash
pip install -r requirements.txt
```


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






## Acknowledgments
We appreciate the following github repos a lot for their valuable code base and datasets:
https://github.com/chaoshangcs/GTS

@article{shang2021discrete,
  title={Discrete Graph Structure Learning for Forecasting Multiple Time Series},
  author={Shang, Chao and Chen, Jie and Bi, Jinbo},
  journal={arXiv preprint arXiv:2101.06861},
  year={2021}


