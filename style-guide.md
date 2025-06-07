# Prompt-as-Code Style Guide  

Version: 1.0.0

---

## 1️⃣  Why treat prompts like code?  

| Benefit         | Result                                                         |
|-----------------|----------------------------------------------------------------|
| **Maintainable**| Prompts live in version control; diffs reveal every tweak.     |
| **Reusable**    | Placeholders turn one prompt into many contexts.               |
| **Self-documented** | Comment blocks explain intent, inputs, and usage.          |
| **Reviewable**  | PR-style reviews catch ambiguity before prompts hit production.|

---

## 2️⃣  File anatomy  

Every prompt file starts with a **YAML-ish comment block**—nothing in that block is sent to the model.  

```text
<!--
  Title: Strategic Brief Prompt
  Purpose: Generates a strategic brief given Objective, Context, Options.
  Inputs:
    {Objective} – one-sentence goal
    {Context}   – 2–3 bullet background
    {Options}   – list of A/B/C
  Usage:
    1. Copy entire file into ChatGPT.
    2. Replace placeholders with real data.
    3. Send the prompt unchanged (comments may stay).
-->
h1. Strategic Brief Prompt  <!-- or ## in pure Markdown -->
<…prompt body…>
```

> **Rule:** Everything before the first heading is a comment; keep it succinct but complete.

---

## 3️⃣  Placeholder syntax  

| Token                 | Meaning / Rule                           | Example                         |
|-----------------------|------------------------------------------|---------------------------------|
| `{Variable}`          | **Required** placeholder                | `{Objective}`                   |
| `{Optional?}`         | Optional—delete if not used             | `{Sub-Objective?}`              |
| `[Choice A | B]`      | Pick one value exactly as written       | `[Public | Internal]`           |
| `<…>`                 | Inline explanation; delete in use       | `<URL here>`                    |
| `<!-- comments -->`   | Comment for humans; ignored by model    | `<!-- Don’t change below -->`   |

---

## 4️⃣  Folder convention  

| Folder path                                      | Contents                                                       |
|--------------------------------------------------|----------------------------------------------------------------|
| `gpt-templates/[role]/format-templates/`         | Finished templates the assistant fills in.                     |
| `gpt-templates/[role]/prompt-generators/`        | “Meta-prompts” that create other prompts or templates.         |
| `gpt-templates/[role]/example-conversations/`    | Gold-standard prompt + response pairs for fine-tuning.         |

**`[role]` placeholder** — replace with the assistant name, e.g.:

- `strategy-assistant`
- `ba-assistant`
- `qa-assistant` (future)

The structure repeats for every role-specific assistant so tooling can glob paths like  
`gpt-templates/*/format-templates/*.md`.
---

## 5️⃣  Versioning & changelog  

- **Each file** contains a single line: `Version: x.y.z`  
  - Major = breaking structure change  
  - Minor = section added, placeholders tweaked  
  - Patch = typo or comment correction  
- **CHANGELOG.md** (root) tracks repo-wide history starting at `v1.0.0`.  
- Use Git tags (`v1.1.0`) for release snapshots.

---

## 6️⃣  Prompt file types  

| Type            | Purpose                                               | Naming rule                                 |
|-----------------|-------------------------------------------------------|---------------------------------------------|
| **Template**    | Format skeleton users fill in                         | `…-template.md`                            |
| **Prompt-Generator** | Asks Qs → outputs a tailor-made prompt           | `gpt-templates/prompt-generators/…`         |
| **Example**     | Shows a perfect conversation for fine-tuning          | `example-conversations/…-example.md`        |
| **Skeleton** (optional) | Ultra-light “blank slate” version of template | `…-skeleton.md` (keep under format-templates)|

---

## 7️⃣  Tone & content principles  

1. **Professional & concise** – no emojis, minimal filler.  
2. **Structured output** – headings, lists, tables as defined in the template.  
3. **Data clarity** – flag placeholders or missing info in a *Needs Clarification* section.  
4. **No hallucinations** – if unsure, ask follow-up.  
5. **Internal vs. Client** – default to internal tone; soften jargon if `Audience: External`.

---

## 8️⃣  Usage checklist (copy/paste in PR descriptions)  

- [ ] Comment header present with Title, Purpose, Inputs, Usage  
- [ ] All placeholders wrapped in `{}` or `[A | B]` syntax  
- [ ] File starts with `Version:` line; matches CHANGELOG if not pre-v1  
- [ ] Runs in ChatGPT 4-level models; no proprietary plugin references  
- [ ] Approved by reviewer with “Prompt-as-Code style OK” feedback

---

> *When in doubt, treat the prompt like production code: lint it, test it, and document why it exists.*