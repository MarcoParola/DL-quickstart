# **Deep learning frameworks** 

## **Plain PyTorch**
**TODO**

## **PyTorch Lightning**
[PyTorch Lightning](https://lightning.ai/docs/pytorch/stable/) is an open-source Python library that provides a lightweight wrapper for PyTorch code. It was designed to facilitate the developement of pytorch research projects making code more modular and readable, providing built-in support for best practices in deep learning training. The advantage of Lightning is that it guides the design of the project in a modular way, allowing to define training/validation/test steps and then performing autonomously otpimizations like the calls to disable gradient computations when not needed. Another advantage of Lightning is that it's perfectly integrated with TensorBoard and Wandb, logging automatically most of the important informations during the training without explicit calls to the methods of those libraries.

A quick introduction to pytorch lightning and its advantages with respect to plain PyTorch can be found [here](https://lightning.ai/docs/pytorch/stable/starter/introduction.html).
