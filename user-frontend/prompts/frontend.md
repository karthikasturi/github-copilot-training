# Frontend Prompt: User Management System

## Role
You are a senior frontend engineer building a clean, maintainable UI for a backend-driven system.

## Goal
Build a Next.js (Node.js) frontend that interacts with a Python FastAPI User Management REST API.

The UI should allow users to view, create, update, and delete users.

## Explicit Scope

### Framework & Technology Stack
- **Framework:** Next.js (App Router preferred)
- **Language:** TypeScript
- **Styling:** Tailwind CSS
- **API Interaction:** fetch / axios (no server actions required)
- **Backend Base URL:** `http://localhost:8000`

### API Endpoints
The backend follows REST conventions:
- `GET /users` - List all users
- `GET /users/{id}` - Get user by ID
- `POST /users` - Create new user
- `PUT /users/{id}` - Update user
- `DELETE /users/{id}` - Delete user

### UI Features
- Display list of users
- Form to create a new user
- Ability to edit and delete a user
- Show loading and error states
- Display backend validation errors clearly

## Constraints

### Data & API Handling
- Do **NOT** hardcode user data
- Do **NOT** assume API always succeeds
- Handle non-200 responses explicitly
- Show backend error messages to the user

### Code Quality
- Keep components readable and modular
- Avoid unnecessary global state management
- Do not add authentication or advanced UI libraries

## Verification / Validation

### Error Handling
Verify API errors are handled correctly:
- Duplicate email
- Invalid email
- User not found

### Testing Checklist
- Ensure form validation exists both client-side and server-side
- Confirm UI does not break if API is unavailable
- Ensure Tailwind styles are clean and accessible

