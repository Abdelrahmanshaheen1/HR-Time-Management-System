# HR Time Management System

A full-stack HR platform (NestJS backend + Next.js frontend) built as a course project, scoped as one subsystem of a larger team HR application.

## What's actually built and working

**Time Management module — fully implemented:** leave requests, attendance, and shift tracking, with complete DTOs, controllers, and services (CRUD endpoints), plus authentication (JWT via Passport.js, role-based access, bcrypt password hashing).

## What's scaffolded but not implemented

The backend also has data models and partial scaffolding for Employee Profiles, Organization Structure, Recruitment, Payroll (configuration, execution, and tracking), and Performance modules — but these are **not functionally complete** (missing DTOs, controllers, or service logic, as tracked honestly in the project's own [`backend/MISSING_IMPLEMENTATIONS_REPORT.md`](backend/MISSING_IMPLEMENTATIONS_REPORT.md)). This README leads with that distinction deliberately: the full feature list in [`PROJECT_DOCUMENTATION.md`](PROJECT_DOCUMENTATION.md) describes the platform's intended scope, not its current implementation status — read the missing-implementations report alongside it for an accurate picture of what's done.

## Running it locally

Needs Node 18+ and a local MongoDB.

~~~bash
# backend (http://localhost:3000)
cd backend
cp .env.example .env          # set JWT_SECRET
npm ci
npm run seed:auth             # optional demo users; deletes existing employee_profiles / employee_system_roles
npm run start:dev

# frontend (http://localhost:3001), in a second terminal
cd frontend
cp .env.example .env.local
npm ci
npm run dev
~~~

`nest build` completes cleanly on the backend. The `seed:auth` demo accounts all use the password `123456`, so only use them on a local database. Details and every environment variable are in [`PROJECT_DOCUMENTATION.md`](PROJECT_DOCUMENTATION.md) and the two `.env.example` files.

## Known limitations

- Several modules are scaffolded only (see above).
- The JWT strategies fall back to a hard-coded secret when `JWT_SECRET` is unset. Always set it outside local development.
- Some frontend pages hard-code `http://localhost:3000` / `5000` as the API fallback instead of reading one shared setting; setting `NEXT_PUBLIC_API_URL` in `.env.local` covers it.

## Stack

- **Backend:** NestJS, MongoDB via Mongoose, Passport.js + JWT, class-validator
- **Frontend:** Next.js, React, Tailwind CSS, Radix UI

See [`PROJECT_DOCUMENTATION.md`](PROJECT_DOCUMENTATION.md) for full architecture, API endpoints, database models, and setup instructions.

## Skills demonstrated

Full-stack TypeScript architecture (NestJS + Next.js), JWT-based auth with role-based access control, MongoDB schema design via Mongoose, and — just as relevantly — accurately scoping and documenting what's actually complete in a large, multi-module system rather than overstating it.
