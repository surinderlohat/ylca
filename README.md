# YLCA Agent  
**Your Logical Coding Agent**

YLCA Agent is a goal-driven coding and engineering agent designed for **logical planning, controlled execution, and user ownership**.

This repository is the **official public support and documentation hub** for YLCA Agent.

---

## Core Principle

> **Your code is your property.**  
> By default, YLCA Agent runs locally and does not send your code to the cloud.

Local execution is the default behavior.  
Any other execution mode is always an **explicit configuration choice**.

---

## What YLCA Agent Is

YLCA Agent is built to help developers **plan and execute coding tasks** using locally hosted language models, with a strong focus on:

- Transparency
- Predictability
- Diagnostics
- User control

The agent follows a **think → plan → execute** approach and avoids hidden or autonomous behavior.

---

## What This Repository Is For

This repository exists to provide:

- 📌 Bug reports and issue tracking  
- 📘 User-facing documentation  
- 🧪 Diagnostics and troubleshooting guidance  
- ⚠️ Known issues and limitations  
- 🗺️ High-level roadmap and direction  

---

## What This Repository Is NOT

This repository does **not** contain:

- Agent source code  
- Prompts or system instructions  
- Internal planning or execution logic  
- Model configuration files  
- Backend or runtime implementations  

The core YLCA Agent implementation is **not publicly hosted**.

---

## Core Features

### Local-First Execution
- Runs entirely on your machine by default
- No mandatory cloud dependency
- Suitable for private codebases and restricted environments

---

### Works with Local LLM Models
- Designed to operate with **locally hosted LLMs**
- Supports CPU and GPU execution (environment dependent)
- Model choice remains fully under user control

YLCA Agent does **not** require:
- Hosted APIs
- External inference services
- Vendor-locked model providers

---

### Built on the LLaMA Ecosystem

YLCA Agent builds on the broader **LLaMA open-model ecosystem**, enabling:

- Efficient local inference
- Cross-platform support
- Community-driven improvements

We acknowledge and appreciate the work of the **LLaMA / llama.cpp community**, whose open-source contributions make reliable local agents practical and accessible.

---

### Controlled Agent Behavior
- Goal-driven, not autonomous
- Plans actions before execution
- Executes only within explicit boundaries
- Surfaces errors instead of hiding them

This design prioritizes:
- Safety
- Debuggability
- Predictable outcomes

---

### Diagnostics-First Design
- Environment checks before execution
- Clear error messages for missing dependencies
- Explicit GPU / CPU capability reporting

YLCA Agent prefers **failing early with clarity** over silent degradation.

---

### Deployment Flexibility

While local execution is the default, YLCA Agent is designed to support:

- Local mode  
- Cloud mode  
- Hybrid mode  

Deployment mode is a **configuration choice**, not a product limitation.

---

## Code Ownership & Privacy

Your code remains yours.

By default:
- Source code stays on your system
- Model inference happens locally
- No background uploads of code or prompts occur

YLCA Agent does not silently change how or where your code is processed.

---

## Reporting Issues

Please use the **GitHub Issue Templates** provided in this repository.

When reporting a bug, include:
- Operating system
- Execution mode (local / cloud / hybrid)
- Model name (if applicable)
- Diagnostic output
- Clear reproduction steps

Issues without sufficient information may be closed.

---

## Documentation

Additional documentation is available in the [`docs/`](./docs) directory, including:

- Getting started guidance
- Diagnostics and troubleshooting
- Known limitations
- Frequently asked questions

---

## Security

For security-related concerns, please read [`SECURITY.md`](./SECURITY.md).

❗ Do **not** report security vulnerabilities via public issues.

---

## Roadmap

High-level product direction is available in [`ROADMAP.md`](./ROADMAP.md).

This roadmap intentionally avoids internal implementation details.

---

## License

This repository contains **documentation only**.

No license is granted for:
- The YLCA Agent implementation
- Internal logic
- Prompts
- Model integrations

---

## Design Philosophy (Summary)

> YLCA Agent prioritizes **logic, transparency, and user control** over hidden automation.

---

*This repository defines the public boundary of YLCA Agent.*
