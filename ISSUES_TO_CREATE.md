# Drafted Issues for VoNhu2901/skills-integrate-mcp-with-copilot

Below are the 14 drafted issues gathered from a comparison with other club-management repositories. Create them as GitHub issues when you're ready.

---

## 1) Add persistent database (SQLite)

**Summary:** Replace in-memory storage with a persistent database (start with SQLite).

**Acceptance criteria:**
- Add SQLAlchemy (or equivalent) models for `Activity` and `Student`.
- Persist participants and activity metadata to a DB file.
- Update `src/app.py` endpoints to use the DB.
- Provide migration / simple setup instructions in `README`.

**Labels:** enhancement, backend, database
**Estimate:** medium

---

## 2) Add authentication and roles (students + admins)

**Summary:** Add user accounts, login, and role-based access (admin vs student).

**Acceptance criteria:**
- Implement simple auth (session or JWT) and registration for students.
- Admin role can create/edit/delete activities.
- Protect admin endpoints; sign-up/unregister remain available to students.

**Labels:** enhancement, auth, backend
**Estimate:** medium

---

## 3) Add admin dashboard for activity management

**Summary:** Provide a simple UI for admins to create/edit/delete activities and view signups.

**Acceptance criteria:**
- New `/admin` static pages or SPA for managing activities and participants.
- Admin flows call protected API endpoints.
- Basic validation for activity creation (name, schedule, max participants).

**Labels:** enhancement, frontend, admin
**Estimate:** medium

---

## 4) Enforce capacity and add waitlist support

**Summary:** Prevent signups past `max_participants`; add optional waitlist.

**Acceptance criteria:**
- API returns proper error when full; optionally add `waitlist` entry.
- Admin can view and promote waitlisted students.

**Labels:** enhancement, backend
**Estimate:** small

---

## 5) Add email notifications and bulk mailer

**Summary:** Send signup confirmation emails and provide admin bulk-mail to participants.

**Acceptance criteria:**
- Integrate SMTP/email (config via env vars).
- Send confirmation on signup and notifications for cancellations/changes.
- Admin endpoint to send bulk email to activity participants.

**Labels:** enhancement, notifications
**Estimate:** medium

---

## 6) Add certificate generation and export (PDF/CSV)

**Summary:** Allow admins to generate certificates for participants and export participant lists.

**Acceptance criteria:**
- CSV export for an activity.
- PDF certificate generation template per participant (basic).

**Labels:** enhancement, export
**Estimate:** medium

---

## 7) Add calendar integration (iCal / Google Calendar export)

**Summary:** Allow users to add activity schedules to calendars.

**Acceptance criteria:**
- Provide iCal (.ics) download for activities.
- Document how to add to Google Calendar (link or instructions).

**Labels:** enhancement, integrations
**Estimate:** small

---

## 8) Improve search & discovery (filters, pagination)

**Summary:** Add filtering (by day, availability) and pagination for `/activities`.

**Acceptance criteria:**
- Support query params to filter and paginate results.
- Client UI supports filtering and paged lists.

**Labels:** enhancement, api, frontend
**Estimate:** small

---

## 9) Add mobile-friendly UI / responsive improvements

**Summary:** Improve frontend responsiveness and consider a mobile-first layout.

**Acceptance criteria:**
- Static UI passes basic mobile layout checks.
- Consider a roadmap for a mobile app or mini-program.

**Labels:** enhancement, frontend
**Estimate:** small

---

## 10) Add third-party auth (OAuth) and Firebase option

**Summary:** Add optional OAuth login and document Firebase integration for auth/data.

**Acceptance criteria:**
- Provide a stubbed OAuth flow or docs to enable social login.
- Document Firebase alternative architecture.

**Labels:** docs, auth, integrations
**Estimate:** medium

---

## 11) Add realtime updates (WebSocket) for participant lists

**Summary:** Use WebSockets to push participant updates to connected clients.

**Acceptance criteria:**
- Implement a simple WS endpoint to broadcast signup/unregister events.
- Update frontend to subscribe for live changes.

**Labels:** enhancement, realtime
**Estimate:** medium

---

## 12) Add analytics & reporting

**Summary:** Track participation metrics and add simple reports for admins.

**Acceptance criteria:**
- Record signups with timestamps.
- Admin report endpoint showing participation counts and trends.

**Labels:** enhancement, analytics
**Estimate:** medium

---

## 13) Add Docker and basic deployment docs

**Summary:** Provide Dockerfile and docker-compose for local and production-like runs.

**Acceptance criteria:**
- Add `Dockerfile` + optional `docker-compose.yml`.
- Update `README` with run and deploy steps.

**Labels:** devops, docs
**Estimate:** small

---

## 14) Improve API (pagination, errors, docs)

**Summary:** Harden the API: consistent error responses, pagination, OpenAPI docs improvements.

**Acceptance criteria:**
- Standardized error schema.
- Add pagination to `/activities`.
- Ensure OpenAPI docs include new endpoints and auth details.

**Labels:** enhancement, api, docs
**Estimate:** small

---

If you'd like, I can now:
- create these as actual GitHub issues (I can do that if you grant GitHub access or if the environment supports issue creation), or
- open a PR that adds these drafts as files under `.github/ISSUE_TEMPLATES/` or `docs/` for manual creation.

Tell me which you'd prefer (create issues now, add as files, or tweak draft content).