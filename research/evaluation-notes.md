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

Most AI agent frameworks **do not have a standard way to evaluate or compare performance**.

The purpose of the Observatory is to:

- ✔ Benchmark agent performance  
- ✔ Measure accuracy  
- ✔ Detect hallucinations  
- ✔ Evaluate cost efficiency  
- ✔ Score task completion reliability  
- ✔ Produce reproducible evaluation datasets  

This turns the project into **AI research**, making it strong evidence for UK Global Talent.

---

## 2. Key Agent Frameworks Being Evaluated

We compare performance across:

- **CrewAI**  
- **AutoGen**  
- **LangGraph (LangChain)**  
- **Custom Agent Implementations**  

### Architecture Comparison Table

| Framework | Type                        | Notes                       |
|----------|------------------------------|-----------------------------|
| CrewAI   | Role-based multi-agent       | Good for workflow pipelines |
| AutoGen  | Conversational multi-agent   | Flexible, dialogue-driven   |
| LangGraph| Directed graph + memory      | Powerful for graph control  |
| Custom   | User-built agents            | Maximum flexibility         |

Studying their behaviour gives deep insight into agent architecture trade-offs.

---

## 3. Types of Tasks Tested

### **Extraction Tasks**
- Extract key-value pairs  
- Extract structured JSON  
- Extract clauses (used in Contract Intelligence Engine)  

### **Summarisation Tasks**
- Summaries of long text  
- Multi-document summaries  
- Technical abstraction  

### **Search Tasks**
- Supplier research  
- Evidence gathering  
- Web lookups  

### **Reasoning Tasks**
- Chain-of-thought  
- Multi-step logic  
- Decision-making  

### **Evaluation Tasks**
- Fact checking  
- Detect inconsistencies  
- Compare statements  

Each task includes a **ground truth** for reliable scoring.

---

## 4. Evaluation Metrics

The Observatory measures five key metrics.

---

### **4.1 Accuracy Score (0–100)**  
How correct the output is.

Methods include:
- ground truth comparison  
- semantic similarity  
- exact vs fuzzy match scoring  

---

### **4.2 Hallucination Rate (%)**

Hallucinations = incorrect or fabricated statements.

Detection uses:
- contradiction checks  
- fact mismatches  
- ungrounded claims  

Formula:
Hallucination Rate = Incorrect Claims / Total Claims

---

### **4.3 Task Success Rate (%)**

Checks if the agent completed the task correctly.

Examples:
- returned valid JSON  
- followed instructions  
- completed workflow steps  

---

### **4.4 Cost per Run (Token Efficiency)**

Tracks:
- prompt tokens  
- completion tokens  
- total cost per task  

Some agents are accurate but too expensive.

---

### **4.5 Response Time (Latency)**

Measures speed:
- per task latency  
- average latency  
- distribution over repeated runs  

---

## 5. Dataset and Ground Truth Design

A **Task Case Store** defines each evaluation case:

```json
{
  "input": "...",
  "expected_output": "...",
  "ground_truth": "...",
  "task_type": "extraction/summarisation/reasoning",
  "evaluation_method": "exact/semantic"
}
This ensures reproducible, comparable results across all agent frameworks.
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

The planned React dashboard will show:

Accuracy trends

Radar charts comparing multiple agents

Hallucination scatter plots

Cost vs performance charts

Task success heatmaps

Leaderboards

This makes evaluation results easy to interpret.

8. Insights Provided

The Observatory identifies which agents are:

Most accurate

Least hallucination-prone

Fastest

Most cost-efficient

Most reliable for structured tasks

Best for reasoning vs extraction

These insights help organisations choose the right agent framework and model.
