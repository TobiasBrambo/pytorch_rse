# PyTroch Random Self-Ensemble (RSE)

This repository provides an implementation of the Random Self-Ensemble (RSE) technique for PyTorch, designed to enhance model robustness against adversarial attacks by introducing random noise layers during training.

### Overview
RSE is a method that incorporates random noise into the training process of neural networks, aiming to improve their resilience to adversarial perturbations. This implementation follows the approach outlined in this paper: https://arxiv.org/abs/1712.00673v2


### Installation

```
pip install pytorch-rse
```

### Usage

To apply RSE to your PyTorch model you do the following.


```
from pytorch_rse.rse import RSE

model = "Some_pytorch_model"

rse_model = RSE(model, std_devs=("some_init_noise", "some_inner_noise"))
```

After applying this, you can use your new `rse_model` in your regular training loop. The parameters can be tweaked to your desired values for initial and inner noise, default values are 0.1 for both.
