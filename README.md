# AllSet

This is the repo for our paper: [You are AllSet: A Multiset Function Framework for Hypergraph Neural Networks](https://openreview.net/forum?id=hpBTIv2uy_E). We prepared all codes and a subset of datasets used in our experiments.

All codes and script are in the folder `src`, and a subset of raw data are provided in folder `data`. To run the experiments, please go the the `src` folder first. 
## Enviroment requirement:
This repo is tested with the following enviroment, higher version of torch PyG may also be compatible. 
```
pytorch==1.4.0+cu100
torch-geometric==1.6.3
torch-scatter==2.0.4
```
## Generate dataset from raw data.

To generate PyG or DGL dataset for training, please create the following three folders:
```
p2root: '../data/pyg_data/hypergraph_dataset_updated/'
p2raw: '../data/AllSet_all_raw_data/'
p2dgl_data: '../data/dgl_data_raw/'
```

And then unzip the raw data zip file into `p2raw`.


## Run one single experiment with one model with specified lr and wd: 
```
source run_one_model.sh [dataset] [method] [MLP_hidden_dim] [Classifier_hidden_dim] [feature noise level]
```

## To reproduce the results in Table 2 (with the processed raw data)
```
source run_all_experiments.sh [method]
```

## Citation
If you use our code or data in your work, please cite our paper:
```
@inproceedings{
chien2022you,
title={You are AllSet: A Multiset Function Framework for Hypergraph Neural Networks},
author={Eli Chien and Chao Pan and Jianhao Peng and Olgica Milenkovic},
booktitle={International Conference on Learning Representations},
year={2022},
url={https://openreview.net/forum?id=hpBTIv2uy_E}
}
```

