# AI-Agents-with-Crew-AI

# AI Agents for DevOps: Research and Reporting with Crew AI

This project demonstrates how to build autonomous AI agents using the Crew AI framework to perform research and summarization tasks. The example project focuses on researching Kubernetes trends and generating a comprehensive report using local language models (LLMs). 

## Key Features:
- Autonomous agents that can complete tasks without human guidance
- Utilizes open-source frameworks (Crew AI) and local language models (Llama)
- No reliance on cloud-based services, avoiding security and cost concerns
- Generates a research report summarizing Kubernetes trends

## Table of Contents:
- [Project Overview](#project-overview)
- [Requirements](#requirements)
- [Setup Instructions](#setup-instructions)
- [Project Structure](#project-structure)
- [Running the Project](#running-the-project)
- [Limitations](#limitations)

---

## Project Overview

This project involves creating two AI agents:
1. **Researcher Agent**: Researches the latest trends in Kubernetes.
2. **Reporting Agent**: Summarizes the research findings into a comprehensive Markdown report.

Both agents are powered by the **Crew AI** framework and the **Llama 3.1** language model.

## Requirements

- Python version 3.10 - 3.13
- [Crew AI](https://crew-ai.github.io) package
- Local **Llama** model (Llama 3.1 or newer)
- Virtual environment for Python dependencies

## Setup Instructions

### 1. Create a Virtual Environment

First, create a Python virtual environment to keep dependencies isolated.

```bash
python3 -m venv ai-agents-env
source ai-agents-env/bin/activate  # On Windows use ai-agents-env\Scripts\activate
2. Install Dependencies
Install the Crew AI package using pip:

bash
Copy
Edit
pip install crew-ai
If you don't have the Llama model installed, follow the instructions to install Ollama and pull the Llama 3.1 model.

3. Generate Project Structure
Create the project structure using Crew AI's crew create command:

bash
Copy
Edit
crew create
When prompted, choose the following:

Language Model Provider: Llama

Llama Model Version: Llama 3.1 (or newer if available)

4. Install Project Dependencies
Install any additional dependencies using the crew install command:

bash
Copy
Edit
crew install
Project Structure
After generating the project, Crew AI will create a directory structure with the following important files:

1. agents.yaml
Defines the agents and their roles, goals, and backstories. For example:

Researcher Agent: Tasked with researching Kubernetes trends.

Reporting Agent: Tasked with summarizing the findings into a structured report.

2. task.yaml
Defines the tasks that each agent will execute. The Researcher Agent will find the latest Kubernetes trends, and the Reporting Agent will generate a Markdown report.

3. main.py
Ties everything together by initializing the agents and running them.

4. crew.py
Contains Python class definitions and decorators that implement the agent functionality.

Running the Project
1. Execute the Agents
Run the following command to execute the agents:

bash
Copy
Edit
crew run
2. Review the Results
Once the agents finish executing, the output will be saved in a Markdown file (reports.md). You can view this report to see the summarized Kubernetes trends.

