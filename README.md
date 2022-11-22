# Learning to Accelerate Partial Differential Equations via Latent Global Evolution

This repository reproduces the results in the paper [Learning to Accelerate Partial Differential Equations via Latent Global Evolution](https://arxiv.org/abs/2206.07681) (Tailin Wu, Takashi Maruyama, Jure Leskovec, NeurIPS 2022), which introduces a simple, fast and scalable LE-PDE method to accelerate the simulation and inverse optimization of PDEs, which are crucial in many scientific and engineering applications (e.g., weather forecasting, material science, engine design). LE-PDE achieves up to 128x reduction in the dimensions to update, and up to 15x improvement in speed, while achieving competitive accuracy compared to state-of-the-art deep learning-based surrogate models.

<a href="url"><img src="https://github.com/snap-stanford/le_pde/blob/master/assets/le_pde.png" align="center" width="700" ></a>

If you find our work and/or our code useful, please cite us via:

```bibtex
@inproceedings{wu2022learning,
title={Learning to accelerate partial differential equations via latent global evolution},
author={Wu, Tailin and Maruyama, Takashi and Leskovec, Jure},
booktitle={Neural Information Processing Systems},
year={2022},
}
```

# Installation

1. First clone the directory. Then run the following command to initialize the submodules:

```code
git submodule init; git submodule update
```
(If showing error of no permission, need to first [add a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).)

2. Install dependencies.

First, create a new environment using conda . Then install pytorch, torch-geometric, deepsnap and other dependencies as follows. 

The repository is run with the following dependencies. Other version of torch-geometric or deepsnap may work but there is no guarentee.

Install pytorch (replace "cu113" with appropriate cuda version. For example, cuda11.1 will use "cu111"):
```code
pip install torch==1.10.2+cu113 torchvision==0.11.3+cu113 torchaudio==0.10.2+cu113 -f https://download.pytorch.org/whl/torch_stable.html
```

Install torch-geometric. Run the following command:
```code
pip install torch-scatter==2.0.9 -f https://data.pyg.org/whl/torch-1.10.2+cu113.html
pip install torch-sparse==0.6.12 -f https://data.pyg.org/whl/torch-1.10.2+cu113.html
pip install torch-geometric==1.7.2
pip install torch-cluster==1.5.9 -f https://data.pyg.org/whl/torch-1.10.2+cu113.html
```

Install other dependencies:
```code
pip install -r requirements.txt
```
