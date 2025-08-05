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
<img width="1366" height="768" alt="Screenshot 2025-08-01 220307" src="https://github.com/user-attachments/assets/b7e0cd3b-0a2e-4740-ab8c-7a32549fb14a" />

##Training

After seeing terrible results i dicided to fine-tune the model to specifically sci-fi genre

<img width="1366" height="768" alt="Screenshot 2025-08-02 173834" src="https://github.com/user-attachments/assets/ab8f7dcb-10fd-4b21-b277-2a0364858f71" />

and then i got this (because of session timeout )

<img width="1366" height="768" alt="Screenshot 2025-08-02 174059" src="https://github.com/user-attachments/assets/fdfd649f-46c2-4faa-881c-3a1f18c72d21" />

##After training 
(For session 1 i randomly selected the books and i think 5 of them from project gutenburg)
<img width="1366" height="768" alt="Screenshot 2025-08-02 181233" src="https://github.com/user-attachments/assets/bbae3483-2d32-4cc0-9701-d18e0e530e25" />
results are improved better than last time
<img width="1366" height="768" alt="Screenshot 2025-08-02 181312" src="https://github.com/user-attachments/assets/34b10537-8211-4a5f-9305-49c8ca382f99" />
<img width="1366" height="768" alt="Screenshot 2025-08-02 181348" src="https://github.com/user-attachments/assets/b0132c9f-afdb-4dd4-893a-6fb85a3777f4" />
<img width="1366" height="768" alt="Screenshot 2025-08-03 003031" src="https://github.com/user-attachments/assets/95c46835-b3c7-4c62-8957-1fb3ace4fe60" />
After that i added 'panchatantra' stories which are direct story and to help the model to learn story writing
<img width="1366" height="768" alt="Screenshot 2025-08-03 132819" src="https://github.com/user-attachments/assets/4b1bae1a-8633-4551-852c-9ffa4da478ee" />
these are the results i got mixed up with writing 
<img width="1366" height="768" alt="Screenshot 2025-08-03 143445" src="https://github.com/user-attachments/assets/a80fddd2-7033-48b0-80d3-b54acd9a254f" />
and again usage limit hit me again
<img width="1366" height="768" alt="Screenshot 2025-08-03 152732" src="https://github.com/user-attachments/assets/c4dee0bc-b40f-443a-a0a3-4b4d59a49f8e" />
again i started in another google account but now i espessiaaly taken ten books which are perfect to train model with sci-fi genre writing 
<img width="1366" height="768" alt="Screenshot 2025-08-03 184607" src="https://github.com/user-attachments/assets/18e5f2be-9b6b-487e-bbde-fc10d6045ac7" />
results
<img width="1366" height="768" alt="Screenshot 2025-08-03 213253" src="https://github.com/user-attachments/assets/9cd8a2ed-5042-4444-bbdd-8116d890a2ee" />
<img width="1366" height="768" alt="Screenshot 2025-08-03 213823" src="https://github.com/user-attachments/assets/a39d967e-5d8c-4025-a7ce-b95d2497c066" />


## 🛠️ How To Use

1.  Clone this repository.
2.  Install the required libraries (`pip install -r requirements.txt`).
3.  Run the Gradio application.
