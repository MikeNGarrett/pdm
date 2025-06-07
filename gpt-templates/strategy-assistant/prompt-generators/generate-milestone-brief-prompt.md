<!--
  Title: Milestone‑Brief Prompt Generator
  Purpose: Build a Milestone Brief prompt by collecting key info interactively.
  Inputs:
    {Milestone_Name}
    {Target_Quarter}
    {Primary_Epics}
    {Goals}
    {KPIs}
    {Stakeholders}
    {Budget}
  Usage:
    1. Paste this generator into ChatGPT.
    2. Provide answers to each question.
    3. Assistant returns a Milestone‑Brief prompt that follows milestone-brief-template.md.
-->

### **Step 1 – Collect Milestone data**  
Sequentially ask:

1. *Milestone name and target quarter?* (e.g., “Self‑Serve Onboarding – Q3 2025”)  
2. *List primary epics/projects inside this milestone.*  
3. *List 1‑3 high‑level goals for the milestone.*  
4. *Key KPIs & targets for each goal?*  
5. *List primary stakeholders & roles (exec sponsor, PM, etc.).*  
6. *Budget or effort estimate (XS…XL or dollar)?*  

---

### **Step 2 – Output the Milestone‑Brief Prompt**  

Return the following block with populated fields:

```prompt
Milestone Brief: {Milestone_Name}

Target quarter: {Target_Quarter}
Primary epics: {Primary_Epics}
Goals: {Goals}
KPIs: {KPIs}
Stakeholders: {Stakeholders}
Effort / Budget: {Budget}

Follow milestone-brief-template.md to flesh out
scope, risks, roadmap, and next steps. Ask clarifying
questions if any field is unclear or missing.
```