MultiPDF Chat App — Built by Dipanshu
Link - https://chat-to-pdf-c91v.onrender.com/
A smart PDF chatbot that lets you interact with multiple documents using natural language — ask questions, get instant answers, all grounded in the actual PDF content.

---

About the Project

This project is a full-fledged **AI-powered PDF QA system** that I built using **Python**, **LangChain**, **FAISS**, and **Streamlit**. It allows users to upload multiple PDF files and ask questions in plain English. The app uses **GPT models** under the hood to generate answers strictly based on the content of the uploaded PDFs — ensuring relevant, grounded responses.

How It Works

Here's a quick breakdown of the workflow:

1. **PDF Parsing:** The app extracts raw text from all uploaded PDF files using `PyPDF2`.
2. **Text Chunking:** It breaks the extracted text into manageable chunks to fit LLM input limits.
3. **Embeddings:** These chunks are converted into vector representations using **OpenAI Embeddings**.
4. **Vector Store (FAISS):** The vectors are stored in a FAISS index for efficient similarity search.
5. **Query Matching:** When a user asks a question, it’s converted into a vector and compared to the indexed chunks.
6. **Answer Generation:** The most relevant chunks are sent to **GPT-3.5/4** via **LangChain** to generate a concise, context-aware response.
7. **Frontend:** A clean and responsive UI is built with **Streamlit** for easy interaction.

---

Tech Stack

* **Frontend:** Streamlit
* **Backend:** Python, LangChain
* **LLM:** OpenAI GPT-3.5/4
* **Vector Store:** FAISS
* **PDF Processing:** PyPDF2
* **Embeddings:** OpenAI Embeddings

---

Installation & Setup

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/dipanshu180/MultiPDF-Chat-App.git
   cd MultiPDF-Chat-App
   ```

2. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Add Your OpenAI API Key:**

   Create a `.env` file and add your key:

   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   ```

4. **Run the App:**

   ```bash
   streamlit run app.py
   ```

---

How to Use

* Launch the app in your browser.
* Upload one or more PDF documents.
* Ask any question related to the content.
* Get instant, intelligent answers based on your PDFs.

---

Notes

* The app only responds based on the PDFs you upload — no external or general knowledge.
* Responses improve if PDFs are well-structured and text-based (not image-only).
