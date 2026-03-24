---
name: web-developer
description: Build and maintain full-stack web features using HTML, CSS, JavaScript, and PHP, including admin panels, CRUD, validation, security, and responsive UI consistency.
---

# Web Developer Skill (HTML + CSS + JS + PHP)

## Purpose
Use this skill to plan and implement production-ready web features in projects that use:
- HTML/CSS for UI
- JavaScript for interactions and validation
- PHP for server logic and CRUD
- MySQL (or similar) for persistence

## When To Use
Use this skill when the request involves one or more of the following:
- Creating new pages (user-side or admin-side)
- Building admin modules (upload, edit, delete, monitoring)
- Integrating forms with PHP backend
- Implementing authentication, authorization, and session checks
- Adding search, filtering, pagination, and dashboard metrics
- Refactoring UI to match existing design patterns

## Inputs To Collect First
Before coding, gather:
- Feature goal and success criteria
- Existing file/folder structure and naming conventions
- Required fields and validation rules
- Database tables and relationships
- Access rules (admin only, user only, public)
- Error handling and edge cases

## Workflow
1. Understand the request
- Restate the outcome in one sentence.
- Identify affected layers: UI, JS logic, PHP API/routes, database.

2. Inspect existing patterns
- Reuse navbar/footer/components already used in the project.
- Match CSS classes, spacing, typography, and existing code style.

3. Plan data flow
- Define source of truth for each field.
- Map request flow: form -> validation -> PHP handler -> DB -> response UI.

4. Implement in thin vertical slices
- Build one complete path first (create/list/edit/delete) before broadening.
- Keep changes minimal and scoped to the feature.

5. Validate behavior
- Test happy path, invalid input, empty states, and permission checks.
- Confirm links, relative paths, and asset loading.

6. Final polish
- Keep UI consistent with existing pages.
- Add concise comments only where logic is non-obvious.
- Ensure no secrets, debug dumps, or broken links remain.

## Decision Points
- If page must match existing site look: reuse global CSS and shared layout blocks.
- If feature is admin-only: enforce server-side session checks on every action page.
- If file upload is needed: validate type/size, sanitize filename, store outside executable paths when possible.
- If list can grow: implement pagination and search early.
- If operation changes data: use POST for mutations and CSRF tokens where possible.

## Admin Panel Build Order (Recommended)
1. Admin auth foundation
- Login, logout, session middleware, route guards.

2. Admin dashboard
- Cards for totals (movies, categories, users, downloads).
- Recent activity and quick actions.

3. Movie management CRUD
- Create movie (metadata + poster/file upload)
- List/search/filter movies
- Edit movie details
- Soft delete or hard delete

4. Category/genre management
- Add/edit/delete genres used by movies.

5. User monitoring
- User list, activity status, recent downloads, simple moderation controls.

6. Download/activity monitoring
- Logs, top downloads, date-range filtering.

7. Settings and maintenance
- Site settings, admin profile, password change, backup/export.

## Quality Checklist
- Security:
- Prepared SQL statements
- Password hashing (`password_hash`, `password_verify`)
- Session checks for protected pages
- Upload validation (mime/type/size)
- CSRF for critical forms

- UX:
- Matches existing navbar/footer and layout
- Mobile responsive at key breakpoints
- Clear success/error states
- Empty states for no-data pages

- Reliability:
- Server-side validation mirrors client-side rules
- Graceful handling for DB/file errors
- No PHP warnings visible in production UI

## Output Contract For Tasks
When applying this skill, produce:
- Clear list of changed files
- Brief explanation of data flow
- Verification steps performed
- Remaining risks or follow-up suggestions

## Example Prompts
- "Build admin dashboard with stats cards and recent uploads table using existing theme."
- "Create movie CRUD in PHP with poster upload, validation, and edit/delete actions."
- "Add admin-only route guard to all pages under `pages/admin` and redirect to login if session missing."
- "Implement user monitoring page with search, pagination, and last-login/download columns."

## Anti-Patterns To Avoid
- Creating new visual style that conflicts with current site design
- Trusting client-side validation alone
- Running SQL with string concatenation
- Mixing unrelated refactors with feature work
- Deleting records without confirmation or audit trail
