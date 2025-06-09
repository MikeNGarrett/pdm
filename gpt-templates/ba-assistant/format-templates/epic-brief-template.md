<!--
  Title: Epic Brief Template
  Purpose: Define a Jira Epic in one page so designers, developers, QA, and stakeholders share the same understanding.
  Inputs:
    {Epic_ID}, {Epic_Title}, {Objective}, {Background}, {Summary},
    {Goals}, {Success_Metric?}, {Timeline_Table?}, {Key_User_Stories?},
    {Acceptance_Criteria}, {Definition_of_Done}, {Risks}, {Assumptions},
    {Dependencies?}, {Stakeholders}, {Confluence_Space?}, {Ancestor_ID?}
  Usage:
    1. Copy entire file into ChatGPT.
    2. Replace placeholders with real data.
    3. Provide Confluence fields if you want the BA GPT to auto-publish.
-->

h1. Epic Brief – {Epic_Title}  

Version: 1.0.0

---

|| Jira Epic ID     || {Epic_ID} ||  
|| Status           || [Backlog \| In Progress \| Done] ||  
|| Objective        || {Objective} ||  
|| Success Metric   || {Success_Metric?} ||  
|| Confluence Space Key || {Confluence_Space?} ||  
|| Parent Page ID (optional) || {Ancestor_ID?} ||  

---

h2. 1. Background / Context  

{Background}

---

h2. 2. Summary  

{Summary} 

---

h2. 3. Goals  

- {Goal 1}  
- {Goal 2}  


---

h2. 4. Timeline / Phases  {Timeline_Table?}  

| Phase | Dates | Description |  
|-------|-------|-------------|  
| Strategy Review | | |  
| Design Phase    | | |  
| … | | |  


---

h2. 5. Key User Stories  {Key_User_Stories?}  

| Story ID | Title | Status |  
|----------|-------|--------|  

---

h2. 6. Acceptance Criteria (AC)  

{Acceptance_Criteria} 

---

h2. 7. Risks & Assumptions  

*Risks* – {Risks} 
*Assumptions* – {Assumptions}

---

h2. 8. Dependencies  {Dependencies?}  

- {Dependency 1}  
- {Dependency 2}

---

h2. 9. Stakeholders & Team  

| Name | Role | Engagement |  
|------|------|------------|  
| {Name} | {Role} | {Weekly sync} |

---

h2. 10. Attachments & References  

- {Link 1} (strategy deck, design file, etc.)  
- {Link 2}

---

> **Internal QA Gate:** Before publishing, ensure no `{Placeholder}` text remains and all AC & DoD items are mapped to user stories or tasks.