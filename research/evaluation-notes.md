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

This turns the project into **AI research**, which is strong evidence for UK Global Talent.

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

---

## 3. Types of Tasks Tested

### **Extraction Tasks**
- Extract key-value pairs  
- Extract structured JSON  
- Extract clauses (Project 2)  

### **Summarisation Tasks**
- Highlights  
- Long text summaries  
- Multi-document summaries  

### **Search Tasks**
- Supplier discovery  
- Web lookups  

### **Reasoning Tasks**
- Chain-of-thought  
- Multi-step logic  
- Decision-making  

### **Evaluation Tasks**
- Fact checking  
- Detect inconsistencies  

---

## 4. Evaluation Metrics

### **4.1 Accuracy Score (0–100)**  
Measures correctness using:
- ground truth comparison  
- semantic similarity  

---

### **4.2 Hallucination Rate (%)**

Formula:

Hallucination Rate = Incorrect Claims / Total Claims

Detected using:
- contradictions  
- fact mismatches  
- ungrounded statements  

---

### **4.3 Task Success Rate (%)**

Checks if the task was completed correctly:

- valid JSON returned  
- instructions followed  
- workflow completed  

---

### **4.4 Cost per Run (Token Efficiency)**

Tracks:
- prompt tokens  
- completion tokens  
- total cost per task  

---

### **4.5 Response Time (Latency)**

Measures:  
- time per task  
- averages  
- distribution  

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

The planned dashboard will include:

Accuracy trends

Radar charts

Hallucination scatter plots

Cost vs performance charts

Leaderboards


8. Insights Provided

The Observatory identifies agents that are:

Most accurate

Least hallucination-prone

Fastest

Most cost-efficient

Best for structured extraction

Best for reasoning

These insights help organisations select the right agent framework.