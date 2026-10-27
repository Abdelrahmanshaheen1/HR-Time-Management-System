# HR Time Management System

A full-stack HR platform (NestJS backend + Next.js frontend) built as a course project, scoped as one subsystem of a larger team HR application.

## What's actually built and working

**Time Management module — fully implemented:** leave requests, attendance, and shift tracking, with complete DTOs, controllers, and services (CRUD endpoints), plus authentication (JWT via Passport.js, role-based access, bcrypt password hashing).

## What's scaffolded but not implemented

The backend also has data models and partial scaffolding for Employee Profiles, Organization Structure, Recruitment, Payroll (configuration, execution, and tracking), and Performance modules — but these are **not functionally complete** (missing DTOs, controllers, or service logic, as tracked honestly in the project's own [`backend/MISSING_IMPLEMENTATIONS_REPORT.md`](backend/MISSING_IMPLEMENTATIONS_REPORT.md)). This README leads with that distinction deliberately: the full feature list in [`PROJECT_DOCUMENTATION.md`](PROJECT_DOCUMENTATION.md) describes the platform's intended scope, not its current implementation status — read the missing-implementations report alongside it for an accurate picture of what's done.

## Stack

- **Backend:** NestJS, MongoDB via Mongoose, Passport.js + JWT, class-validator
- **Frontend:** Next.js, React, Tailwind CSS, Radix UI

See [`PROJECT_DOCUMENTATION.md`](PROJECT_DOCUMENTATION.md) for full architecture, API endpoints, database models, and setup instructions.

## Skills demonstrated

Full-stack TypeScript architecture (NestJS + Next.js), JWT-based auth with role-based access control, MongoDB schema design via Mongoose, and — just as relevantly — accurately scoping and documenting what's actually complete in a large, multi-module system rather than overstating it.
