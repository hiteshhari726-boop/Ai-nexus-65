# NEXUS

NEXUS is a premium personal knowledge intelligence platform that turns scattered AI conversation history into a unified, searchable, interconnected knowledge universe.

## What this repository contains

This repository includes:

- A working FastAPI backend scaffold with auth, import, graph, and AI discovery endpoints.
- A Next.js + Tailwind frontend dashboard and graph UI.
- Database migration SQL for the core tables.
- Environment configuration examples.
- A reference knowledge graph model for conversations, nodes, relationships, and suggestions.

## Stack

- Frontend: Next.js, React, TypeScript, Tailwind CSS, Framer Motion
- Backend: Python, FastAPI, Pydantic
- Database: PostgreSQL + pgvector-ready schema
- Auth: Supabase-ready interface
- AI Providers: OpenAI, Anthropic, Gemini adapters

## Repository structure

```text
.
├── README.md
├── .env.example
├── .gitignore
├── backend/
│   ├── app/
│   ├── requirements.txt
│   └── tests/
├── database/
│   └── migrations/
├── frontend/
│   ├── package.json
│   ├── next.config.mjs
│   ├── postcss.config.js
│   ├── tailwind.config.ts
│   ├── tsconfig.json
│   └── src/
└── docs/
    └── API.md
```

## Quick start

### 1) Backend

```bash
cd backend
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

### 2) Frontend

```bash
cd frontend
npm install
npm run dev
```

### 3) Environment variables

Copy `.env.example` and fill in values for your local environment.

## API basics

Core endpoints are implemented in the FastAPI app:

- `POST /auth/signup`
- `POST /auth/login`
- `POST /imports/upload`
- `GET /graph/overview`
- `POST /graph/search`
- `POST /ai/ask`
- `POST /ai/discover`

## Design direction

The app follows the project requirement for a premium research UI with:

- deep navy background
- subtle gradients
- futuristic node graph canvas
- responsive dashboard
- detailed node sidebar

## Notes

This repository establishes the project architecture and practical working core for the NEXUS vision. It is designed for incremental expansion with real provider adapters, Supabase auth, PostgreSQL migrations, and production-grade graph processing.

## License

MIT
