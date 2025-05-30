# 🧰 LLM Prompt Template Pack for Software Dev Tasks

 Below is a Prompt Engineering Template Pack for Software Development, designed for reuse and integration into your tools or workflow (e.g., with VS Code snippets, CLI tools, or custom GPT wrappers).

---

## 🧱 1. Code Generation

```
Generate [language] code that [brief functionality description].

Requirements:
- Input: [input types or parameters]
- Output: [expected output or return type]
- Constraints: [frameworks, no external libs, performance, etc.]

Example: 
Generate a Python function that takes a list of numbers and returns the median value. No external libraries.
```

---

## 🧼 2. Code Refactoring

```
Refactor the following code to improve [clarity / performance / DRY / readability].

Constraints:
- [e.g., no external libraries, keep logic the same, modern syntax only]

Original Code:
[Insert code snippet here]
```

---

## 🐞 3. Debugging

```
Analyze and fix the following code. It's producing this error: “[error message]”.

Expected behavior: [what should happen]
Actual behavior: [what happens instead]

Code:
[Insert buggy code here]

What’s the root cause, and how can I fix it?
```

---

## 🧪 4. Unit Test Generation

```
Write [unit/integration] tests for the following [function/class/component] using [testing framework].

- Cover normal use cases and edge cases.
- Use proper test naming conventions.

Code:
[Insert code to test]
```
---

## 📘 5. Documentation / Inline Comments

```
Document the following [function/class] using [JSDoc/docstring/inline comments].

Code:
[Insert code snippet]

Style guide: [Optional—Google, PEP-8, etc.]
```

---

## 🧠 Bonus: Explain Code

```
Explain what the following [JavaScript/Python/etc.] code does, line by line.

Code:
[Insert code here]

Use plain language suitable for a junior developer.
```

---

## 🔌 Suggested Integrations

VS Code Snippet (example for code generation)

```
"LLM: Generate Function": {
  "prefix": "llm-gen-func",
  "body": [
    "Generate ${1:language} code that ${2:brief functionality}.",
    "",
    "Requirements:",
    "- Input: ${3:input details}",
    "- Output: ${4:output details}",
    "- Constraints: ${5:constraints}",
    "",
    "Example: ${6:optional example}"
  ],
  "description": "Template for generating functions using LLM"
}
```

CLI/Terminal Use (bash alias or script)

alias gpt-gen='gh copilot prompt "Generate JavaScript code that does X..."'

---
