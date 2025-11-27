# AI Agent Evaluation – Technical Research Notes
**Project:** AI Agent Observatory  
**Author:** Hanif Hazrati  

---

## 1. Purpose of the AI Agent Observatory

AI agents behave differently depending on:

- their underlying frameworks  
- their prompting style  
- their memory and state management  
- their tool access  
- the type of task assigned  

Most AI agent frameworks **do not have a standard standardised evaluation method**.

The Observatory provides:

- ✔ Performance benchmarking  
- ✔ Accuracy measurement  
- ✔ Hallucination detection  
- ✔ Cost efficiency analysis  
- ✔ Task reliability scoring  
- ✔ Reproducible evaluation datasets  

This elevates the project into **AI research**, strengthening UK Global Talent evidence.

---

## 2. Key Agent Frameworks Being Evaluated

We evaluate:

- CrewAI  
- AutoGen  
- LangGraph (LangChain)  
- Custom Agent Implementations  

### Architecture Comparison

| Framework | Type                        | Notes                       |
|----------|------------------------------|-----------------------------|
| CrewAI   | Role-based multi-agent       | Strong for workflows        |
| AutoGen  | Conversational multi-agent   | Flexible & coordination-based|
| LangGraph| Directed graph + memory      | State-aware & deterministic |
| Custom   | User-defined agents          | Full flexibility            |

---

## 3. Types of Tasks Tested

### Extraction Tasks
- JSON extraction  
- Key-value pairs  
- Contract clause extraction  

### Summarisation Tasks
- Long-document summaries  
- Multi-source synthesis  

### Search Tasks
- Supplier discovery  
- Web queries  

### Reasoning Tasks
- Multi-step decision making  
- Chain-of-thought reasoning  

### Evaluation Tasks
- Fact checking  
- Consistency detection  

---

## 4. Evaluation Metrics

### 4.1 Accuracy Score (0–100)

Measured using:
- semantic similarity  
- ground truth matching  

### 4.2 Hallucination Rate (%)

**Formula:**

<div style="font-family: monospace; padding: 6px; background: #f6f8fa; border-radius: 6px;">
Hallucination Rate = Incorrect Claims / Total Claims
</div>

Detected by:
- contradiction analysis  
- mismatched facts  
- ungrounded statements  

### 4.3 Task Success Rate (%)

Checks if the agent:
- followed instructions  
- returned valid JSON  
- completed the workflow  

### 4.4 Cost per Run

Tracks:
- prompt tokens  
- completion tokens  
- total cost per evaluation  

### 4.5 Latency

Measures:
- execution time  
- average latency  
- time distribution  

---

## 5. Dataset and Ground Truth Design

A **Task Case Store** entry:

<div style="background:#f6f8fa; padding:10px; border-radius:8px;">
<pre>
{
  "input": "...",
  "expected_output": "...",
  "ground_truth": "...",
  "task_type": "extraction/summarisation/reasoning",
  "evaluation_method": "exact/semantic"
}
</pre>
</div>

This ensures **consistent and reproducible results** across agent frameworks.

---

## 6. Evaluation Engine — Scoring Mechanism

Example scoring logic:

<div style="background:#f6f8fa; padding:10px; border-radius:8px;">
<pre>
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
</pre>
</div>

---

## 7. Dashboard Visualisation

Planned UI includes:

- Accuracy over time  
- Radar charts  
- Hallucination scatter plots  
- Cost vs accuracy  
- Leaderboards  
- Latency distribution charts  

---

## 8. Insights Provided

The Observatory reveals:

- Best-performing agents  
- Most reliable JSON extractors  
- Fastest agents  
- Most cost-efficient frameworks  
- Best reasoning vs extraction models  

This helps organisations choose the right AI agent framework.

---
