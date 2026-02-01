# Image Caption Generator using LLaVA

This project is a full-stack **Image Caption Generator** that allows users to upload an image and receive a natural-language description of the image.  
It uses a **vision–language model (LLaVA)** running locally via **Ollama**, with a **FastAPI backend** and a **Streamlit frontend**.

---

## Project Overview

The goal of this project is to demonstrate how **multimodal AI models** (image + text) can be integrated into real-world applications using modern backend and frontend frameworks.

The system:
1. Accepts an image from the user
2. Sends the image to a backend API
3. Uses a vision-language model to understand the image
4. Generates a descriptive caption in natural language

---

## Tech Stack

- **LLaVA** – Vision-language model for image understanding and caption generation  
- **Ollama** – Local model hosting and inference  
- **FastAPI** – Backend REST API  
- **Streamlit** – Frontend user interface  
- **Python** – Core programming language  
- **Git & GitHub** – Version control  

---

## Architecture

```

User
↓
Streamlit Frontend
↓
FastAPI Backend
↓
LLaVA Model (via Ollama)

```

- The frontend handles user interaction
- The backend handles image processing and model communication
- The AI model runs locally for inference

---

## Project Structure

```

image-caption-llava/
├── backend/
│   └── main.py        # FastAPI backend
├── frontend/
│   └── app.py         # Streamlit frontend
├── requirements.txt   # Python dependencies
├── .gitignore
└── README.md

````

---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/NehaCh11/image-caption-llava.git
cd image-caption-llava
````

### 2. Create and Activate Virtual Environment

```bash
python -m venv venv
source venv/bin/activate    # Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Run the Project

### Step 1: Install and Run Ollama

Download and install Ollama from:
[https://ollama.com](https://ollama.com)

Pull the LLaVA model:

```bash
ollama pull llava
```

Ensure Ollama is running in the background.

---

### Step 2: Start the Backend (FastAPI)

```bash
uvicorn backend.main:app --reload
```

Backend will run at:

```
http://localhost:8000
```

---

### Step 3: Start the Frontend (Streamlit)

```bash
streamlit run frontend/app.py
```

Frontend will open at:

```
http://localhost:8501
```

---

## How It Works

1. The user uploads an image using the Streamlit UI
2. The image is sent to the FastAPI backend
3. The backend encodes the image in Base64
4. The image and prompt are sent to the LLaVA model via Ollama
5. The model generates a caption
6. The caption is returned and displayed to the user

---

## Features

* Local AI inference (no paid APIs)
* Vision-language understanding
* Clean backend–frontend separation
* Simple and interactive UI
* Easy to extend and scale

---

## Future Improvements

* Support for longer and more detailed captions
* Multiple caption styles (creative, technical, concise)
* Batch image captioning
* Dockerized deployment
* Cloud deployment option


---

## License

This project is for educational purposes.



Just tell me 👍
```
