# Incident Agent (Agentic Incident Analysis System)

## 🎯 Overview

An **intelligent, agent-based incident analysis system** that automatically investigates production incidents using logs, metrics, alerts, chat messages, and runbooks. Produces verified incident reports and prioritized action items.

**Key Features:** Multi-Agent Architecture • Multi-Source Analysis • Evidence-Driven • Verification Layer • Evaluation Framework

---

## 📁 Project Structure

```
incident-agent/
├── data/
│   ├── scenarios/          # Test incident datasets
│   └── active/             # Currently selected incident
├── agents/                 # Triage, forensics, hypothesis, verifier
├── tools/                  # Data loader, anomaly detection, timeline
├── outputs/                # Generated reports
├── scripts/                # Scenario selector
├── evaluation/             # Evaluation logic
└── main.py                 # Main orchestration
```

---

## 🚀 Quick Start

### Installation

```bash
# Clone and navigate
git clone <repository-url>
cd incident-agent

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Usage

```bash
# 1. Select incident scenario
python scripts/select_scenario.py scenario_01

# 2. Run analysis
python main.py

# 3. View outputs
cat outputs/incident_report.md
cat outputs/action_items.json

# 4. (Optional) Run evaluation
python evaluation/evaluate.py
```

### Available Scenarios

- `scenario_01` - Payment processing slowdown
- `scenario_02` - Database connectivity issues
- `scenario_03` - Memory leak causing crashes

---

## 🎨 Design Principles

1. **Evidence-Driven Analysis** - All conclusions backed by data
2. **Conservative Approach** - No hallucinated root causes
3. **One Incident Per Run** - Focused, deep analysis
4. **Graceful Degradation** - Works with missing data
5. **Verification-First** - Multi-pass verification before finalizing

---

## 🛠️ Configuration

### Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `GROQ_API_KEY` | API key for GROQ LLM | Required |
---

## 📊 Adding New Scenarios

```bash
# Create scenario directory
mkdir -p data/scenarios/scenario_04

# Add data files: logs.json, metrics.json, alerts.json, chat_messages.json, runbooks.md

# Run analysis
python scripts/select_scenario.py scenario_04
python main.py
```

---

## 🐛 Troubleshooting

**No Data Found:** Run `python scripts/select_scenario.py <scenario_name>` first

**Import Errors:** Reinstall dependencies: `pip install -r requirements.txt`

---

## 📝 License

MIT License - see [LICENSE](LICENSE) file for details.

---

**Made with ❤️ by the Sushanth D Gowda**
