# Backend API Prompt: User Management System

## Role
You are a senior backend engineer designing a production-quality REST API.

## Goal
Build a Python FastAPI-based User Management API that will be consumed by a Node.js / Next.js frontend application.

The API should support clean, predictable CRUD operations for users.

## Explicit Scope

### Framework & Architecture
- **Framework:** FastAPI
- **API Style:** REST (JSON over HTTP)
- **Resource:** User
- **Data Storage:** In-memory (dictionary or list), no database
- **Schema Validation:** Use Pydantic models for request/response schemas

### User Model
- `id`: integer (auto-generated)
- `name`: string (required, non-empty)
- `email`: string (required, valid email, unique)

### Operations
- Create user
- Get user by id
- List users
- Update user
- Delete user

## Constraints

### Validation
- Validate input strictly (missing fields, invalid email)
- Enforce unique email constraint

### HTTP Status Codes
- **201** for create
- **200** for read/update
- **404** for not found
- **400 or 422** for validation errors

### Error Response Format
All error responses must follow this consistent JSON structure:
```json
{
  "error_code": "STRING_CODE",
  "message": "Human readable explanation"
}
```

### Best Practices
- Keep code simple and readable
- Do **NOT** add authentication, authorization, or database logic
- Avoid unnecessary abstractions or over-engineering

## Verification / Validation

Ensure each endpoint behaves correctly for:
- Missing user
- Duplicate email
- Invalid email format

Additional checks:
- Verify that response models do not leak internal state
- Code should be suitable for frontend consumption without modification
