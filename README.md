# 📄 AI Resume Evaluator & Candidate Ranker

An AI-powered recruitment tool built with **Python**, **Groq LLM** (`gpt-oss-120b`), **Pydantic**, and **Streamlit**. 

This application parses job descriptions and candidate resumes (`.pdf` and `.docx`), extracts structured data, evaluates skill alignment, and ranks applicants with detailed match scores and HR verdicts.

---

## 🌟 Key Features

* **Multi-Format Document Parsing**: Seamlessly extracts text from both PDF and DOCX files.
* **Structured Data Extraction**: Uses **Pydantic** to enforce valid JSON outputs for candidate skills, experience, and education.
* **Smart Matching Logic**: Evaluates candidate fit against key job requirements (Required Skills, Preferred Skills, STEM Education).
* **High-Speed LLM Inference**: Powered by **Groq API** (`openai/gpt-oss-120b`).
* **Interactive Web Dashboard**: Built with **Streamlit** for easy drag-and-drop resume evaluation and visual candidate ranking.


## 🛠️ Tech Stack

* **Frontend / UI**: [Streamlit](https://streamlit.io/)
* **LLM Provider**: [Groq API](https://groq.com/) (`openai/gpt-oss-120b`)
* **Data Validation**: [Pydantic v2](https://docs.pydantic.dev/)
* **Document Readers**: `pypdf`, `python-docx`
* **Environment Management**: `python-dotenv`, `venv`

---

## 📁 Repository Structure

```text
AI-Resume-Evaluator/
├── resume_parser.py    # Main Streamlit web application & LLM pipeline
├── requirements.txt    # Required Python dependencies
├── .env.example        # Template for environment variables
├── .gitignore          # Keeps secrets (.env) and environments (.venv) safe
└── README.md           # Project documentation


## 🚀 Quickstart Guide

### 1. Prerequisites
* Python 3.11 or higher
* A Groq API Key (Get a free key at [console.groq.com](https://console.groq.com))

### 2. Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/AI-Resume-Evaluator.git](https://github.com/YOUR_USERNAME/AI-Resume-Evaluator.git)
   cd AI-Resume-Evaluator

python3 -m venv venv
source venv/bin/activate

pip install -r requirements.txt

GROQ_API_KEY=your_actual_groq_api_key_here


streamlit run resume_parser.py


---

### Chunk 4: How It Works & License

```markdown
## 💡 How It Works

1. **Job Description Extraction**: The LLM parses the JD to extract required skills, preferred qualifications, and minimum required education into a structured JSON object using Pydantic.
2. **Semantic Resume Parsing**: Candidacy files (`.pdf`/`.docx`) are extracted and analyzed by meaning—identifying skills, work experience, and internships regardless of header formatting.
3. **Structured Candidate Ranking**: Candidates are scored against job criteria (0–100%), generating a breakdown of matched skills, missing requirements, and a final HR verdict.

---

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.