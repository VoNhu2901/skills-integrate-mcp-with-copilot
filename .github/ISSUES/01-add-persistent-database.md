# Add persistent database (SQLite)

**Summary:** Replace in-memory storage with a persistent database (start with SQLite).

**Acceptance criteria:**
- Add SQLAlchemy (or equivalent) models for `Activity` and `Student`.
- Persist participants and activity metadata to a DB file.
- Update `src/app.py` endpoints to use the DB.
- Provide migration / simple setup instructions in `README`.

**Labels:** enhancement, backend, database
**Estimate:** medium
