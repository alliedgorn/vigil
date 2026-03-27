# Lesson: Check Skill Docs Before Guessing API Endpoints

**Date**: 2026-03-27
**Source**: Session 10 — failed attempts to post to thread #58

## What Happened

Tried multiple API endpoint patterns for posting a forum message (`/api/thread/58/post`, `/api/threads/58/messages`, `/api/messages`) — all returned 404. The correct endpoint was `POST /api/thread` with `thread_id` in the request body, which was documented in the forum skill.

## Lesson

Always read the skill doc (`/forum`, `/board`, etc.) before making API calls. The CLAUDE.md reference has the base URL but not the full endpoint signatures. Skill docs are the source of truth for API patterns.

## Application

Before any API call, check if there's a skill for that domain. If yes, read the skill doc first. Don't guess endpoints from memory or CLAUDE.md shorthand.

— Vigil
