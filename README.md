# 🚨 Agentic-Responder

**AI DevOps Incident Responder (Advanced)**

An intelligent, autonomous agent designed to monitor production environments, diagnose root causes of alerts, draft actionable runbooks, and escalate to the right engineers. 

## 📖 Overview

Agentic-Responder serves as your AI DevOps counterpart. It actively listens for production alerts, synthesizes data across your observability stack, and executes diagnostic workflows to reduce Mean Time To Resolution (MTTR).

It is built with a focus on advanced agentic workflows that bring order to chaotic production incidents.

## 🚀 How It Works

1. **Ingestion**: An event listener continuously ingests alerts from Prometheus.
2. **Investigation**: The agent autonomously calls log-search and metric-query tools to gather evidence.
3. **Diagnosis**: Runs a sophisticated chain-of-thought process to analyze the symptoms.
4. **Resolution**: Writes an incident summary and chooses from a set of actions:
   - 🛠️ Auto-remediate the issue
   - 📞 Page the on-call engineer (Human-in-the-loop)
   - 🎫 Open a GitHub issue for tracking

## 🛠️ Tech Stack

- **LLMs**: Claude / GPT-4o
- **Observability**: Prometheus + Grafana API
- **Logging**: Elasticsearch
- **Incident Management**: PagerDuty API
- **Core Language**: Python
- **Agent Framework**: LangGraph

## 🧠 Key Agentic Patterns

This project highlights complex AI agent implementations:
- **Parallel Tool Calling**: Gathering logs and metrics simultaneously for faster context assembly.
- **Conditional Branching**: Adapting the investigation path based on evidence found.
- **Human-in-the-loop Escalation**: Recognizing when an issue requires human judgment versus when it can be auto-remediated.

## 🎯 Stretch Goals & Future Roadmap

- [ ] **Incident Memory**: Introduce past incident memory to enable the agent to recognize and learn from historical patterns.
- [ ] **Impact Assessment**: Implement cost and blast radius estimation for proactive risk evaluation.

## 📁 Folder Structure

```text
├── agents/
│   ├── event_listener.py
│   ├── triage_agent.py
│   ├── runbook_writer.py
│   └── escalator.py
│
├── tools/
│   ├── prometheus_api.py          # Prom + Grafana
│   ├── elasticsearch_logs.py      # logs
│   ├── pagerduty_api.py
│   └── github_api.py
│
├── workflows/
│   ├── incident_workflow.py
│   └── oncall_rotation_workflow.py
│
├── app/
│   ├── api/
│   │   ├── alerts_webhook.py
│   │   ├── oncall_api.py
│   ├── core/
│   └── __init__.py
│
├── data/
│   ├── sample_alerts/
│   └── incident_templates/
│
├── outputs/
│   └── runs/
│
├── tests/
│   ├── unit/
│   └── integration/
│
├── config/
│   ├── dev.yaml
│   ├── staging.yaml
│   └── prod.yaml
│
├── README.md
└── requirements.txt
```

---
*Built to bring intelligent automation to modern incident response.*
