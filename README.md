# AI Meeting Assistant

An AI powered meeting assistant built with Python that helps turn meeting recordings into useful information. It can transcribe audio, summarize discussions, extract important decisions and action items, and let users ask questions about their meetings.

The goal of this project is to make it easier to review long meetings without having to listen to the entire recording again.

## What It Does

**Audio and Video Transcription**

Process audio and video recordings and convert speech into text using OpenAI Whisper and Sarvam AI for supported languages.

**Meeting Summaries**

Generate clear and concise summaries that cover the main topics discussed during a meeting.

**Action Items and Decisions**

Extract important tasks, responsible people, deadlines, key decisions, and questions that still need to be answered.

**Chat With Your Meetings**

Ask questions about a meeting and get answers based on its transcript using Retrieval Augmented Generation (RAG).

**Semantic Search**

Use Hugging Face embeddings and ChromaDB to find relevant information from meeting transcripts.

**Report Export**

Save meeting summaries and other extracted information as PDF or TXT files where supported by the application.

## Technologies Used

Python, Streamlit, OpenAI Whisper, Sarvam AI, LangChain, Mistral AI, ChromaDB, Hugging Face Embeddings, and Retrieval Augmented Generation.

## How It Works

The application takes an audio or video recording and prepares its audio for transcription. Whisper or Sarvam AI converts the speech into text, depending on the selected transcription workflow.

The transcript is then processed using a language model to generate a summary and identify action items, decisions, and follow up questions.

For question answering, the transcript is divided into smaller chunks and converted into embeddings. These embeddings are stored in ChromaDB so the application can retrieve relevant information when a user asks a question.

The retrieved content is passed to the language model to generate an answer based on the meeting transcript.

## Project Structure

```text
AI-Video-Assistant/
│
├── app.py
├── main.py
├── test.py
├── Requirements.txt
│
├── core/
│   ├── extractor.py
│   ├── rag_engine.py
│   ├── summarizer.py
│   ├── transcriber.py
│   └── vector_store.py
│
└── utils/
    └── audio_processor.py
```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/mohda9as/AI--Video-Assistent.git
cd AI--Video-Assistent
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install the Dependencies

```bash
pip install -r Requirements.txt
```

### 4. Configure API Keys

Create a `.env` file in the project folder and add the API keys required by the application. Use the exact environment variable names expected by the code.

Keep your API keys private and never upload your `.env` file to GitHub.

### 5. Run the Application

```bash
streamlit run app.py
```

## What I Learned

While building this project, I explored speech recognition, audio processing, working with language models, building LangChain pipelines, generating text embeddings, storing vectors in ChromaDB, and implementing Retrieval Augmented Generation for question answering.

It also helped me understand how different AI components can be combined into a single application to solve a practical problem.

## Future Improvements

I would like to add speaker identification, improve answer accuracy with source references, support searching across multiple meetings, and make the application easier to deploy and use.

## Author

**Mohd Anas**

GitHub: [mohda9as](https://github.com/mohda9as)

