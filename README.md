# DDPM_and_GAN_for_landscape_pictures

In [this](https://github.com/m4andreyushkova/DDPM_and_GAN_for_landscape_pictures/blob/main/DDPM_landscapes.ipynb) notebook I implemented DDPM from [this](https://arxiv.org/abs/2006.11239) article for lanscape pictures generation. And in [this](https://github.com/m4andreyushkova/DDPM_and_GAN_for_landscape_pictures/blob/main/Landscape_gan.ipynb) notebook I implemented GAN with convolutional layers for the same task. [This](https://www.kaggle.com/datasets/arnaud58/landscape-pictures) dataset was used for training.

As for GAN, both the discriminator and the generator consist of 4 convolutional blocks, each having a structure of 'convolutional layer + batch normalization + Leaky ReLU'. The final convolutional layer uses hyperbolic tangent or sigmoid activation. There are no pooling or fully connected layers. 

Below are the GAN's training results over 200 epochs:

![](https://github.com/m4andreyushkova/DDPM_and_GAN_for_landscape_pictures/assets/126197652/bd91872d-1d8b-4cc9-b01d-f13fc01f29c4)

As for DDPM, it uses a linear scheduler for betas and UNet architecture with skip connections for predicting noise. UNet also includes sinusoidal position embeddings to encode t.

Below are the DDPM's training results over 200 epochs:

![](https://github.com/m4andreyushkova/DDPM_and_GAN_for_landscape_pictures/assets/126197652/de7f2dc8-8937-46b6-85f3-f410ab7cb0d9)

GAN has shown better results, as can be seen both in the generated images and in the value of the FID metric. DDPM could have shown better results, but it would require more epochs and, therefore, larger computing power.
