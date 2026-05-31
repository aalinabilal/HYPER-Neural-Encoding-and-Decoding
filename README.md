# HYPER
 Hyperrealistic Neural Coding of Perception (Neural Encoding and Decoding)

Overview
This project explores how the human brain represents perceived faces by building two complementary models:

Neural encoding (face → brain): Given a face image, predict the fMRI brain response it would evoke
Neural decoding (brain → face): Given an fMRI brain response, reconstruct the face the participant was perceiving

Both pipelines are grounded in the latent space of NVIDIA's Progressively Growing GAN (PGGAN) — a generative model trained to synthesize photorealistic faces. The dataset consists of (latent vector, fMRI response) pairs recorded while participants viewed GAN-generated faces in an MRI scanner.


Stack
ComponentTools Generative: modelPGGAN (MXNet/Gluon)
Feature extraction: AlexNet (pretrained, MXNet)
Encoding/decoding models: scikit-learn (Ridge, RidgeCV)
fMRI data handling: nibabel, nilearn
Visualization: nilearn glass brain, matplotlib
Environment Google Colab (GPU), CUDA 11.2

Key Concepts Demonstrated: 
Encoding models as a tool for mapping stimulus feature spaces to neural response spaces
Representational hierarchy in visual cortex via AlexNet layer analysis
Generative models as a structured latent space for neural decoding
Per-voxel regression at scale with chunked inference for memory efficiency
Brain visualization with atlas-based parcellation (Glasser atlas)
