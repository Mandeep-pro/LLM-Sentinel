# 🛡️ LLM-Sentinel

An automated red-teaming dashboard designed to evaluate Large Language Model (LLM) safety guardrails. LLM-Sentinel allows developers and security researchers to run adversarial prompts against target models and assess their resilience against common attack vectors.

## 🚀 Features

- **Interactive Streamlit Dashboard**: A clean, user-friendly UI to configure attacks and analyze model responses in real-time
- **Automated Safety Grader**: An evaluation engine that scans model outputs and classifies responses as:
  - 🟢 **SECURE** (Attack Refused)
  - 🔴 **VULNERABLE** (Guardrails Bypassed)
- **Live API & Mock Modes**:
  - Test live models like `gpt-3.5-turbo` and `gpt-4o` using an active OpenAI API key
  - Use built-in Demo/Mock Mode to test the UI and grading logic without consuming API credits
- **Preset & Custom Attacks**: Quickly load common attack vectors (e.g., System Prompt Overwrites, Safety Instruction Bypasses) or write custom adversarial prompts

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| **Language** | Python 3.8+ |
| **Frontend UI** | Streamlit |
| **AI Orchestration** | LangChain |
| **LLM Integration** | OpenAI API (langchain-openai) |

## 💻 Installation & Setup

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Mandeep-pro/LLM-Sentinel.git
   cd LLM-Sentinel
   ```

2. **Create and activate a virtual environment** (Recommended):
   ```bash
   # On Windows
   python -m venv venv
   .\venv\Scripts\activate

   # On macOS/Linux
   python -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install streamlit langchain langchain-openai
   ```

4. **Run the application:**
   ```bash
   python -m streamlit run app.py
   ```
   The dashboard will automatically open in your default web browser at `http://localhost:8501`

## 🎯 Usage Guide

1. **Configure the Environment**: 
   - Open the left sidebar
   - Toggle **Demo Mode ON** for quick UI testing
   - Or turn it OFF and enter your OpenAI API Key for live model testing

2. **Select an Attack**: 
   - Use the dropdown menu to load a preset attack (e.g., "Prompt Injection: Ignore Safety Instructions")
   - Or select **Custom Prompt** to write your own

3. **Run Scan**: 
   - Click the **Run Vulnerability Scan** button

4. **Analyze Results**: 
   - The built-in safety grader will evaluate the model's output
   - Display shows a live status badge alongside the raw text response

## 🗺️ Roadmap

- [ ] **Session State History**: Implement a running log of past attacks and evaluations within a single session
- [ ] **Batch CSV Testing**: Add the ability to upload a `.csv` file of adversarial prompts and download a comprehensive safety report
- [ ] **LLM-as-a-Judge**: Upgrade the keyword-based evaluation engine to use a secondary AI model for highly accurate, nuanced safety grading

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! 

Please feel free to:
- Check the [issues page](https://github.com/Mandeep-pro/LLM-Sentinel/issues) for open discussions
- Submit a pull request with your improvements
- Open a new issue to report bugs or request features

## 📝 License

*Add your license information here (e.g., MIT, Apache 2.0, etc.)*

## 📧 Contact

*Add your contact information or links here*

---

**Last Updated**: July 2026
