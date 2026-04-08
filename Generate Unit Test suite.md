# 🧪 Unit Test Generation Prompt Template (Production-Level)

This prompt template helps generate **comprehensive, high-quality unit tests** like a senior QA/SDET engineer — covering edge cases, robustness, and real-world scenarios. 

It forces the LLM to follow the AAA (Arrange, Act, Assert) pattern, think through failure paths, and analyze code testability before writing a single line of test code.

---

## 🧠 The Prompt Template

Copy and paste the text below into your LLM. Fill out the bracketed variables `[LIKE THIS]` before hitting send.

```text
You are a senior software engineer and testing expert with deep expertise in [TECH_STACK].

Your task is to generate comprehensive, production-quality unit tests for the given code.

---

### 🧠 Step 1: Understand Before Writing Tests (MANDATORY)
Before writing any tests, you must:
1. Analyze what the code does.
2. Identify inputs, outputs, and behavior.
3. Determine edge cases and failure scenarios.

---

### 🎯 Objective
[Explain what the code/module is supposed to do, e.g., "Processes payment transactions and updates the database"]

---

### ⚙️ Technical Requirements
* **Language:** [e.g., Python, Java, JavaScript]
* **Testing Framework:** [e.g., Pytest, JUnit, Jest]

---

### 🧩 Code Under Test
<code_under_test>
[PASTE YOUR CODE HERE]
</code_under_test>

---

### 🔍 Test Generation Goals

**Functional Testing**
* Cover all core functionalities.
* Validate expected outputs for valid inputs.

**Edge Cases**
* Empty inputs.
* Null/None values.
* Boundary conditions.
* Invalid inputs.

**Negative Testing**
* Error handling scenarios.
* Exceptions and failure paths.

**Performance (Optional)**
* Identify heavy operations and test limits.

---

### 🛡️ Best Practices to Apply
* Use clear, descriptive test naming conventions.
* Strictly follow the AAA pattern (Arrange → Act → Assert).
* Keep tests completely independent and isolated.
* Use mocks/stubs for external dependencies (DBs, APIs) where required.
* Avoid hardcoding values where possible; use factories or fixtures.

---

### 🧪 Coverage Requirements
* Ensure high test coverage (aim for 90%+).
* Cover both success (happy path) and failure scenarios.

---

### 🚫 Constraints
* Do NOT modify the original code being tested.
* Do NOT skip edge cases.
* Do NOT write redundant or overlapping tests.

---

### ✨ Extra Instructions
* If assumptions about the code's environment are needed, state them clearly.
* Prefer clarity and maintainability over cleverness or complex setup.
* Use parameterized tests where applicable to test multiple inputs cleanly.
* **Code Testability Analysis:** Identify untestable parts of the provided code (e.g., hidden dependencies, lack of dependency injection) and suggest structural improvements to make it more testable.

---

### 📂 Output Format
Please format your response exactly as follows:

1. **🧾 Test Strategy:** (Brief explanation of your approach and what you plan to mock)
2. **🚧 Testability Feedback:** (Identify untestable parts and suggest structural improvements)
3. **🧪 Test Cases List:** (Bullet points of the scenarios covered)
4. **🔧 Complete Test Code:** (The full, copy-pasteable test file)
5. **🚀 How to Run Tests:** (Command to execute the tests)
6. **📊 Coverage Notes:** (Optional notes on what is covered vs. what might need integration tests)

Now generate the unit tests step-by-step like a senior engineer.
```

---

## 📌 Usage Tips

* **Isolate the Code:** Feed the LLM one logical module or class at a time for the highest quality tests. 
* **Provide Context:** If the code relies on complex internal data structures, paste a quick JSON example or schema alongside the code so the LLM can mock it accurately.
* **Combine with Refactoring:** Since this prompt now automatically identifies untestable parts of your code, run that feedback back through your refactoring prompt to fix the architecture before finalizing your tests!
