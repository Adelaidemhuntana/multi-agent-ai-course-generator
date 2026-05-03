# multi-agent-ai-course-generator
A cloud-ready multi-agent AI system that generates structured courses from user prompts using Researcher, Judge, Content Builder, and Orchestrator agents. Built with Python, FastAPI, and microservices architecture.

##  Overview

This project demonstrates how multiple AI agents can collaborate to solve a complex task. Instead of relying on a single model, the system distributes responsibilities across independent services that communicate with each other.

A user provides a prompt (e.g., *"Create a course about the history of coffee"*), and the system automatically researches, validates, and builds a complete structured course.



##  Architecture

The system is built using four core agents:

- **Orchestrator Agent**
  - Controls the workflow
  - Sends tasks to other agents
  - Manages the full pipeline

- **Researcher Agent**
  - Gathers relevant information
  - Performs initial content generation

- **Judge Agent**
  - Evaluates the quality and accuracy of responses
  - Decides whether content should be improved

- **Content Builder Agent**
  - Generates the final structured course
  - Formats output into a clean, readable structure

---

##  Workflow

User Prompt → Orchestrator → Researcher → Judge → Content Builder → Final Output

If the Judge rejects the content, the system loops back and improves the result until it meets quality standards.

---

##  Tech Stack

- Python
- FastAPI
- Uvicorn
- Google Cloud (Cloud Run ready)
- JSON-RPC (Agent-to-Agent communication)
- Microservices architecture

---

## Running Locally

### 1. Clone the repository

```bash
git clone https://github.com/Adelaidemhuntana/multi-agent-ai-course-generator.git
cd multi-agent-ai-course-generator
