# Weather-Aware Image Translation Pipeline

An end-to-end image generation system that performs domain translation between various weather and time-of-day conditions using CycleGAN and super-resolution enhancement with SR3GAN. The model is trained on a custom dataset of over 89,000 images, including augmented variants, and evaluated on multiple loss metrics.
 
 ![Status](https://img.shields.io/badge/demo-inactive-red)
 
## Overview

This project enables realistic image-to-image translation under different environmental conditions such as:

- **Day ↔ Night**
- **Clear ↔ Foggy / Rainy / Snowy**
- Resolution enhancement using **SR3GAN**

The system is modular and can be adapted to other image translation tasks with appropriate datasets.

## Features

- CycleGAN-based translation for **day/night** and **weather condition** simulation.
- SR3GAN-based **super-resolution upscaling** for enhanced image quality.
- Custom dataset of **89K+ images**, generated through augmentation and manual curation.
- Evaluation using:
  - **Reconstruction Loss**: 0.565
  - **Latent Loss**: 0.053
- Demo visualization setup using **Gardio** (lightweight frontend prototype).

## Model Architecture

- **CycleGAN**: Used for image domain translation.
- **SR3GAN**: Applied as a post-processing step for super-resolution enhancement.

## Dataset

- Total images: 89,000+
- Sources: Open datasets + self-generated image augmentations (fog, rain, snow overlays, day/night filters).
- Split: 80% training / 20% validation

## Results

| Metric              | Value   |
|---------------------|---------|
| Reconstruction Loss | 0.565   |
| Latent Loss         | 0.053   |

Qualitative results show effective transformation across both weather and lighting domains with perceptual consistency.

## Demo

A simple interactive interface was built using **Gardio** to visualize input-output transformations and test the model with custom images. 
> **Note:** The Gradio demo is currently **inactive**.

## Installation

```bash
git clone https://github.com/your-username/weather-image-translation.git
cd weather-image-translation
# Install dependencies
pip install -r requirements.txt
```

## Outputs 

![NIGHT-DAY IMG 2](https://github.com/user-attachments/assets/785119ee-610b-41f0-ab20-6476ac02242e)
![NIGHT-DAY IMG 1](https://github.com/user-attachments/assets/5c4adedc-dfcf-4a2a-b519-8e9d0c453035)
![DAY-NIGHT IMG 2](https://github.com/user-attachments/assets/314fb098-2549-4de9-ac34-b1e1e218f326)
![DAY-NIGHT IMG 1](https://github.com/user-attachments/assets/cbeca322-dafa-44cf-9a7e-981d79a75f20)
![CLEAR-RAINY IMG 1](https://github.com/user-attachments/assets/d07538d8-2f11-4ab2-8567-c49d85337086)
![RAINY-CLEAR IMG 1](https://github.com/user-attachments/assets/18006331-f6ca-4051-b1ca-e96230ee0ec2)
![NORMAL-HEAVY-FOG](https://github.com/user-attachments/assets/e8c032d4-df89-40b8-8c66-580729470dc9)
