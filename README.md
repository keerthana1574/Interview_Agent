🧑‍💼 AI Interview Agent
Intelligent Interview Automation — Powered by Groq LLM

The AI Interview Agent is a smart interview automation system built with Streamlit + Groq AI. It dynamically generates interview questions, records candidate answers, evaluates all responses at the end, and produces a complete hiring report — enabling structured, unbiased, and efficient interviews for recruiters and HR teams.

🔥 Features
Feature	Description
🎯 AI-Generated Questions	Role-based, experience-level–aware question generation.
📝 Answer Recording	Interviewer types/pastes candidate responses; saved automatically.
⏭ Skip Support	Skip any question without penalty.
📄 Resume Parsing (Optional)	Upload PDF/TXT resume to auto-extract skills.
🧠 End-of-Interview Evaluation	Prevents real-time bias; scores generated only at the end.
📊 Scoreboard	Per-question score + final score.
🧾 Final AI Summary	Strengths, weaknesses, improvement suggestions, hire/no-hire.
⚡ Groq-Powered Inference	Uses llama-3.1-8b-instant for ultra-fast responses.
🧩 Architecture Overview
Interviewer
   │
   ▼
Streamlit Web Interface
   │
   ▼
Interview Engine (Python)
   ├─ Resume → Skill Extraction
   ├─ Dynamic Question Generation
   ├─ Answer Storage (Session State)
   ├─ Final Answer Evaluation
   └─ Final Summary Report
   │
   ▼
Groq LLM API (llama-3.1-8b-instant)

📁 Project Structure
📦 interview-agent
 ┣ 📜 app.py               # Main Streamlit app
 ┣ 📜 .env                 # Groq API key (excluded from repo)
 ┣ 📜 requirements.txt     # Dependencies
 ┗ 📜 README.md            # Documentation

🔧 Installation & Setup
1️⃣ Clone the Repository
git clone <your-repo-url>
cd interview-agent

2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Add Environment Variables

Create a .env file:

GROQ_API_KEY=your_groq_api_key_here


Get a free key at:
🔗 https://console.groq.com/

▶ Run the Application
streamlit run app.py

📦 Requirements (requirements.txt)
streamlit
pandas
python-dotenv
PyPDF2
groq

🖥 How the App Works

Enter candidate details (name, role, experience).

Upload resume (optional).

Start interview → AI generates questions one by one.

Record candidate’s answers or skip questions.

Click Submit & Generate Report at the end.

View results:

Scoreboard

Average score

Final report

Hiring recommendation

🎯 Why This Tool Matters
Advantage	Benefit
Evaluation happens at the end	Removes interviewer bias
Automated skill extraction	Saves time & reduces manual entry
Groq-powered speed	Very fast question generation
Structured reporting	Standardized evaluation across candidates
Streamlit UI	Simple, clean & accessible
🚀 Future Enhancements

🎤 Voice-based answer input

📄 Export final report to PDF

📊 Admin dashboard for multiple candidates

🔗 ATS integration (Airtable / Notion)

🌍 Multi-language interview support

👨‍💻 Tech Stack
Layer	Technology
UI	Streamlit
Backend	Python
LLM	Groq — llama-3.1-8b-instant
Resume Parser	PyPDF2
State Store	Streamlit Session State
