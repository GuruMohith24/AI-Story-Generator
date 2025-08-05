# My Custom AI Story Generator

*A Generative AI project where a standard language model was fine-tuned to become a specialized science fiction author.*

---

## 🚀 The Problem

When I started my journey into Generative AI, I realized that base models like GPT-2, while powerful, often produce generic, incoherent, and uninteresting text. My goal was to move beyond tutorials and build a custom AI that had a unique personality and could write high-quality stories in a specific style.

## 💡 My Solution

I built a complete, end-to-end pipeline to create my own specialized AI story writer. The process involved three major stages:

1.  **Local Inference:** I first learned to run a base model (`distilgpt2`) locally to overcome the limitations of public APIs.
2.  **Data Curation:** Realizing the base model's quality was poor, I curated a high-quality, focused dataset of classic science fiction novels from Project Gutenberg to serve as my training material.
3.  **Fine-Tuning:** Using Google Colab and the Hugging Face `transformers` library, I fine-tuned the base model on my custom sci-fi dataset, teaching it the style, vocabulary, and narrative patterns of the genre.
4.  **Interactive App:** I created a simple, user-friendly web app using Gradio to allow anyone to interact with my custom-trained AI.

## ✨ Key Features

*   **Custom-Trained AI:** This is not a generic model. It has been specifically trained to write in the style of classic sci-fi.
*   **Interactive UI:** Users can enter their own story ideas, choose a genre, and generate unique stories.
*   **Story Continuation:** The app can continue writing from a previously generated story, allowing for longer narratives.

## 🔧 My Learning Journey & The Challenges I Solved

This project was a deep dive into the real-world challenges of building AI. Here are some of the key problems I solved:

*   **Overcoming Bad Model Quality:** My first experiments with the base model produced terrible results. I solved this by learning about fine-tuning and the importance of high-quality data.
*   **Debugging Technical Errors:** I worked through and solved deep library errors, such as the `loss` error (by implementing a `DataCollator`) and `FileNotFound` errors (by learning about Colab's temporary storage).
*   **Resource Management:** When the free Google Colab GPU locked me out due to usage limits, I learned how to manage resources and even found creative workarounds to keep my project moving forward.
*   **Creating a Permanent Workflow:** To solve the problem of my trained models being deleted, I developed a professional workflow to save my final model to Google Drive, separating the "training" phase from the "inference" phase.

##Before fine tuning the model
<img width="1366" height="768" alt="Screenshot 2025-08-01 220307" src="https://github.com/user-attachments/assets/fb593d91-8aa7-4b69-96ed-99d44c73db41" />


## 🛠️ How To Use

1.  Clone this repository.
2.  Install the required libraries (`pip install -r requirements.txt`).
3.  Run the Gradio application.
