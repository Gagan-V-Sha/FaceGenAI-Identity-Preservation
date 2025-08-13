# FaceGenAI: Identity-Preserving Face Generation

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A project exploring and implementing advanced pipelines for generating high-fidelity, identity-preserving human faces with pose control and photorealistic enhancement using ComfyUI.

## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Project Evolution](#project-evolution)
- [Results Gallery](#results-gallery)
- [Setup and Usage](#setup-and-usage)
- [Future Work](#future-work)
- [Acknowledgments](#acknowledgments)

## Project Overview
The primary challenge in generative AI for face synthesis is preserving a person's identity across different outputs (e.g., poses, expressions, styles). This project documents an iterative process to build a robust pipeline that addresses this challenge, starting from foundational model comparisons to a complete system with pose control and realism enhancement.

## Key Features
- **Identity Preservation:** Consistently maintains facial identity using models like PhotoMaker.
- **High-Fidelity Output:** Leverages the power of SDXL for high-resolution image generation.
- **Precise Pose Control:** Utilizes ControlNet to guide the generation process into diverse and specific poses.
- **Photorealistic Enhancement:** Integrates GFPGAN as a post-processing step to fix artifacts and dramatically improve facial quality and realism.

## Tech Stack
- **Workflow Engine:** [ComfyUI](https://github.com/comfyanonymous/ComfyUI)
- **Core Models:** SDXL, PhotoMaker, ControlNet, GFPGAN
- **Initial Research Models:** ArcFace, StyleGAN, InstantID

## Project Evolution
This project was developed in three main stages, each building upon the last.

### Part 1: Initial Exploration (LinkedIn Post 1)
The first phase involved researching and comparing existing state-of-the-art models for identity preservation. I experimented with various architectures like InstantID and StyleGAN within ComfyUI to evaluate their effectiveness at retaining identity.
*(Here, you can embed a comparison image from `results/part1_comparison/`)*
`![Comparison](results/part1_comparison/comparison.png)`

### Part 2: Advanced Pipeline with Pose Control (LinkedIn Post 2)
Building on the initial findings, I constructed a more powerful pipeline. By combining **SDXL** (for quality), **PhotoMaker** (for identity), and **ControlNet** (for pose), I was able to generate images of the same identity in various controlled poses.
*(Embed an image showing the same face in different poses)*
`![Pose Control](results/part2_pose_control/pose_grid.png)`

### Part 3: Achieving Photorealism with GFPGAN (LinkedIn Post 3)
The final step was to perfect the output quality. I integrated **GFPGAN** as a post-processing step. This significantly enhanced facial details, removed artifacts, and resulted in truly photorealistic outputs.
*(Embed a powerful before-and-after comparison image)*
`![GFPGAN Enhancement](results/part3_realism_enhancement/before_vs_after.png)`

## Results Gallery
Here are some of the best results from the final pipeline.
*(Showcase 2-4 of your best images here)*

## Setup and Usage
To replicate these results, you will need a working installation of ComfyUI.

1.  **Prerequisites:**
    - [ComfyUI](https://github.com/comfyanonymous/ComfyUI) installed.
    - [ComfyUI Manager](https://github.com/ltdrdata/ComfyUI-Manager) for easy custom node installation.

2.  **Install Custom Nodes:**
    Use the ComfyUI Manager to install the necessary custom nodes for PhotoMaker, ControlNet, etc.

3.  **Download Models:**
    The required models (SDXL, ControlNet models, PhotoMaker, GFPGAN) are too large for this repository. You must download them from their official sources (e.g., Hugging Face) and place them in the `ComfyUI/models/` directory.

4.  **Load a Workflow:**
    Drag one of the workflow files from the `/comfyui_workflows` folder directly onto the ComfyUI interface in your browser.

## Future Work
- [ ] Explore video generation using models like AnimateDiff while preserving identity.
- [ ] Build a simple Gradio or Streamlit interface for easier use.
- [ ] Fine-tune a model specifically on a custom dataset for improved consistency.

## Acknowledgments
This project builds on the incredible work of the teams behind ComfyUI, Stable Diffusion, PhotoMaker, ControlNet, and GFPGAN.
