# GitHub Copilot Prompt Templates – SDLC Playbook

> **Purpose:** Provide a simple, repeatable, language-agnostic way to use GitHub Copilot across the entire SDLC — safely, responsibly, and production-ready.

This playbook focuses on **how to think**, **how to structure prompts**, and **how to refine outputs**, not on any specific framework or language.

---

## 1. How to Use This Playbook (Read First)

### Key Principles

* Copilot is an **assistant**, not an author
* Every AI output must be **understood, reviewed, and validated**
* Prompts are **engineering artifacts**, not chat messages

### Universal Prompt Structure

Every prompt should contain:

1. **Context** – what exists today
2. **Task** – what you want done
3. **Constraints** – rules, standards, limits
4. **Output expectation** – what format and scope
5. **Validation request** – explanation, risks, tests

---

## 2. Global Project Instruction Template (Use Once)

Use this as **GitHub Copilot Instructions** or as the first prompt in a session.

```
You are assisting on a software project.

Project context:
- Language(s): <language>
- Framework(s): <framework>
- Project type: <new / migration / refactor>
- Coding standards: readable, maintainable, production-grade
- Security: follow secure coding practices; never assume trust
- Testing: code must be testable
- Responsibility: suggestions only; I will review and decide

Do not:
- Invent APIs or libraries
- Change behavior unless explicitly asked
- Skip error handling or validation
```

---

## 3. SDLC Phase Prompt Templates

---

### Phase 1: Requirement Understanding & Discovery

**Goal:** Understand before building

**Prompt Template:**

```
Analyze the following code / description.

Tasks:
- Summarize the business functionality
- List key inputs and outputs
- Identify assumptions and unclear areas
- Highlight potential risks

Do NOT suggest code changes yet.
```

**When to Use:**

* Legacy systems
* Poor documentation
* Migration projects

---

### Phase 2: Design & Architecture

**Goal:** Shape decisions, not implementations

**Prompt Template:**

```
Propose a high-level design for this feature/system.

Constraints:
- Maintain existing behavior
- Follow separation of concerns
- Optimize for maintainability

Output:
- Suggested structure
- Component responsibilities
- Trade-offs and assumptions

Do not generate full code.
```

---

### Phase 3: Implementation / Migration

**Goal:** Generate constrained, reviewable code

**Prompt Template:**

```
Implement the following requirement based on the agreed design.

Constraints:
- Preserve existing behavior
- Follow project coding standards
- Include basic error handling
- Keep changes scoped to this feature

After generating code:
- Explain the logic
- List assumptions made
```

---

### Phase 4: Testing & Validation

**Goal:** Prove correctness

**Prompt Template:**

```
Generate automated tests for the following behavior.

Requirements:
- Cover normal cases and edge cases
- Validate error handling
- Avoid testing implementation details

After generating tests:
- Explain what is covered
- Identify gaps or risks
```

---

### Phase 5: Refactoring & Code Quality

**Goal:** Improve without breaking behavior

**Prompt Template:**

```
Refactor this code to improve readability and maintainability.

Constraints:
- Do not change external behavior
- Preserve public interfaces
- Avoid unnecessary abstractions

Explain each refactoring decision.
```

---

## 4. Production Readiness Prompt Templates

Production readiness should be **incremental**, not one big step.

---

### Reliability & Failure Handling

```
Review this code for reliability concerns.

Focus on:
- Failure scenarios
- Timeouts and retries
- Graceful degradation

Suggest improvements without changing core behavior.
```

---

### Security Hardening

```
Review this code for security risks.

Focus on:
- Input validation
- Authentication and authorization assumptions
- Sensitive data handling

List risks and recommended mitigations.
```

---

### Observability & Debuggability

```
Suggest logging, metrics, and error reporting improvements.

Constraints:
- Avoid sensitive data in logs
- Logs should support production debugging

Explain why each signal is useful.
```

---

### CI/CD & Deployment Readiness

```
Prepare this project for automated CI/CD.

Tasks:
- Suggest test execution steps
- Identify quality gates
- Highlight rollback considerations

Do not assume a specific CI tool unless specified.
```

---

### Performance & Scalability

```
Review this code for performance risks.

Focus on:
- Inefficient patterns
- Resource usage
- Scalability limits

Explain trade-offs clearly.
```

---

## 5. Hallucination Detection Prompt (Mandatory)

Use after any non-trivial AI output.

```
Review the previous output.

Tasks:
- Identify anything that may be incorrect or assumed
- Flag APIs, libraries, or configurations that need verification
- Highlight areas requiring human confirmation
```

---

## 6. Prompt Refinement Process (Teach This)

1. Start with **understanding**, not generation
2. Narrow scope aggressively
3. Add constraints explicitly
4. Force explanation
5. Validate with tests or docs
6. Refine and re-run

> Better prompts come from better engineering thinking.

---

## 7. Final Guidance for Attendees

* Never accept AI output blindly
* Treat prompts like code
* Review before commit
* Test before merge
* You remain accountable

AI accelerates work — **responsibility remains human**.

---

**End of Prompt Templates Playbook**

