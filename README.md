# Video-Analysis

This project implements a pipeline for analyzing short videos and answering user prompts. It combines:

- **LLaVa** (Vision-Language Model) for multimodal understanding
- **T5** for summarization
- **OpenCV** for keyframe extraction

The goal is to generate concise summaries and answer questions about small video clips.

---

## Description

Processing video data is resource-intensive. On Google Colab’s free‐tier T4 GPU, memory constraints can impact performance. Below is a brief comparison of different model combinations and their trade-offs:

- **BART + CNN**  
  – Tends to hallucinate and produce inaccurate or repetitive descriptions.

- **Moondream + OpenCV**  
  – Very slow inference, especially on limited hardware.

- **QwenVL + YOLO**  
  – Best accuracy when sufficient GPU memory is available, but runs out of memory on Colab T4.

- **Blip + OpenCV**  
  – Fast inference but generates extremely brief, generic one-line descriptions.

---

## Sample Outputs

### Sample #1

![Sample #1 Output](https://github.com/user-attachments/assets/2df0b481-832a-4d7a-906a-ee95917f74b0)

> **Generated Description:**  
> The video captures a snowy street scene with a car driving down the road. The street is lined with houses, and there are multiple cars parked or driving along the roadway. The overall atmosphere of the scene is calm and quiet, with no visible signs of activity.

---

### Sample #2 (BART + CNN Hallucination)

![Sample #2 Output](https://github.com/user-attachments/assets/394ed4db-8390-4126-a65c-aff51ed61028)

> **Generated Description (BART + CNN, with hallucinations):**  
> A video shows a large fire burning in a city, with smoke billowing into the sky. The fire appears to be near a building, as there is smoke coming from that direction. The video captures the intensity of the fire and the impact it has on the cityscape. In this video, there is a large fire burning in a city, with black smoke billowing from the fire. The fire is located near an apartment building and seems to be spreading rapidly. The scene is quite dramatic, with the fire’s intensity making it difficult to focus on the details. Tuation for the city and its residents. tuation for city and their residents. The city is in the midst of a major crisis. It is the first time in its history that the city has been forced to close its doors for more than a year.

> *Note: This output contains clear hallucinations and repetitive text, illustrating why BART + CNN may not be reliable for detailed video descriptions.*

---

## Hardware & Performance Notes

- **Colab T4 Limitations**:  
  - 16 GB RAM and 16 GB total GPU memory shared between code, models, and input data  
  - Large vision-language models (e.g., QwenVL + YOLO) often exceed memory limits  

- **Recommended Setup for Best Results**:  
  - GPU with ≥ 24 GB VRAM (e.g., NVIDIA RTX 3090 or A6000)  
  - At least 32 GB system RAM  
  - SSD storage for faster I/O when extracting keyframes and loading video files  

---

