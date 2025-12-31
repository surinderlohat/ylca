
# Diagnostics Guide

This document explains **how to collect diagnostics** for YLCA Agent.

Diagnostics help identify issues related to:
- System compatibility
- Local LLM execution
- CPU / GPU availability
- Missing or misconfigured dependencies

Please follow this guide **before opening an issue**.

---

## Why Diagnostics Are Required

YLCA Agent runs locally by default and depends on your system environment.

Most issues are caused by:
- Missing system libraries
- Unsupported GPU drivers
- Incorrect model setup
- Environment mismatches

Diagnostics allow issues to be resolved **quickly and accurately**.

---

## When to Run Diagnostics

Run diagnostics if you experience:
- Agent failing to start
- Model failing to load
- GPU not being detected
- Unexpected crashes or errors
- Performance significantly worse than expected

---

## How to Run Diagnostics

YLCA Agent provides a built-in diagnostic command or script.

Run the diagnostics using the method provided by your installation (for example, CLI or bundled diagnostic tool).

The diagnostic process typically checks:
- Operating system details
- CPU information
- GPU availability
- Driver and runtime compatibility
- Model runtime readiness

⚠️ Exact commands may differ depending on how YLCA Agent is installed.

---

## What Information Is Collected

Diagnostics output may include:
- OS name and version
- CPU and GPU identifiers
- Available memory
- Runtime capability checks
- Error messages from dependency validation

Diagnostics **do NOT** include:
- Your source code
- Repository contents
- API keys or secrets
- Personal files

You are responsible for reviewing the output before sharing it.

---

## Sharing Diagnostics

When asked to provide diagnostics:

1. Copy the **full diagnostic output**
2. Review it to ensure no sensitive data is included
3. Paste it into a GitHub issue using the **Diagnostic Report** template

Do not attach screenshots unless explicitly requested.
Text output is preferred.

---

## Common Diagnostic Outcomes

- **GPU not detected**  
  Usually caused by missing drivers or unsupported hardware.

- **Model runtime not available**  
  Indicates missing or incompatible local model dependencies.

- **Fallback to CPU**  
  GPU may be present but not usable by the runtime.

These outcomes are informational and help guide next steps.

---

## Important Notes

- Always run diagnostics **after** installation changes
- Re-run diagnostics if you update drivers or models
- Do not modify diagnostic output unless removing sensitive data

---

## Need Help?

If diagnostics are unclear:
- Include them in a GitHub issue
- Clearly describe what you were trying to do
- Mention any recent system changes

This helps resolve issues faster and avoids unnecessary back-and-forth.
