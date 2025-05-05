# Job-Analyzer-using-Gen-AI
🔍 Job Analyzer AI
Job Analyzer AI is an AI-powered web scraping and resume analysis tool designed to streamline the job search experience. Using cutting-edge language models (LLMs), it extracts job postings directly from company websites, matches them with your portfolio, and generates tailored interview questions—powered by Groq Cloud and LangChain.

📌 Key Features
🌐 Web-Based Job Description Scraping

🧠 Skill Extraction Using LLMs (LLaMA 3.3 70B via Groq Cloud)

📊 Portfolio Match Score & Skill Gap Analysis

💬 AI-Generated Interview Questions

⚡ Fast LLM Inference via Groq Cloud

🧱 LangChain & ChromaDB-Powered Workflow

🖼️ Gradio UI for Simple Interaction

🛠️ Tech Stack
Component	Tech Used
Backend / LLM	Python, LangChain, ChatGroq (LLaMA 3)
Frontend	Gradio
Database	ChromaDB (Vector Store)
Deployment	Localhost or Cloud

📦 Installation
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/yourusername/job-analyzer-ai.git
cd job-analyzer-ai
2. Install Requirements
bash
Copy
Edit
pip install -r requirements.txt
Or individually:

bash
Copy
Edit
pip install langchain-core langchain_groq langchain_community
pip install chromadb gradio pandas
3. Set Environment Variables
Create a .env file:

env
Copy
Edit
GROQ_API_KEY=your_groq_api_key_here
▶️ How to Run
bash
Copy
Edit
python app.py
Or directly in your Jupyter/colab environment.

The Gradio interface will open at:
http://localhost:7860/

📁 Inputs Required
🔗 Job Posting URL (e.g., careers page or job listing page)

📄 Portfolio CSV File with a column named Technology

🧠 How It Works
Scrapes job details from the provided URL

Uses LLM (LLaMA 3 on Groq) to extract role, experience, skills, description

Matches scraped skills with portfolio CSV

Calculates match percentage and generates interview questions

Outputs all data in structured JSON format

📊 Output Sample
json
Copy
Edit
{
  "skills_match": {
    "Python": 90,
    "TensorFlow": 75
  },
  "interview_questions": [
    "How do you optimize a deep learning model for low latency inference?",
    "What is the role of attention mechanisms in transformers?"
  ]
}

📂 Folder Structure
bash
Copy
Edit
job-analyzer-ai/
├── app.py
├── requirements.txt
├── README.md
└── vectorstore/             # ChromaDB persistent storage

🧩 Future Enhancements
Resume PDF parser

Resume-to-job matching score visualization

Integration with LinkedIn Jobs or Indeed

Telegram or email alerts

