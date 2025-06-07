<!--
  Title: KPI Prompt Generator
  Purpose: Interactively build a custom KPI & Success Definition prompt from minimal inputs.
  Inputs:
    {Goal_List}      – comma‑separated high‑level goals
    {Owners}         – owner per goal (same order)
    {Baseline_Date}  – date from which baselines are measured
    {Cadence}        – measurement cadence (weekly / monthly / quarterly)
  Usage:
    1. Copy this entire file into ChatGPT (or your LLM).
    2. Answer the assistant’s questions one by one.
    3. The assistant will output a ready‑to‑run KPI‑Sheet prompt using `kpi-template.md`.
    4. Paste that generated prompt into a new chat; replace any remaining placeholders.
-->

### **Step 1 – Gather details**  
Ask the user these questions one at a time (stop after each until answered):

1. *What are the high‑level goals you want to track?* (Provide as comma‑separated list.)  
2. *Who is the owner for each goal?* (Match order to goals.)  
3. *What baseline date should we use for measurement?* (YYYY‑MM‑DD)  
4. *How often will you measure each KPI?* (Choose one: weekly / monthly / quarterly.)  

---

### **Step 2 – Output the KPI Prompt**  

Once answers are provided, return EXACTLY the following block (replace bracketed fields):

```prompt
KPI Sheet:
Goals: {Goal_List}
Owners: {Owners}
Baseline date: {Baseline_Date}
Measurement cadence: {Cadence}

Use kpi-template.md to map each goal to at least one KPI,
including baseline values and targets.  Ask follow‑up
questions if any KPI details are missing.
```