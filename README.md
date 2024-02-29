# Neural Graph Generator

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-red.svg)](#python)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Code for the paper [Neural Graph Generator: Feature-Conditioned Graph Generation
using Latent Diffusion Models](https://arxiv.org/abs/).

## Overview of the proposed architecture

![alt text for screen readers](/img/ldm.pdf "Overview of the proposed architecture. The variational graph autoencoder is responsible for generating a compressed latent representation for each graph. Those representations are fed to the diffusion model which operates in that latent space. The denoising process is conditioned on a vector that contains the graph's properties. The output of the diffusion model is passed on to the decoder which generates a graph.")

### Requirements
Code is written in Python 3.8 and requires:
* NetworkX 2.6
* python-louvain 0.16
* Torch-geometric 2.2.0
* Pytorch 1.13.1
* GraKeL 0.1.8 

### Datasets
Request access from the authors of this paper. Soon available on Pytorch Geometric



### Run the model
First, specify the dataset and the hyperparameters in the `main.py` file. Then, use the following command:

```
$ python main.py
```

Arguments:
```
--lr "Initial Learning rate"
--dropout "Dropout rate"
--batch-size "Input batch size for training"
--epochs-autoencoder "Number of epochs to train autoencoder"
--hidden-dim-encoder "Size of hidden layer of encoder"
--hidden-dim-decoder "Size of hidden layer of decoder"
--latent-dim "Size of latent representation"
--n-max-nodes "Maximum number of nodes for the graphs of our dataset"
--n-layers-encoder "Number of layers of encoder"
--n-layers-decoder "Number of layers of decoder"
--spectral-emb-dim "Size of spectral embeddings"
--variational-autoencoder "Set this argument if you want to use the Variational Autoencoder"
--epochs-denoise "Number of epochs to train diffusion model"
--timesteps "Number of timesteps for the diffusion process"
--hidden-dim-denoise "Size of hidden layer of denoiser"
--n-layers_denoise "Number of layers of denoiser"
--train-autoencoder "Set this argument if you want to train autoencoder"
--train-denoiser "Set this argument if you want to train diffusion model"
--n-properties "Number of graph properties"
--dim-condition "Size of hidden layer of conditioner MLP"

```

### Cite
Please cite our paper if you use this code:
```

```
