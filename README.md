# LifeOS AI

LifeOS AI is an adaptive personal operating system that brings schedules, tasks, messages, notes, and documents into one intelligent daily plan. This OpenAI Build Week prototype includes a responsive dashboard, AI planning, interactive tasks, connected-source demos, and three user-selectable themes.

## Features

- OpenAI Responses API integration with safe demo fallback
- Daily timeline, priority tasks, focus score, unified sources, and proactive insights
- Aurora, Midnight, and Warm Editorial themes saved in the browser
- Today, Inbox, Calendar, Tasks, Notes, Documents, Sources, and Settings views
- Responsive desktop, tablet, and mobile layouts
- Safe behavior: LifeOS proposes changes and asks before modifying external data

## Run locally

1. Install Node.js 22 or newer.
2. Run `npm install`.
3. Copy `.env.example` to `.env.local`.
4. Put a **new private** OpenAI API key in `.env.local`.
5. Run `npm run dev` and open the displayed local address.

```env
OPENAI_API_KEY=your_new_private_key
OPENAI_MODEL=gpt-5.6
```

Never place a key in a source file, upload `.env.local`, or commit it to GitHub. The website works in demo mode without a key.

## How GPT-5.6 and Codex were used

GPT-5.6 powers the natural-language planning layer. It interprets requests, explains scheduling tradeoffs, and proposes safe actions across a user’s day. The server prompt prevents it from claiming external changes and requires approval for consequential actions.

Codex helped shape the product, generate three visual systems, implement the responsive Next.js interface, build the secure server-side OpenAI route, create demo fallbacks, and validate the production artifact.

## Production integrations

The source includes Google OAuth placeholders. A production version should use OAuth for Gmail and Calendar, encrypt tokens, request narrow scopes, provide disconnect/delete controls, and never expose provider tokens in browser code. WhatsApp should be added through an approved Meta integration or user-directed imports.

## Stack

Next.js 16, React 19, TypeScript, Tailwind CSS, Vinext, and the OpenAI Responses API.
