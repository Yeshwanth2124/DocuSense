# DocuSense AI

**DocuSense** is an intelligent, document-based Q&A system that allows you to chat with your files (PDF, DOCX, TXT) using advanced local LLMs. It features a modern chat interface, voice interaction, and conversation memory.

## Features

-   **📄 Multi-Format Support**: Upload and analyze **PDF**, **DOCX**, and **TXT** files.
-   **🗣️ Voice Interaction**:
    -   **Voice Input**: Speak your questions using the microphone button.
    -   **Voice Output**: Listen to the AI's answers with the speaker button.
-   **🧠 Conversation Memory**: Ask follow-up questions (e.g., "Summarize *it*") with context awareness.
-   **🎨 Modern UI**: Beautiful, responsive "Glassmorphism" interface with Dark/Light accents.
-   **🔒 Local Privacy**: Powered by **Ollama**, ensuring your documents stay on your machine.
-   **Semantic Search**: Utilizes SentenceTransformers and FAISS for fast and accurate semantic search.

---
### Tech Stack

|     Layer      |                      Tools Used                      |
| -------------- | ---------------------------------------------------- |
| **Frontend**   | `React.js`, `HTML`, `CSS`                            |
| **Backend**    | `Flask`, `PyMuPDF` (fitz), `Transformers`            |
| **NLP Models** | `SentenceTransformers` (MiniLM), `Hugging Face LLMs` |
| **Search**     | `FAISS`                                              |
| **Deployment** | `Flask API` (local, extendable to Render/Heroku)     |

---
### Architecture Diagram
<img width="877" height="663" alt="arc" src="https://github.com/user-attachments/assets/b868e97d-8662-413e-90b7-4caeae6a9e27" />

---


## Project Structure

```bash
DocuSense/
├── Q-A_Retrieval/      # Backend (Flask) & Frontend code
│   ├── app.py          # API Entry point
│   ├── easycontext-frontend/ # React Application
│   └── ...
```

## Prerequisites

-   **Python 3.8+**
-   **Node.js 16+**
-   **Ollama**: Installed and running (`ollama pull phi`).

## Installation & Usage

### 1. Backend Setup

 Navigate to the `Q-A_Retrieval` directory:

```bash
cd Q-A_Retrieval
pip install -r requirements.txt
```

Start the Flask server:

```bash
python app.py
```
*Server runs on http://127.0.0.1:5000*

### 2. Frontend Setup

Navigate to the frontend directory:

```bash
cd Q-A_Retrieval/easycontext-frontend
npm install
npm install lucide-react # If not already installed
```

Start the React app:

```bash
npm start
```
*App runs on http://localhost:3000*

## Usage

1.  Open the frontend in your browser.
2.  **Upload** a document (Drag & drop or Click).
3.  **Type** or **Speak** your question.
4.  View the answer and click **Show Debug Info** to see the underlying prompt.

## 🤝 Contributions
Contributions are welcome!
1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Submit a pull request.

## Author

**Yeshwanth Goud**

*Data Scientist | Full Stack & ML Enthusiast*
