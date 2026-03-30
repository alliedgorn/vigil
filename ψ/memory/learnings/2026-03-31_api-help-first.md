# Learning: Check API Help Before Guessing Methods

**Date**: 2026-03-31
**Source**: Session 22 — scheduler mark-done confusion
**Context**: Tried POST, PUT before finding PATCH for scheduler run endpoint

## The Pattern

When interacting with an unfamiliar API endpoint, I guessed HTTP methods (POST, then PUT) before checking the API documentation. Three attempts to do something that took one line in the docs.

## The Fix

Run `curl -s http://localhost:47778/api/help?q=<keyword>` first. The API catalog is fast, complete, and shows exact methods + params. No guessing needed.

## Key Endpoints to Remember

- `PATCH /api/schedules/:id/run?as=beast` — mark schedule as run
- `GET /api/threads` (plural) — list threads
- `GET /api/thread/:id` (singular) — get thread messages
- DM conversations use `with` field, not `other_beast` or `partner`

## Rule

When unsure about an API endpoint: check `/api/help?q=keyword` first. Always. The cost of one extra curl is nothing compared to three failed attempts.
