h1. Functional Requirements Document (FRD)

Version: 1.0  

|| Priority || {status:MEDIUM} ||
|| Size     || [Small \| Medium \| Large] ||

---

h2. 1. Overview  

h3. 1.1 Purpose  
Describe the objective of the feature or component in **one sentence**.

h3. 1.2 Background / Context  
Brief context explaining *why* this work is needed (business driver, user pain, etc.).

h3. 1.3 Scope  
*In Scope* – bullet list of what is included.  
*Out of Scope* – bullet list of what is not included.

---

h2. 2. Goals & KPIs  

|| *Business Goals* ||  
| • Goal 1 – {text} |  
| • Goal 2 – {text} |

|| *Key Performance Indicators (KPIs)* ||  
| • KPI 1 – {text} |  
| • KPI 2 – {text} |

---

h2. 3. Functional Requirements  

h3. 3.1 Feature Summary  
Describe core feature capabilities in plain language.

h3. 3.2 Requirement Details  
|| *ID* || *Requirement* || *Priority* || *Notes / Business Rule* ||  
| FR-1 | {text} | High | — |  
| FR-2 | {text} | Medium | [Link to rule] |  

h3. 3.3 Non-Functional Requirements  
|| *NFR ID* || *Requirement* || *Metric / Target* ||  
| NFR-1 | Performance | Response < 500 ms |  
| NFR-2 | Accessibility | WCAG 2.2 AA compliance |

---

h2. 4. Content & Data Structure  

h3. 4.1 Data Model / Fields  
|| *Field* || *Type* || *Required* || *Description* ||  
| Title | Text | Yes | Main heading |  
| Image | Media | Optional | 3:2 ratio |  
| … |  |  |  |

h3. 4.2 Sample JSON / Payload  
```json
{
  "title": "Sample",
  "image": "/sample.jpg"
}