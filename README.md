# 🟦 BLUE-AI Robot
> **A Multimodal Autonomous Assistant powered by Generative AI**

<img height="300" alt="Robot Poster Camera-Added" src="https://github.com/user-attachments/assets/9c17bcc3-1f1a-49dd-98f9-a45f83317625" />

## 📖 Overview
**BLUE-AI** is not just a remote-controlled car; it is an intelligent agent capable of "Visual Spatial Reasoning." 

Unlike traditional line-following robots, BLUE-AI uses a **Large Language Model (LLM)** to perceive its environment. It can capture an image, understand the context, and autonomously decide whether to move **Left, Right, or Forward** to reach a target object. It also features voice interaction, making it a true personal assistant.

## ✨ Key Features
* **🧠 Visual Reasoning:** Uses Vision-Language Models (VLM) to detect object placement (Left/Right/Center).
* **🗣️ Voice Interface:** Fully interactive voice command and response system.
* **🔍 Autonomous Exploration:** Can be commanded to "Find the bottle" and will search the room.
* **💬 Contextual Chat:** Capable of describing what it sees and answering general questions.

## ⚙️ Tech Stack
* **Hardware:** Raspberry Pi 4 , PI Camera, DC Motors, L298N Driver.
* **AI Models:** Ollama-Qwen 2.5 , Moondream
* **vision*** YOLOv8 
* **Language:** Python 3.9+
* **Libraries:** `opencv-python`, `speech_recognition`, `pyttsx3`

## 🚀 How It Works
The core logic follows a "See-Think-Act" loop:
1.  **Input:** User gives a voice command (e.g., "Find the Remote").
2.  **Vision:** Robot captures a frame using OpenCV.
3.  **Inference:** The image is sent to the yolov8 [Location calculated. Is it Left, Right, or Center?]*
4.  **Action:** The LLM response triggers the specific motor function in `motor_driver.py`.

## 📂 Repository Structure
```text
/src           # Source code for robot control
/docs          # Project documentation and Pinout diagrams
/assets        # Images and Demos
