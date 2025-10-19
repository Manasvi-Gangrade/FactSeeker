FactSeeker : Detect, Verify, Alert

Demonstration Video : 

FactSeeker is an autonomous, multi-agent AI system designed to detect, verify, and mitigate misinformation in real-time. Leveraging Large Language Models (LLMs), Generative AI, Retrieval-Augmented Generation (RAG), and multimodal analysis, FactSeeker scans multiple platforms—text, images, video, and audio—to identify false content and verify it against trusted, verified sources.

Overview
FactSeeker is built to proactively protect public trust and safety by delivering verified information before misinformation spreads. It integrates a working dashboard, autonomous alerting system, and an explainability layer that shows the reasoning behind flagged content.
The system is scalable and modular, suitable for health crises, political events, or public safety situations where misinformation can have severe consequences.

Features
1. Multi-Agent Architecture: Detection, Verification, and Alert Agents work autonomously.
2. Multimodal Analysis: Processes text, images, videos, and audio.
3. LLM Integration: Context-aware understanding and summarization.
4. RAG Fact-Checking: Retrieves verified information from trusted sources.
5. Real-Time Alerts: Telegram, WhatsApp, and web dashboard notifications.
6. Explainability Layer: Provides reasoning behind each flagged item.
7. Impact Scoring: Prioritizes high-risk misinformation based on virality and severity.
8. User Feedback Loop: Enables continuous model improvement.

Architecture

FactSeeker follows a modular, multi-layer architecture:

Data Ingestion Layer: Streams data from social media, news, and messaging platforms.

Preprocessing & Embeddings Layer: Cleans data and generates embeddings for text, images, and audio/video.

Detection Layer: Multimodal AI classifies content as true or potential misinformation.

Fact-Checking Layer: RAG + LLM verifies flagged content using trusted sources.

Agentic Decision Layer: Multi-agent system calculates Impact Score and triggers alerts.

Dashboard & Notification Layer: Displays flagged content and sends real-time alerts.

Explainability & Feedback Layer: Provides reasoning and incorporates user feedback for model fine-tuning.

Refer to docs/architecture_diagram.png for a visual representation.

Implementation

Backend & AI Orchestration: Python, FastAPI/Flask, LangChain/AutoGPT

Data Storage: MongoDB (NoSQL), FAISS/Pinecone (Vector DB)

NLP Models: BERT, RoBERTa, GPT-4.5, LLaMA, Sentence-BERT

Multimodal Models: Vision Transformer, CNN, Whisper (audio)

Frontend/Dashboard: Streamlit / React.js, D3.js for visualizations

Notifications: Telegram Bot API, WhatsApp Business API, Web Push Notifications

Explainability: SHAP, LIME, LLM-generated rationale

Workflow:

Stream content from APIs and messaging platforms.

Preprocess and generate embeddings for all modalities.

Detect potential misinformation using AI models.

Verify flagged content with RAG + LLM.

Prioritize alerts based on Impact Score.

Notify users and update dashboard autonomously.

Provide reasoning and incorporate user feedback.

Installation

Clone the repository:

git clone https://github.com/yourusername/factseeker.git
cd factseeker


Create virtual environment:

python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows


Install dependencies:

pip install -r requirements.txt


Set API keys for social media/news integrations in .env file.

Usage

Start backend server:

uvicorn backend.main:app --reload


Launch dashboard:

streamlit run frontend/dashboard.py


Alerts will be sent automatically via Telegram/WhatsApp.
