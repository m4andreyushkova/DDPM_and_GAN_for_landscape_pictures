# DDPM_and_GAN_for_landscape_pictures

In this notebook I implemented DDPM from [this](https://arxiv.org/abs/2006.11239) article and GAN with convolutional layers for landscape pictures generation. [This](https://www.kaggle.com/datasets/arnaud58/landscape-pictures) dataset was used for training.

As for GAN, both the discriminator and the generator consist of 4 convolutional blocks, each having a structure of 'convolutional layer + batch normalization + Leaky ReLU'. The final convolutional layer uses hyperbolic tangent or sigmoid activation. There are no pooling or fully connected layers. 

Below are the GAN's training results over 200 epochs  

As for DDPM, it uses a linear scheduler for betas and UNet architecture for predicting noise. Unet also includes sinusoidal position embeddings to encode t.

Below are the DDPM's training results over 200 epochs
