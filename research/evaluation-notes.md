1. Purpose of the AI Agent Observatory

AI agents behave differently depending on:

their underlying frameworks

their prompting style

their memory and state management

their tool access

the type of task assigned

Most AI agent frameworks do not have a standard way to evaluate or compare performance.

The purpose of the Observatory is to:

✔ Benchmark agent performance

✔ Measure accuracy

✔ Detect hallucinations

✔ Evaluate cost efficiency

✔ Score task completion reliability

✔ Produce reproducible evaluation datasets

This elevates the project into AI research, which strengthens a UK Global Talent application.

2. Key Agent Frameworks Being Evaluated

We compare:

CrewAI

AutoGen

LangGraph (LangChain)

Custom Agent Implementations

Architecture Comparison
Framework	Type	Notes
CrewAI	Role-based multi-agent	Strong for workflows
AutoGen	Conversational multi-agent	Very flexible
LangGraph	Directed graph + memory	Excellent control & state
Custom	User-defined agents	Maximum customization
3. Types of Tasks Tested
Extraction Tasks

Key-value extraction

Structured JSON extraction

Clause extraction (used in Contract Intelligence Engine)

Summarisation Tasks

Long text summaries

Multi-document summaries

Technical synthesis

Search Tasks

Supplier research

Web lookups

Reasoning Tasks

Chain-of-thought

Multi-step logic

Decision-making

Evaluation Tasks

Fact checking

Detecting inconsistencies

4. Evaluation Metrics
4.1 Accuracy Score (0–100)

Measured using:

semantic similarity

ground truth match

4.2 Hallucination Rate (%)

Formula:

Hallucination Rate = Incorrect Claims / Total Claims


Detected via:

contradictions

false statements

ungrounded assertions

4.3 Task Success Rate (%)

Checks whether the agent:

returns valid JSON

follows instructions

completes the assigned workflow

4.4 Cost per Run (Token Efficiency)

Tracks:

prompt tokens

completion tokens

total cost

4.5 Response Time (Latency)

Measured as:

per-task runtime

average latency

distribution across runs

5. Dataset and Ground Truth Design

A Task Case Store defines each evaluation case:

{
  "input": "...",
  "expected_output": "...",
  "ground_truth": "...",
  "task_type": "extraction/summarisation/reasoning",
  "evaluation_method": "exact/semantic"
}


This ensures reproducibility and consistent evaluation across all agent frameworks.

6. Evaluation Engine – Scoring Mechanism

Example scoring logic:

def evaluate_agent_output(output, ground_truth):
    accuracy = semantic_similarity(output, ground_truth)
    hallucination = detect_hallucination(output, ground_truth)
    task_success = validate_json(output)
    cost = calculate_tokens(output)
    latency = measure_time()

    return {
        "accuracy": accuracy,
        "hallucination": hallucination,
        "task_success": task_success,
        "cost": cost,
        "latency": latency
    }

7. Dashboard Visualisation

The planned dashboard will include:

Accuracy trend lines

Radar charts for multi-agent comparison

Hallucination scatter plots

Cost vs accuracy graphs

Leaderboards

Latency distributions

These visualisations help interpret performance intuitively.

8. Insights Provided

The Observatory helps identify which agents are:

Most accurate

Least hallucination-prone

Fastest

Most cost-efficient

Best for structured extraction

Best for reasoning tasks

These insights support organisational decisions about which AI agent frameworks to adopt.