# Capstone Projects: AI‑Assisted Migration using GitHub Copilot

**Duration:** 3–4 hours per project
**Primary Tool:** GitHub Copilot (Chat / Inline)
**Optional:** MCP servers (GitHub, Jira, Confluence, File System)
**Focus:** Application modernization + SDLC alignment with human‑supervised AI

---

## Project 1: Legacy Backend API Modernization (Python / Java)

### Target Audience

* Backend Developers (Python / Java)
* DevOps Engineers
* QA / Test Engineers

### Problem Statement

An organization maintains a **legacy monolithic REST API** written in either:

* Python (Flask, unstructured code) **or**
* Java (Spring MVC, outdated patterns)

The codebase lacks:

* Clear modular structure
* Automated tests
* CI/CD readiness
* Modern documentation

### Objective

Migrate the legacy API to a **modern, maintainable service** while preserving behavior.

* Flask → **FastAPI** (Python)
* Spring MVC → **Spring Boot (modern style)** (Java)

### SDLC Stages Covered

* Requirements understanding
* Design & architecture
* Development & refactoring
* Testing
* CI/CD & deployment readiness

### Step-by-Step Flow

#### 1. Understanding Requirements (10–15 mins)

**Activity:**

* Review legacy source code
* Identify API endpoints and expected behavior

**Copilot Prompt Example:**

> Analyze this legacy API code and summarize the business functionality, endpoints, inputs, and outputs. Highlight risky or unclear areas.

Human Role: Validate functional understanding

---

#### 2. Design & Architecture (15–20 mins)

**Activity:**

* Decide folder structure
* Define DTOs / schemas

**Copilot Prompt Example:**

> Propose a modern FastAPI / Spring Boot project structure for this application. Include layers, error handling, and validation.

Optional MCP:

* Use GitHub MCP to store design notes in repo

---

#### 3. Migration & Refactoring (60–75 mins)

**Activity:**

* Rewrite endpoints
* Improve readability and standards

**Copilot Prompt Example:**

> Rewrite this endpoint using FastAPI best practices with Pydantic models and async support, without changing behavior.

Human Role: Code review, approve changes

---

#### 4. Testing & Validation (30 mins)

**Activity:**

* Create unit tests
* Validate backward compatibility

**Copilot Prompt Example:**

> Generate pytest / JUnit tests covering normal cases, edge cases, and error handling for this API.

---

#### 5. CI/CD & Deployment Readiness (20 mins)

**Activity:**

* Add GitHub Actions pipeline
* Prepare Dockerfile

**Copilot Prompt Example:**

> Create a GitHub Actions workflow to run tests, build the project, and fail on coverage below 80%.

---

### Outcome

* Modernized backend service
* Tests + CI pipeline
* Demonstrated safe AI‑assisted migration

---

## Project 2: Frontend / Mobile Application Modernization

### Target Audience

* Frontend Developers (React / Next.js)
* Mobile Developers (React Native / Flutter)
* UX‑focused engineers

### Problem Statement

A customer-facing UI is:

* Built with outdated components
* Poorly documented
* Hard to maintain

### Objective

Modernize UI while preserving UX behavior.

Examples:

* React → **Next.js App Router**
* React Native class components → **Functional components with hooks**

### SDLC Stages Covered

* Requirement interpretation
* UI design alignment
* Development
* Testing
* Performance review

### Step-by-Step Flow

#### 1. UX & Requirement Understanding (10 mins)

**Copilot Prompt Example:**

> Review this UI code and describe the user flows, screens, and reusable components.

---

#### 2. Design Alignment (15 mins)

**Activity:**

* Map components to design intent

**Copilot Prompt Example:**

> Suggest a modern component structure for this UI using best practices for maintainability.

Optional MCP:

* Figma MCP (if available) for design reference

---

#### 3. Refactoring & Migration (60 mins)

**Copilot Prompt Example:**

> Refactor this component to a functional component using hooks and improve state management.

---

#### 4. Testing & Quality (20–30 mins)

**Activity:**

* Add UI tests

**Copilot Prompt Example:**

> Generate Playwright / Jest tests for these user flows.

---

#### 5. Performance & Readiness (15 mins)

**Copilot Prompt Example:**

> Identify performance improvements and suggest code-level optimizations.

---

### Outcome

* Cleaner UI architecture
* Testable components
* AI‑assisted UI modernization experience

---

## Project 3: Test Automation & DevOps Enablement

### Target Audience

* QA / Test Engineers
* DevOps Engineers
* SREs

### Problem Statement

A project has:

* Manual testing
* No CI feedback loop
* No deployment confidence

### Objective

Introduce **automation-first quality gates** using AI assistance.

### SDLC Stages Covered

* Testing
* CI/CD
* Deployment
* Observability

### Step-by-Step Flow

#### 1. Test Strategy Definition (10 mins)

**Copilot Prompt Example:**

> Based on this codebase, propose a test pyramid including unit, integration, and e2e tests.

---

#### 2. Automated Test Creation (45–60 mins)

**Copilot Prompt Example:**

> Generate pytest / Playwright tests for critical workflows with clear assertions.

---

#### 3. CI/CD Integration (30 mins)

**Copilot Prompt Example:**

> Create a GitHub Actions pipeline with test stages and artifact reporting.

Optional MCP:

* GitHub MCP for workflow creation

---

#### 4. Deployment & Monitoring Readiness (20 mins)

**Copilot Prompt Example:**

> Suggest Prometheus metrics and Grafana dashboards relevant to this application.

---

### Outcome

* Automated quality gates
* CI confidence
* Clear DevOps value of AI assistance

---

## Evaluation Criteria (Common)

* Correctness of migration
* Prompt quality and refinement
* Human review decisions
* Test coverage
* SDLC alignment

---

## Key Learning Outcomes

* Apply GitHub Copilot across SDLC stages
* Practice prompt refinement with human oversight
* Understand safe, enterprise‑ready AI usage
* Deliver real value within 3–4 hours

---

**End of Capstone Projects**

