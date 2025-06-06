h1. Flow Diagram Template

Version: 1.0.0

---

h2. 1. Title  
`[Flow Name]`

h3. Objective  
Briefly describe the purpose of the flow in **one short sentence**.

---

h2. 2. Primary Success Flow  

{code:language=mermaid}
%% Replace the sequence diagram below with the actual steps
sequenceDiagram
    participant User
    participant System
    User->>System: [Step 1 — action / request]
    System-->>User: [Step 2 — response]
    note right of System: [Optional business rule]
{code}

> *Tip* – Mermaid `sequenceDiagram` is the default.  
> • Use `flowchart TD` for non-sequential flows.  
> • Keep step labels short; add detail in *Descriptions* if needed.

---

h2. 3. Alternate & Exception Flows  

|| Flow ID || Trigger / Condition || Steps || Outcome ||  
| ALT-1 | `[Condition diverting from primary]` | `[Steps]` | `[Result]` |  
| ERR-1 | `[Error scenario]` | `[Steps]` | `[User/system feedback]` |

---

h2. 4. Descriptions & Business Rules  

|| Step ID || Detailed Description || Business Rule / Constraint ||  
| 1 | `[Explain Step 1]` | `[e.g., must validate input]` |  
| 2 | `[Explain Step 2]` | `[e.g., must log transaction]` |

---

h2. 5. Needs Clarification  

Use this section when information is missing or ambiguous.

- `[Open question 1]`  
- `[Open question 2]`

---

h2. 6. Documented Assumptions  

- `[Assume user has an active session]`  
- `[Assume API latency < 500 ms]`

---

h2. 7. Potential Conflicts or Contradictions  

- `[If another flow handles refunds, remove refund logic here]`

---

*QA Alignment* – Each acceptance criterion in related stories should trace to a **Step** or **Business Rule** above, and error flows must specify expected HTTP codes or UI feedback.