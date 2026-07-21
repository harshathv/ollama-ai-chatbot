# 🤖 Harsha's AI Chatbot — Streamlit + Ollama

A local, privacy-friendly ChatGPT-style chatbot built with **Python**, **Streamlit**, and **Ollama**. The application runs entirely on your machine using open-source Large Language Models (LLMs), eliminating the need for API keys, cloud services, or OpenAI credits while ensuring complete data privacy.

---

## 🚀 Features

- 💬 Chat interface with full conversation memory
- ⚡ Real-time streaming responses (token-by-token)
- 🌡️ Adjustable temperature/creativity slider
- 📝 Editable system prompt
- 🔄 Clear chat / reset session
- 🩺 Automatic Ollama health check with setup guidance
- 🎛️ Switch between multiple local models (Llama 3, Llama 3.2, Llama 3.1, Mistral, Gemma2, Qwen2.5, and Qwen2.5:3B)
- 🎨 Clean and responsive custom Streamlit interface

---

## 🛠️ Tech Stack

- **Frontend:** Streamlit
- **LLM Runtime:** Ollama (Local Large Language Models)
- **Programming Language:** Python
- **HTTP Client:** Requests (for streaming responses from Ollama's `/api/chat` endpoint)

---

## 📋 Prerequisites

Before running the application, ensure you have:

- Python 3.9 or above
- Ollama installed on your system
- At least one Ollama model downloaded locally

---

## ⚙️ Setup & Installation

### 1. Clone the Repository

```bash
git clone https://github.com/harshathv/ollama-ai-chatbot.git
cd ollama-streamlit-chatbot
```

### 2. Install Dependencies

Using pip:

```bash
pip install streamlit requests
```

Or install from the requirements file:

```bash
pip install -r requirements.txt
```

### 3. Start the Ollama Server

Open a terminal and run:

```bash
ollama serve
```

### 4. Download a Model

In another terminal:

```bash
ollama pull llama3.2
```

You can also download any supported model:

- llama3
- llama3.1
- mistral
- gemma2
- qwen2.5
- qwen2.5:3b

### 5. Run the Application

```bash
streamlit run app.py
```

The application will launch in your browser at:

```
http://localhost:8501
```

---

## 💻 Usage

1. Select an LLM from the sidebar.
2. Adjust the temperature slider to control response creativity.
3. Modify the system prompt to customize the assistant's behavior (optional).
4. Enter your query in the chat box.
5. Watch responses stream in real time.
6. Use **Clear Chat** to reset the conversation whenever needed.

---

## ⚙️ How It Works

- The application first checks whether the Ollama server is running locally.
- Conversation history is stored using **Streamlit Session State**.
- User messages and the system prompt are sent to Ollama's `/api/chat` endpoint.
- Responses are streamed token-by-token and displayed instantly in the chat interface.
- The assistant's replies are stored to maintain conversational context throughout the session.

---

## 📁 Project Structure

```
ollama-streamlit-chatbot/
│── app.py
│── requirements.txt
├── README.md
└── .gitignore
```

---

## ❗ Troubleshooting

### Ollama is not running

Start the Ollama server:

```bash
ollama serve
```

Then refresh the application.

---

### Model Not Found

Download the selected model before using it:

```bash
ollama pull <model-name>
```

Example:

```bash
ollama pull llama3.2
```

---

### Slow Responses

Large language models require more system resources. If responses are slow, consider using a lightweight model such as:

- qwen2.5:3b

---

## 📄 License

This project is open source and intended for educational and learning purposes. Feel free to fork, modify, and extend it.

---

