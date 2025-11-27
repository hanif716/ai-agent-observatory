AI Agent Evaluation – Technical Research Notes

Project: AI Agent Observatory
Author: Hanif Hazrati

🧠 1. Purpose of the AI Agent Observatory

AI agents behave differently depending on:

their underlying frameworks,

their prompting style,

their memory,

their tool access,

and the type of task assigned.

However, most AI agent frameworks have no standard way to compare performance.

The purpose of the AI Agent Observatory is to:

✔ Benchmark agent performance
✔ Measure accuracy
✔ Detect hallucinations
✔ Evaluate cost efficiency
✔ Score task completion reliability
✔ Produce reproducible evaluation datasets

This elevates the project from “tool building” to AI research, which is extremely valuable for UK Global Talent.

🧩 2. Key Agent Frameworks Being Evaluated

We evaluate the following agents:

CrewAI

AutoGen

LangGraph (LangChain)

Custom Agent Implementations

Each agent uses different architectures:

Framework	Type	Notes
CrewAI	Role-based multi-agent	Good for workflows
AutoGen	Conversational multi-agent	Flexible
LangGraph	Directed graph + memory	Very powerful
Custom Agent	Your own design	Maximum flexibility

Studying how they perform across tasks shows meaningful technical insight.

📚 3. Types of Tasks Tested

We test agents on tasks relevant to:

Extraction Tasks

Extract key-value pairs from text

Extract structured JSON

Extract contract clauses (useful for Project 2)

Summarisation Tasks

Summaries of long text

Multi-document summaries

Technical brief creation

Search Tasks

Researching suppliers

Finding information on the web

Reasoning Tasks

Chain-of-thought

Multi-step logic

Decision-making tasks

Evaluation Tasks

Fact checking

Comparing two statements

Detecting inconsistencies

Each task has a ground truth to measure accuracy.

🔍 4. Evaluation Metrics Defined

The Observatory focuses on five core metrics:

4.1 Accuracy Score (0–100)

Measures how correct an agent’s answer is.

Method:

Compare agent output with ground truth

Compute semantic similarity

Apply scoring rules (exact match vs. fuzzy match)

4.2 Hallucination Rate (%)

Measures incorrect or fabricated information.

Detection methods:

Contradiction detection

Fact mismatch

Critical errors in reasoning

Output not grounded in input

Example:

Hallucination = Incorrect Claims / Total Claims

4.3 Task Success Rate (%)

Does the agent complete the task as expected?

Examples:

Did it return JSON correctly?

Did it follow instructions?

Did it complete the workflow?

4.4 Cost per Run (Token Efficiency)

Tracks:

Prompt tokens

Completion tokens

Total cost per task

Agents may perform well but be too expensive for practical use.

4.5 Response Time (Latency)

How long it takes each agent to complete a task.

Measured in milliseconds.

🗂 5. Dataset and Ground Truth Design

We create a Task Case Store:

Each case includes:

{
  "input": "...",
  "expected_output": "...",
  "ground_truth": "...",
  "task_type": "extraction/summarisation/reasoning",
  "evaluation_method": "exact/semantic"
}


This provides reproducibility:
any agent can be tested on the same tasks.

⚙️ 6. Evaluation Engine – Scoring Mechanism
6.1 Scoring Algorithm (Example)
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

📊 7. Dashboard Visualisation

The React dashboard will display:

Line charts of performance over time

Radar charts comparing agents

Bar charts for accuracy

Hallucination scatter plots

Cost per task comparisons

Leaderboards

These visualisations are essential for your technical evidence.

🧠 8. Insights Provided

The Observatory reveals which agents are:

Most accurate

Least hallucination-prone

Fastest

Most cost-efficient

Best for reasoning vs. extraction tasks

This allows organisations to make informed decisions when selecting AI tools.

🏆 9. Why This Matters for Global Talent Visa

This is high-value technical evidence because:

✔ It demonstrates advanced AI evaluation understanding
✔ Shows strong independent research capability
✔ Demonstrates you can design reliable AI systems
✔ Clearly displays technical contribution (OC3)
✔ Framework-level innovation (OC1)
✔ You’re producing open-source benchmarking tools (assessors love this)

