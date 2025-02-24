# ReadME

## Issue Tracker

A comprehensive full-stack web application designed for tracking, managing, and visualizing project issues. This project leverages a modern stack including Next.js, React, and TypeScript—ensuring maintainable code, clear data modeling, and an intuitive UI.

---

### Features

#### Issue Management

- Create, update, and remove issues.
- Track status changes with presets: Open, In Progress, and Closed.
- Assign issues to specific users.

#### Authentication & Authorization

- Protected routes using NextAuth.js.
- Google OAuth provider for secure sign-in.

#### Dashboard and Analytics

- A dynamic dashboard displaying a summary of issues.
- Visual representations of issue distribution (e.g., bar charts using Recharts).

#### User Assignments

- Assign issues to registered users.
- Quickly view who is responsible for each issue.

#### Responsive UI

- Designed to work smoothly on both mobile and desktop.
- Built with Tailwind CSS and Radix UI for flexible, accessible styling.

#### Validation & Error Handling

- Zod-based schema validation to ensure data correctness.
- Prisma’s robust error handling for database-level operations.

#### Real-Time-Like Updates

- React Query for efficient data fetching and caching.
- Autorefreshing pages and queries to keep data in sync with minimal overhead.

#### Role-Based Middleware (Future Enhancement)

- Uses NextAuth’s middleware to protect routes; can be extended for fine-grained role-based access.

---

### How It Works (Technical Perspective)

#### Frontend

- Built with Next.js 13 and React 18.
- Uses server-side rendering for initial data (e.g., on the dashboard or issues list).
- Client-side transitions for interactive pages (issue editing, assignment, etc.).

#### Backend & API

- Next.js API routes are used for CRUD operations on issues and handling user data.
- Prisma ORM (with a MySQL database) to manage all data interactions.
- session-based or JWT-based authentication managed by NextAuth.

#### Authentication

- Sign-in with Google using NextAuth.js.
- Session tokens ensure secure endpoints, preventing unauthenticated access to sensitive routes.

#### Database

- Prisma schema defines the “Issue,” “User,” and related models.
- Relations allow each Issue to optionally reference a User as an assignee.

#### State Management & Data Fetching

- React Query (TanStack Query) handles caching, re-fetching, and background updates.
- Axios is used to perform HTTP requests to the Next.js API routes, returning JSON responses.

#### Visuals & Styling

- Tailwind CSS provides utility-first styling and responsiveness.
- Recharts is integrated for analytics charts.
- Radix UI used for design primitives (buttons, dropdowns, etc.) that are both accessible and customizable.
