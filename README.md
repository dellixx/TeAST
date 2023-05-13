<h2 align="center">
TeAST: Temporal Knowledge Graph Embedding via Archimedean Spiral Timeline  <img src="https://pytorch.org/assets/images/logo-dark.svg" height = "20" align=center />
</h2>

<p align="center">
  <img src="https://img.shields.io/badge/ACL-2023-brightgreen">
  <a href = '' target='_blank'><img src="http://img.shields.io/badge/Paper-PDF-red.svg"></a>
  <img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg">
</p>


<p align="center">
Codes for the paper TeAST: Temporal Knowledge Graph Embedding via Archimedean Spiral Timeline accepted by the ACL 2023.
</p>


## 


### Installation
Create a conda environment with pytorch and scikit-learn :
```
conda create --name teast_env python=3.8
source activate teast_env
conda install --file requirements.txt -c pytorch
```


### Datasets

```
python process_icews.py

python process_gdelt.py
```

This will create the files required to compute the filtered metrics.

### Reproducing results of TeAST

In order to reproduce the results of TeAST on the four datasets in the paper,  run the following commands

```
python  learner.py --dataset ICEWS14    --emb_reg 0.0025 --time_reg 0.01

python  learner.py --dataset ICEWS05-15 --emb_reg 0.002  --time_reg 0.1

python  learner.py --dataset GDELT      --emb_reg 0.003  --time_reg 0.003
```

### Acknowledgement
We refer to the code of [TNTComplEx](https://github.com/facebookresearch/tkbc) and [TeLM](https://github.com/soledad921/TeLM). Thanks for their great contributions!

