
# CyCLIP &mdash; Official PyTorch Implementation
![Python 3.10](https://img.shields.io/badge/python-3.10-green.svg?style=plastic)
![PyTorch 1.10](https://img.shields.io/badge/pytorch-1.11.0+cu115-green.svg?style=plastic)
![License CC BY-NC](https://img.shields.io/badge/license-CC_BY--NC-green.svg?style=plastic)

<h1 align="center"><img src="./docs/images/intro.png" width="75%"></h1>

This repository contains the official PyTorch implementation of the following paper:

> **CyCLIP: Cyclic Contrastive Language-Image Pretraining**<br>
> Shashank Goel (UCLA), Hritik Bansal (UCLA), Sumit Bhatia (MDSR Lab, Adobe Systems), Ryan A. Rossi (Adobe Research), Vishwa Vinay (Adobe Research), Aditya Grover (UCLA)<br>
> [https://arxiv.org/abs/2205.14459](https://arxiv.org/abs/2205.14459)
>
> **Abstract:** *Recent advances in contrastive representation learning over paired image-text data have led to models such as CLIP that achieve state-of-the-art performance for zero-shot classification and distributional robustness. Such models typically require joint reasoning in the image and text representation spaces for downstream inference tasks. Contrary to prior beliefs, we demonstrate that the image and text representations learned via a standard contrastive objective are not interchangeable and can lead to inconsistent downstream predictions. To mitigate this issue, we formalize consistency and propose CyCLIP, a framework for contrastive representation learning that explicitly optimizes for the learned representations to be geometrically consistent in the image and text space. In particular, we show that consistent representations can be learned by explicitly symmetrizing (a) the similarity between the two mismatched image-text pairs (cross-modal consistency); and (b) the similarity between the image-image pair and the text-text pair (in-modal consistency). Empirically, we show that the improved consistency in CyCLIP translates to significant gains over CLIP, with gains ranging from 10%-24% for zero-shot classification accuracy on standard benchmarks (CIFAR-10, CIFAR-100, ImageNet1K) and 10%-27% for robustness to various natural distribution shifts*

## Acknowledgements

Some portions of the code in this repository are adaptations from the following repositories: [mlfoundations](https://github.com/mlfoundations/open_clip) and [openai](https://github.com/openai/CLIP).

## Licenses

You can use, redistribute, and adapt the material for non-commercial purposes, as long as you give appropriate credit by citing our paper and indicating any changes that you've made.

## Requirements
 
- Both Linux and Windows are supported, but we strongly recommend Linux for performance and compatibility reasons.
- 64-bit Python 3.7+ installation. 
- One or more high-end GPUs with at least 16GB of DRAM.

## Setup Environment and Install dependencies

### Clone the repository

```bash
git clone git@github.com:goel-shashank/CyCLIP.git
cd CyCLIP
```

### Conda (recommended)

Please follow the instructions at the following link to set up anaconda: [Anaconda Setup](https://docs.anaconda.com/anaconda/install/index.html)

The following commands create a conda environment inside the repository with the dependencies.

```bash
conda env create --prefix ./env -f environment.yml
source activate ./env
```

### Pip

The requirements can be directly installed without creating a conda environment.

```bash
pip install -r requirements.txt
```
