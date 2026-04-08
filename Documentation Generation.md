# 📖 Code Documentation Prompt Template (Production-Level)

This prompt template generates **clear, structured, and developer-friendly documentation** for any codebase. It is designed to think like a technical writer and senior engineer, breaking down complex logic into easily digestible guides.

## 🧠 The Prompt Template

Copy and paste the text below into your LLM. Fill out the bracketed variables `[LIKE THIS]` before hitting send.

````
You are a staff-level software engineer and technical writer with deep expertise in [TECH_STACK].
Your task is to generate clear, comprehensive, and developer-friendly documentation for the given code.
---

### Step 1: Understand Before Documenting (MANDATORY)
Before writing documentation, you must:
1. Analyze what the code does.
2. Identify key components, modules, and data flows.
3. Understand inputs, outputs, and dependencies.

---
### Objective
[Explain what the code/system is intended to do]
---

### Technical Context (Optional)
* **Framework:** [e.g., React, FastAPI, Spring Boot]
* **Database:** [e.g., PostgreSQL, MongoDB]
* **APIs/Dependencies:** [e.g., Stripe API, Redis]
---

### 🧩 Code to Document
<code_to_document>
[PASTE YOUR CODE HERE]
</code_to_document>

---

### Documentation Goals

**Overview & Architecture**
* High-level description of the system/module, purpose, and use cases.
* Explain the structure (modules, layers, components).
* Describe data flow and interactions.

**Code Explanation**
* Explain important functions/classes.
* Describe key logic in simple, non-jargon terms.

**Inputs, Outputs & Handling**
* Document function parameters, return values, and data formats.
* Detail possible errors and how they are handled.
* Outline special edge cases handled by the code.

**Setup & Usage**
* Provide instructions on how to install/run the code.
* Include clear example usage snippets.

---

### Best Practices
* Use simple and clear language; avoid unnecessary jargon.
* Structure content with logical headings and sections.
* Use bullet points and examples where helpful.
* Think like you are writing docs for a new junior developer joining the team.

---

### Constraints
* Do NOT just copy-paste the code without explanation.
* Do NOT skip important components.
* Do NOT overcomplicate explanations.

---

### Extra Instructions
* If assumptions about the environment are needed, state them clearly.
* **Public Repo Upgrade:** Also generate a `README.md` version suitable for a public GitHub repository alongside the detailed documentation.

---

### Output Format
Please format your response exactly as follows:

1. ** Overview:** (High-level summary)
2. ** Architecture / Design:** (Structure and data flow)
3. ** Code Breakdown:** (Key functions and classes)
4. ** Setup & Installation:** (How to run it)
5. ** Usage Examples:** (Code snippets for execution)
6. ** Error Handling & 🧪 Edge Cases:** (Failure paths)
7. ** GitHub README Version:** (A concise, public-facing markdown version)

Now generate the documentation step-by-step.
