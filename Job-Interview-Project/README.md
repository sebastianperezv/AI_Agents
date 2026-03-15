# 🤖 AI Agent-Powered Job Interview Assistant

This project leverages AI Agents to simulate and support job interview scenarios. Using a modular design powered by `CrewAI`, multiple agents collaborate to mimic real-world interview environments, offering preparation, evaluation, and feedback.

## 🔍 Features

- **Role-specific interviewers** with unique personalities and question banks.
- **Dynamic scenario simulation** with AI-driven question/answer flows.
- **Real-time feedback** to evaluate candidate performance.
- **Extensible agent framework** for adding new roles, industries, or interview styles.

## 🧠 Technologies Used

- [CrewAI](https://github.com/joaomdmoura/crewAI) for orchestrating multi-agent workflows.
- [LangChain](https://www.langchain.com/), [OpenAI API](https://platform.openai.com/), [Serper API](https://serper.dev/) for LLM and search capabilities.
- Python in a Jupyter Notebook format for ease of development and testing.

## 📦 Use Cases

- Job seekers looking for **intelligent mock interview preparation**.
- Companies exploring **AI-powered candidate screening tools**.
- Developers interested in **multi-agent systems** applied to real-world tasks.

## 🚀 Getting Started

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/ai-interview-agents.git
    cd ai-interview-agents
    ```

2. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up your API keys**:
    - Add your OpenAI and Serper API keys to a `secrets.json` file located in a safe path.
    - Example format:
      ```json
      {
        "OPENAI_API_KEY": "your-openai-api-key",
        "SERPER_API_KEY": "your-serper-api-key"
      }
      ```

4. **Run the notebook**:
    - Open `Job_Interview_Project.ipynb` in Jupyter Notebook or JupyterLab.
    - Follow the cell instructions to simulate the interview process.

## 🤝 Contributing

Contributions are welcome! If you have ideas for new agent roles or features, feel free to open an issue or pull request.
