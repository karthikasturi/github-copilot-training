# Hands-On Lab Guide: Mastering GitHub Copilot Fundamentals (Python API Focus)

---

## Lab Philosophy (Important)

GitHub Copilot is:

- A **code suggestion system**, not an architect
- Strong at patterns, weak at **implicit constraints**
- Highly sensitive to **context quality**
- Most effective with **human-in-the-loop control**

This lab is designed to **demonstrate Copilot behavior**, not to blindly accept its output.

---

## Prerequisites (Before Lab)

Participants should have:

- VS Code installed
- GitHub Copilot enabled (Individual / Business / Enterprise)
- Python 3.9+
- Basic REST API knowledge

Framework reference: **FastAPI (conceptual guidance only)**  
Participants may use Flask or plain Python if preferred.

---

# Lab 1 – Baseline API with Minimal Prompting

### Objective

Observe Copilot behavior with **minimal context**.

### Steps

1. Create `main.py`
2. Add only this comment:

```python
# create a simple user api
```

3. Trigger Copilot suggestions

### Observe

- Framework choice assumptions
- Missing validations
- Hardcoded logic
- Over-simplified error handling

### Trainer Demo Emphasis

Explain **why** Copilot made these assumptions.

---

## Lab 2 – Context-Rich Prompting

### Objective

Demonstrate how **explicit constraints** improve output.

### Prompt Block

```python
"""
Create a REST API using Python.

Requirements:
- CRUD operations for User
- User fields: id (int), name (string), email (string)
- Validate email format
- Return proper HTTP status codes
- Use structured error responses
- Avoid database integration (in-memory only)
"""
```

### Observe

- Better structure
- Explicit validation logic
- Clearer API contracts
- Improved HTTP semantics

### Key Teaching Point

Copilot performs best when **requirements are unambiguous**.

---

## Lab 3 – Role-Based Prompting

### Objective

Influence **design decisions**, not syntax.

### Prompt Block

```python
"""
Act as a senior backend API engineer.

Design a clean, maintainable REST API:
- Follow REST best practices
- Keep code modular
- Avoid over-engineering
- Prefer readability over cleverness
"""
```

### Observe

- Naming conventions
- Endpoint structure
- Function separation
- Reduced magic values

### Trainer Insight

Role prompts affect **architecture bias**, not correctness guarantees.

---

## Lab 4 – Prompt Iteration & Refinement

### Objective

Show **cause–effect** of prompt evolution.

### Exercise

1. Ask Copilot to add input validation
2. Then refine prompt with:

```text
Consider edge cases:
- Duplicate email
- Missing fields
- Invalid email format

Standardize error responses:
{
  "error_code": "...",
  "message": "..."
}
```

### Compare

- Initial output vs refined output
- Error consistency
- Defensive coding improvements

### Discussion

Why Copilot did **not** infer this earlier.

---

## Lab 5 – Debugging Assistance (Controlled Use)

### Objective

Use Copilot as a **debugging assistant**, not a debugger.

### Steps

1. Introduce a bug:
   - Wrong HTTP status
   - Incorrect conditional
2. Add a comment describing the issue

```python
# API returns 200 even when user is not found
```

3. Ask Copilot for suggestions

### Evaluation Checklist

- Is the fix logically correct?
- Did Copilot change unrelated code?
- Are edge cases still broken?

### Trainer Emphasis

Copilot fixes symptoms, not always **root cause**.

---

## Lab 6 – Human-in-the-Loop Review

### Objective

Reinforce **engineering accountability**.

### Review Checklist

- Requirements met?
- Input validation complete?
- Error paths covered?
- Security assumptions explicit?
- Would this pass a senior code review?

### Key Message

Copilot accelerates typing — **humans own correctness**.

---

## Common Copilot Limitations (Explicit Callout)

- No awareness of org standards unless provided
- Hallucinates APIs or libraries
- Weak at security by default
- Cannot validate runtime behavior
- Over-confident output tone

---

## Best Practices for Real Projects

- Use comments as **design constraints**
- Iterate prompts, don’t accept first output
- Review diffs, not just final code
- Treat Copilot like a junior engineer with fast typing

---

## Optional Extensions (If Time Permits)

- Store prompts alongside code as documentation
- Compare Copilot outputs across models
- Define team-level prompt standards
- Discuss Copilot + Code Review workflows

---
