🧠 LLM SQL Assistant (Text-to-SQL AI)

An AI-powered database assistant that allows users to query databases using natural language.
The system converts user questions into SQL queries using LLMs (OpenAI / Gemini), executes them on a database, and returns results in a human-readable format.

🚀 Features
🔍 Ask questions in natural language (English / Japanese)
🤖 Automatically generate SQL queries using LLMs
🗄️ Execute queries on MySQL / SQLite databases
📊 Display results using Streamlit UI
🔄 Supports multiple LLMs (OpenAI, Google Gemini)
🧠 Prompt-based query generation using YAML templates
💬 Chat-based interaction with database (LangChain agent)
🏗️ Architecture

User Input → Prompt Template → LLM → SQL Query → Database → Result → UI

🛠️ Tech Stack
Language: Python
Frameworks: Streamlit, LangChain
LLMs: OpenAI, Google Gemini
Database: MySQL, SQLite
ORM / Tools: SQLAlchemy, Pandas
Other: YAML, dotenv
📁 Project Structure
├── sql_assistant.py       # Basic LLM SQL generator (OpenAI)
├── sql_agent.py           # LangChain-based SQL agent (chat system)
├── shin_agent.py          # Gemini-based SQL assistant
├── shin_dbagent.py        # Advanced DB agent with execution
├── sql_execution.py       # MySQL query execution
├── prompts/               # YAML prompt templates
├── requirements.txt       # Dependencies
└── app (Streamlit UI)
⚙️ Setup Instructions
1. Clone Repository
git clone https://github.com/amardeep112345/SQL_LLM_AI.git
cd your-repo-name
2. Create Virtual Environment
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
3. Install Dependencies
pip install -r requirements.txt
4. Setup Environment Variables

Create a .env file in the root directory:

# OpenAI
OPENAI_API_KEY=your_openai_key

# Google Gemini
GOOGLE_API_KEY=your_gemini_key

# Database (MySQL example)
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=your_database
DB_PORT=3306
5. Run the Application
streamlit run sql_agent.py
🧪 Example Usage

Input:

Find all parks in Yokohama with swings and toilets

Generated SQL:

SELECT * FROM kanagawa_park WHERE Address LIKE '%横浜市%';

Output:

Structured data displayed in UI
💡 Use Cases
Chat with your database
Business analytics assistant
Internal company data tools
Replacing manual SQL queries
AI-powered dashboards
⚠️ Limitations
SQL accuracy depends on prompt quality
Requires properly structured database schema
Limited error handling for invalid queries
API cost (OpenAI / Gemini)
🔮 Future Improvements
✅ Add better error handling
✅ Improve UI/UX
✅ Add schema auto-detection
✅ Add conversation memory
✅ Support more databases (PostgreSQL, Snowflake)
✅ Role-based query control
👨‍💻 Author

Amardip Chimankar
Full Stack Engineer | AI Enthusiast
