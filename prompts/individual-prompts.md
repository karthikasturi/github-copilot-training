## Phase 1 – Discovery Prompt

Explain the architecture of this application.  
Identify entry points, major features, and critical paths.  
Highlight any legacy or high-risk areas.

---

## Phase 2 – Risk Classification Prompt

Classify components by migration risk (low, medium, high).  
Suggest an incremental migration order with justification.

---

## Phase 3 – Safety Net Prompt

Generate tests that capture the current behavior of this feature.  
Include edge cases and error paths.  
Do not refactor yet.

---

## Phase 4 – Refactoring Prompt

Refactor this feature for maintainability.  
Preserve all external behavior and contracts.  
List exactly what changed and why it is safe.

---

## Phase 5 – Debugging Prompt

This change caused a failure.  
Explain the root cause using the stack trace.  
Propose the smallest possible fix and explain the reasoning.