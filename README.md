# 🧠 AI Agent Inference Benchmarking

This project benchmarks the inference performance and response quality of AI agents built with [CrewAI](https://docs.crewai.com/). Each agent specializes in a different aspect of nightlife advisory (energy level, musical preference, and dancing style), and is evaluated using standard metrics and visualizations.

## 📌 Features

- ✅ Modular benchmarking with `BenchmarkRunner`
- ✅ Individual orchestrators for each specialized agent
- ✅ Human/simulated rating evaluation of language output
- ✅ Tracks runtime, memory usage, token usage, latency, and prediction accuracy
- ✅ Visualizes metrics with Plotly
- ✅ Outputs benchmark results in `.jsonl` format (ready for Tableau or scripts)

## 🧠 Agents Benchmarked

| Agent Name                     | Description |
|-------------------------------|-------------|
| Energy Level Advisor          | Assesses social and emotional energy levels for nightlife planning |
| Musical Genre & Culture Advisor | Matches users to musical genres and cultural experiences |
| Dancing Style Preference Advisor | Helps identify user’s preferred dance experiences |

## 📁 Project Structure

ai-agent-benchmarking/ 
    ├── advisor_agents.py 
    ├── advisor_tasks.py 
    ├── energy_orchestrator.py 
    ├── musical_orchestrator.py 
    ├── dancing_orchestrator.py 
    ├── benchmark_runner.py 
    ├── run_benchmark.py 
    ├── rating_simulator.py 
    ├── metrics_visualizer.py 
    ├── utils.py 
    ├── data/ 
        │ └── questions/ 
            │ └── questions.jsonl 
    └── output/ 
        └── metrics/ 
            └── energy_benchmark_results.jsonl


## 🚀 How to Run

    1. Clone this repo:
           ```bash
           git clone https://github.com/your-username/ai-agent-benchmarking.git
           cd ai-agent-benchmarking

    2. Create and activate a virtual environment:
           python3 -m venv .venv
           source .venv/bin/activate  # or `.venv\\Scripts\\activate` on Windows

    3. Install dependencies:
           pip install -r requirements.txt

    4. Set your LLM API key in a .env file:
           GROQ_API_KEY=your_groq_api_key_here

    5. Run the benchmark:
           python run_benchmark.py






📊 Metrics Collected

    Runtime: Total time per iteration

    Memory: Delta and peak usage (in MB)

    Token usage: Prompt tokens, total tokens, tokens per call

    Latency: Per-question and average LLM latency

    LLM Calls: Total number of calls per agent

    Simulated Rating: Human-like scoring from 1–5

    Prediction Error: MAE, MAPE, RMSE (if applicable)





📈 Visualization

    Visual reports are generated automatically using Plotly, including:

    Latency over time

    Memory consumption

    Simulated language output ratings





📄 License

    MIT License. Feel free to use, fork, or contribute!






🙌 Credits

    Built by Thomas J James, leveraging:

    CrewAI

    LangChain

    Groq API
