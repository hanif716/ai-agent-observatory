# AI Agent Observatory
*A benchmarking and evaluation platform for analysing AI agents across accuracy, hallucination, cost, latency, and task success.*

---

## 🌍 Overview
The AI Agent Observatory is a research and engineering project designed to measure and compare the performance of different AI agent frameworks.

It provides a unified environment for evaluating:
- CrewAI agents  
- AutoGen agents  
- LangGraph workflows  
- Custom agent implementations  

The system focuses on producing transparent, reproducible, and comparable performance metrics.

This is part of a 3-project AI portfolio demonstrating advanced engineering and innovation for the UK Global Talent technical track.

---

## 🎯 Problem Statement
AI agents behave differently depending on:
- framework architecture  
- prompting strategy  
- memory handling  
- tool execution  
- state management  

However, **there is currently no standardised way to evaluate agent quality**.

This makes it difficult for organisations to:
- choose the right agent framework  
- understand trade-offs  
- compare agents on reliability  
- determine hallucination risk  
- estimate cost or latency  

---

## 🚀 Solution
The AI Agent Observatory provides:
- A common evaluation dataset  
- Standard ground truth answers  
- Objective scoring metrics  
- Cost tracking  
- Latency measurement  
- Structured results for dashboards  

This enables fair comparison between autonomous agent systems.

---

## 🧩 Key Features

### ✔ Multi-Framework Evaluation
Supports:
- CrewAI  
- AutoGen  
- LangGraph  
- Custom agents  

### ✔ Performance Metrics
Evaluates:
- Accuracy  
- Hallucination rate  
- Task completion success  
- Cost per run  
- Response time  

### ✔ Dataset-Driven Testing
Each agent is tested on the same curated dataset:
- extraction tasks  
- summarisation tasks  
- reasoning tasks  
- fact-check tasks  
- JSON compliance tasks  

### ✔ Dashboard (Planned)
Visual comparisons of:
- accuracy trends  
- hallucination detection  
- cost distributions  
- agent ranking  
- latency scatter plots  

---

## 🏗 Architecture

### High-Level Architecture  
Image stored at:

### Mermaid Diagram  

---

## 🧠 Technical Stack

| Layer        | Technology                            |
|--------------|----------------------------------------|
| Backend      | FastAPI / Python                       |
| Evaluation   | Custom scoring engine                  |
| Frameworks   | CrewAI, AutoGen, LangGraph             |
| LLMs         | OpenAI / Anthropic                     |
| Storage      | JSON datasets / PostgreSQL (planned)   |
| Frontend     | React dashboard (planned)              |

---

## 🔬 Research Notes
Full technical evaluation logic is documented in:

Includes:
- scoring approaches  
- hallucination detection logic  
- latency measurement  
- cost tracking  
- dataset structure  
- validation rules  

---

## 🛠 Installation (Coming Soon)
Additional setup instructions will be added during early development.

---

## 📅 Roadmap

### Phase 1 — Evaluation Engine
- [x] Architecture design  
- [x] Research notes  
- [ ] Evaluation runner  
- [ ] Accuracy scoring  
- [ ] JSON validation tools  

### Phase 2 — Dataset  
- [ ] Test case library  
- [ ] Ground truth store  
- [ ] Multi-task benchmarks  

### Phase 3 — Framework Integrations
- [ ] CrewAI adapter  
- [ ] AutoGen adapter  
- [ ] LangGraph adapter  

### Phase 4 — Dashboard
- [ ] React interface  
- [ ] Charts and heatmaps  
- [ ] Leaderboard  

---

## 💡 Why This Project Matters (For Assessors)
This project demonstrates:

- **Innovation**: evaluating autonomous AI agents  
- **Technical depth**: building scoring, metrics, hallucination detection  
- **Advanced engineering**: multi-framework evaluation  
- **Research capability**: designing test datasets + metrics  
- **Public value**: knowledge for the wider AI ecosystem  

Supports:
- **Mandatory Criterion (Innovation)**  
- **Optional Criterion (Technical Contribution)**  

---

## 📜 License
MIT License.
