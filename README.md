# My Custom AI Story Generator

*A Generative AI project where a standard language model was fine-tuned to become a specialized science fiction author.*

---

## 🚀 The Problem

When I started my journey into Generative AI, I realized that base models like GPT-2, while powerful, often produce generic, incoherent, and uninteresting text. My goal was to move beyond tutorials and build a custom AI that had a unique personality and could write high-quality stories in a specific style.

## 💡 My Solution

I built a complete, end-to-end pipeline to create my own specialized AI story writer. The process involved several major stages:

1.  **Local Inference:** I first learned to run a base model (`distilgpt2`) locally to overcome the limitations of public APIs.
2.  **Data Curation:** Realizing the base model's quality was poor, I curated a high-quality, focused dataset of classic science fiction novels from Project Gutenberg to serve as my training material.
3.  **Fine-Tuning:** Using Google Colab and the Hugging Face `transformers` library, I fine-tuned the base model on my custom sci-fi dataset, teaching it the style, vocabulary, and narrative patterns of the genre.
4.  **Interactive App:** I created a simple, user-friendly web app using Gradio to allow anyone to interact with my custom-trained AI.

## ✨ Key Features

*   **Custom-Trained AI:** This is not a generic model. It has been specifically trained to write in the style of classic sci-fi.
*   **Interactive UI:** Users can enter their own story ideas, choose a genre, and generate unique stories.
*   **Story Continuation:** The app can continue writing from a previously generated story, allowing for longer narratives.

## 🔧 My Learning Journey & The Challenges I Solved

This project was a deep dive into the real-world challenges of building AI. The process was iterative and required solving numerous problems:

*   **Overcoming Bad Model Quality:** My first experiments with the base model produced terrible, nonsensical results. This led me to the conclusion that fine-tuning was the only way to achieve the quality I wanted.
*   **Data-Driven Discovery:** My first training session with a random mix of books produced a "confused" model that merged different genres. My experiment to add the 'Panchatantra' fables to teach "plot" was a valuable lesson in how a model's output is a direct mirror of its training data. This led me to curate a final, highly-focused dataset of 10 classic sci-fi novels.
*   **Debugging Technical Errors:** I worked through and solved deep library errors, such as the famous `loss` error (by implementing a `DataCollator`) and `FileNotFound` errors (by learning about Colab's temporary storage).
*   **Resource Management:** When the free Google Colab GPU locked me out due to usage limits, I learned how to manage limited compute resources and even found a creative workaround (using a second account) to keep the project moving forward.
*   **Creating a Permanent Workflow:** To solve the problem of my trained models being deleted after a session timeout, I developed a professional workflow to save my final model to Google Drive, separating the "training" phase from the "inference" phase.

---

## 🏆 Project Showcase: The Evolution of the Model

### Stage 1: The Incoherent Base Model

The initial output from the generic, pre-trained `distilgpt2` model was nonsensical. It proved that fine-tuning was necessary.

<img width="1366" height="768" alt="Screenshot 2025-08-01 220307" src="https://github.com/user-attachments/assets/b7e0cd3b-0a2e-4740-ab8c-7a32549fb14a" />

### Stage 2: The Training Process

This is the proof of the fine-tuning process. The 'Training Loss' steadily decreases, showing that the model is learning from the curated sci-fi dataset.

<img width="1366" height="768" alt="Screenshot 2025-08-03 184607" src="https://github.com/user-attachments/assets/18e5f2be-9b6b-487e-bbde-fc10d6045ac7" />

### Stage 3: The Final, Specialized Author

After being trained on a focused dataset of 10 classic sci-fi novels, the final model is vastly superior. It understands tone, atmosphere, and narrative structure. The difference is night and day.

**Example 1: The "Other Dimension" Prompt**

<img width="1366" height="768" alt="Screenshot 2025-08-03 213253" src="https://github.com/user-attachments/assets/9cd8a2ed-5042-4444-bbdd-8116d890a2ee" />

**Example 2: The "Derelict Starship" Prompt**

<img width="1366" height="768" alt="Screenshot 2025-08-03 213823" src="https://github.com/user-attachments/assets/a39d967e-5d8c-4025-a7ce-b95d2497c066" />

---

## 🛠️ How To Use

1.  Clone this repository.
2.  Install the required libraries (`pip install -r requirements.txt`).
3.  Download the trained model from the link provided in the code.
4.  Run the Gradio application.
