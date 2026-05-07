# Diffusion Model with 8X Enhancement (SRDiff)

This repository contains the implementation of a diffusion-based super-resolution model (SRDiff) optimized for 8x upscaling. The project explores the use of iterative refinement via diffusion models to generate high-fidelity, high-resolution images from low-resolution inputs.

**Alternative Kaggle Notebook Link**: [View SRDiff on Kaggle](https://www.kaggle.com/code/ajmeerajailsingh007/srdiff?scriptVersionId=317000635)

## Project Structure

The project is divided into two main components:

### 1. Diffusion with Training
Contains notebooks for training the diffusion model on the DIV2K dataset:
- `Diffusion_with _training.ipynb`: Base training pipeline for the diffusion model.
- `Diffusion with more timesteps(as mentioned T=1000 in research paper).ipynb`: Implementation exploring an extended diffusion schedule (T=1000) for improved noise scheduling and generation quality.
- `diffusion_sr_300epochs.ipynb`: Training notebook scaled to 300 epochs for better convergence.

### 2. Diffusion with 8X
Contains the inference pipeline and evaluation for 8x super-resolution:
- `Diffusion (16).ipynb`: Complete pipeline for 8x upscaling, including evaluation metrics (PSNR, SSIM, LPIPS) to measure reconstruction quality and perceptual fidelity against baseline models (like RRDB).

## Dataset

The model is trained on the **DIV2K dataset**, which consists of high-resolution images and their corresponding low-resolution counterparts. 

*(Note: The DIV2K dataset and PyTorch model checkpoints (`.pth` files) are ignored in this repository due to GitHub file size constraints.)*

## Key Features

- **8x Super-Resolution**: Upscales images by a factor of 8x while preserving visual details.
- **Diffusion-Based Generation**: Utilizes iterative refinement to remove noise and generate crisp, high-resolution outputs.
- **Evaluation Metrics**: Comprehensive evaluation using PSNR, SSIM, and LPIPS to ensure state-of-the-art performance.
