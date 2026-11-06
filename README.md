<!-- MINDSLAB-PAPER-METADATA:START -->
# IA-GPL

**Paper:** Instance-Aware Graph Prompt Learning

**Authors:** Jiazheng Li, Jundong Li, Chuxu Zhang

**Paper link:** [2411.17676](https://arxiv.org/abs/2411.17676)

<!-- MINDSLAB-PAPER-METADATA:END -->

---

# IA-GPL

This repository contains the pytorch code for '**Instance-Aware Graph Prompt Learning**' which is accepted in TMLR. We insert instance-aware prompts to improve performance and efficiency in downstream graph-related tasks.

## Model Architecture
![model figure](./model_fig.png)

## Setup

<!-- Create a new conda environment and run `pip install -r requirements.txt` to install the packages. -->

```python
conda create -n IAGPL python=3.11
conda activate IAGPL
conda install -r requirements.txt
```

## Datasets
We have provided 6 relatively smaller molecule datasets under `dataset/` folder. Please download HIV and MUV datasets from [repo](https://github.com/snap-stanford/pretrain-gnns) and put them under the same folder. 

## Usage

```
python prompt_tuning.py [--device DEVICE] [--epochs EPOCHS] ...
```
For a complete list of hyperparameters, please check the arguments section in the `prompt_tuning.py` file. 

## Reproduction

We have provided scripts with hyper-parameter settings to reproduce the experimental results presented in our paper. You can simply run:
```bash run_final.sh```

---
This codebase is based on [GPF](https://github.com/zjunet/GPF). The pre-trained GNNs and datasets are from [repo](https://github.com/snap-stanford/pretrain-gnns).
 We thank these authors for their great works.
