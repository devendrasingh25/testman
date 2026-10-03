# Testman

**An API and WebSocket testing platform** for sending HTTP requests, debugging real-time connections, and collaborating with a team, all from the browser.

Live demo: [testman-nu.vercel.app](https://testman-nu.vercel.app/sign-in) &nbsp;|&nbsp; Screenshot: _add `public/screenshot.png`_

---

## Overview

Testman is a Postman-style developer tool built with **Next.js 15 and TypeScript**. It combines a REST client, a WebSocket client, and shared team workspaces in one interface, with Gemini-powered assistance for naming requests and generating JSON request bodies.

## Features

### REST API client
- Send requests with any HTTP method (GET, POST, PUT, DELETE, and more)
- Manage query params, headers, and raw JSON/text bodies
- Pretty-printed JSON responses with status, response time, and size
- Save requests into collections and revisit them from history; responses are persisted

### WebSocket client
- Connect to `ws://` and `wss://` endpoints with multiple protocols
- Send and receive messages in real time
- Inspect every message with its direction, payload, size, and timestamp
- Save messages for later inspection

### Workspaces and collaboration
- Create multiple workspaces
- Invite teammates with unique invite links
- Role-based access (Admin, Member)
- Member avatars with hover tooltips

### AI assistance (Gemini)
- Suggests names for new requests
- Generates JSON queries for request bodies

### Developer experience
- Raw body editor with JSON validation, auto-format, and copy to clipboard
- Persistent client state with Zustand
- Responsive UI built with shadcn/ui and Tailwind CSS

## Tech stack

| Area | Tools |
| --- | --- |
| Framework | Next.js 15 (App Router, Server Actions) |
| Language | TypeScript |
| Database | PostgreSQL with Prisma ORM |
| State and data | Zustand, TanStack Query |
| UI | Tailwind CSS, shadcn/ui, Lucide icons |
| Editor | Monaco Editor |
| Auth | Better Auth (GitHub and Google sign-in) |
| AI | Google Gemini |
| Deployment | Vercel |

## Architecture

```
app/          Routes, API handlers, workspace and invite pages
components/   Reusable UI components
modules/      Feature modules: auth, invites, requests, websockets
lib/          Shared utilities: database, auth, store
```

## Credits

Based on the open-source [postman-clone](https://github.com/Aestheticsuraj234/postman-clone) by Aestheticsuraj234, released under the MIT License.
