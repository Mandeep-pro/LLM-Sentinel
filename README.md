🛡️ LLM-Sentinel: Safety Evaluator
An automated red-teaming dashboard designed to evaluate Large Language Model (LLM) safety guardrails. LLM-Sentinel allows developers and security researchers to run adversarial prompts against target models to test for vulnerabilities like prompt injection, jailbreaks, and data leakage.

🚀 Features
Interactive Streamlit Dashboard: A clean, user-friendly UI to configure attacks and analyze model responses in real-time.

Automated Safety Grader: An evaluation engine that scans model outputs and classifies the response as 🟢 SECURE (Attack Refused) or 🔴 VULNERABLE (Guardrails Bypassed).

Live API & Mock Modes:

Test live models like gpt-3.5-turbo and gpt-4o using an active OpenAI API key.

Use the built-in Demo/Mock Mode to test the UI and grading logic without consuming API credits.

Preset & Custom Attacks: Quickly load common attack vectors (e.g., System Prompt Overwrites, Safety Instruction Bypasses) or write custom adversarial prompts.

🛠️ Tech Stack
Language: Python 3.8+

Frontend UI: Streamlit

AI Orchestration: LangChain

LLM Integration: OpenAI API (langchain-openai)

💻 Local Installation & Setup
1. Clone the repository:

Bash
git clone https://github.com/Mandeep-pro/LLM-Sentinel.git
cd LLM-Sentinel
2. Create and activate a virtual environment (Recommended):

DOS
python -m venv venv
.\venv\Scripts\activate
3. Install dependencies:
Make sure you install the exact LangChain and Streamlit packages required for the dashboard.

DOS
pip install streamlit langchain langchain-openai
4. Run the application:

DOS
python -m streamlit run app.py
The dashboard will automatically open in your default web browser at http://localhost:8501.

🎯 How to Use
Configure the Environment: Open the left sidebar. Toggle Demo Mode ON for quick UI testing, or turn it OFF and enter your OpenAI API Key for live model testing.

Select an Attack: Use the dropdown menu to load a preset attack (e.g., Prompt Injection: Ignore Safety Instructions) or select Custom Prompt to write your own.

Run Scan: Click Run Vulnerability Scan.

Analyze Results: The built-in safety grader will evaluate the model's output and display a live status badge alongside the raw text response.

🗺️ Future Roadmap
[ ] Session State History: Implement a running log of past attacks and evaluations in a single session.

[ ] Batch CSV Testing: Add the ability to upload a .csv of adversarial prompts and download a comprehensive safety report.

[ ] LLM-as-a-Judge: Upgrade the keyword-based evaluation engine to use a secondary AI model for highly accurate, nuanced safety grading.

🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.
