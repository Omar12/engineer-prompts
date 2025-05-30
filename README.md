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

Absolutely! As an expert prompt engineer focused on software development, I’ll guide you in crafting clear, precise, and structured prompts that get the most effective results from AI—whether you’re generating code, debugging, reviewing, or designing systems.

⸻

🧠 PRINCIPLES OF EFFECTIVE SOFTWARE DEVELOPMENT PROMPTS
	1.	Be specific about the task
Avoid: “Generate code for a login system.”
Use: “Write a React component that displays a login form with email and password fields, validates inputs on blur, and submits the form to a POST /login endpoint.”
	2.	Include all technical constraints
Mention the language, framework, libraries, data formats, etc.
Example: “Use TypeScript with React and TailwindCSS. Input should be typed using Zod schema.”
	3.	Structure your prompt
A clear layout improves results dramatically:

### Task:
### Context:
### Requirements:
### Input/Output Examples:


	4.	Add edge cases or testing expectations
This helps the model generate more robust and usable code.
	5.	Use the right tone and role for the AI
Prompt it to behave like a senior engineer, architect, or code reviewer for clearer thinking.

⸻

🔧 TEMPLATE FOR PROMPTING SOFTWARE CODE GENERATION

You can reuse this template depending on the type of development task.

### Role:
Act as a [Senior Frontend Engineer | Backend Developer | Software Architect].

### Task:
[Explain the goal concisely.]

### Context:
- [Mention relevant business logic or use case.]
- [Mention tech stack: language, framework, libraries.]

### Requirements:
- [Specific features or constraints.]
- [Performance or readability expectations.]

### Input:
- [Example of what is passed in.]

### Output:
- [What should be returned or rendered.]

### Edge Cases:
- [List any exceptions, empty states, invalid inputs.]

### Format:
- [Code only | Code with comments | Code with explanation]


⸻

💡 EXAMPLES

🔹Example 1 – Generate a React Component with Validation

Act as a Senior Frontend Engineer.

Task:
Write a React component in TypeScript for a newsletter signup form.

Context:
- We're using React 18, TypeScript, and TailwindCSS.
- The backend expects a POST request to /api/signup with { email }.

Requirements:
- Validate email format using Zod.
- Disable the submit button when the form is invalid.
- Show error messages inline.

Input:
- An empty form with a single email field.

Output:
- A styled form with real-time validation and submit handler.

Edge Cases:
- Invalid email format
- Empty input

🔹Example 2 – Debug an Error

Act as a senior JavaScript engineer.

Task:
Help me debug this error: "TypeError: Cannot read properties of undefined (reading 'map')".

Context:
- This happens in a React component.
- I suspect the prop `items` is sometimes undefined.

Code:
```tsx
function List({ items }) {
  return (
    <ul>
      {items.map(item => <li key={item.id}>{item.name}</li>)}
    </ul>
  );
}

What is the best way to fix this?

---

## ✅ PROMPTING CHECKLIST FOR SOFTWARE DEVELOPMENT

Before submitting a prompt, ask yourself:
- [ ] Did I clearly define the **task**?
- [ ] Did I provide the **tech context** (language, tools)?
- [ ] Did I include **input/output expectations**?
- [ ] Did I define **edge cases** or **constraints**?
- [ ] Did I format it clearly?

---

Would you like help generating reusable prompt templates for specific software tasks like:
- Component generation
- API design
- Unit testing
- Linting or formatting
- Code review feedback
- Architecture explanation

Just let me know your use cases, and I’ll tailor prompt templates for them.


