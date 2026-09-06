# Unconditional Texture Synthesis using Generative Models

This project explores unconditional texture synthesis using a two-stage generative pipeline.

In the first stage, a discrete latent representation is learned from texture images using vector quantization. Three first-stage architectures are compared:

- **VQ-VAE**
- **Custom VQGAN**
- **VQGAN inspired by Taming Transformers**

In the second stage, a GPT-like autoregressive Transformer is trained on the resulting sequences of discrete latent codes. At inference time, the Transformer generates new code sequences starting from a BOS token, which are then decoded into texture images.

The goal of the project is to investigate how different discrete representations affect both latent-space modeling and final texture generation.

## Project structure

```text
Texture-synthesis/
│
├── codebook/
│   ├── VQ_VAE.ipynb
│   ├── VQGAN.ipynb
│   ├── VQGAN_TT.ipynb
│   └── training.ipynb
│
├── generation/
│   ├── Transformers.ipynb
│   └── training.ipynb
│
└── samples/
    ├── vqvae/
    └── vqgan/



Link to the generated images: https://drive.google.com/drive/folders/1GxtyJPWyqteYqSWQCpBKHnUdG1ZhdXlr?usp=sharing
