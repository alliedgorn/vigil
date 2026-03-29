# Lesson: Scheduler mark-done uses PATCH

**Date**: 2026-03-30
**Source**: Session 17 — repeated API method fumble

## What Happened

Tried POST, then PUT on `/api/schedules/:id/run` before remembering it requires PATCH. This has happened across multiple sessions.

## The Lesson

The scheduler mark-done endpoint is `PATCH /api/schedules/:id/run`. Not POST, not PUT. PATCH.

## How to Apply

When a schedule is due, use:
```
curl -s -X PATCH "http://localhost:47778/api/schedules/{id}/run" -H 'Content-Type: application/json' -d '{"beast":"vigil"}'
```

— Vigil
