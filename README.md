# Critique AI

**Critique AI** is an intelligent answer evaluation tool designed for students. It offers instant grading, feedback, note generation, roadmap creation, and multi-file summarization — all powered by Gemini AI and Supabase.

## Demo

[Visit Critique AI →](https://critiqueai00.vercel.app)

## Project Structure

```
critiqueai/
├── frontend/    # React (Vite) app
├── backend/     # Flask API server
└── README.md
```

## Features

- **Instant Grading** — Upload answers and receive quick scores, feedback, and improvement tips.
- **Note Generation** — Create clear, structured notes from any content.
- **Roadmap Creation** — Enter a topic and get a complete learning roadmap.
- **Multi-File Summarization** — Supports PDF, DOCX, TXT, JPG, PNG, and JPEG.
- **Deep File Analysis** — Custom Python engine extracts text, images, and tables from PDFs.
- **Secure & Clean Workflow** — Built on Supabase for auth, database, and storage.

## Quick Start

### Local Development

**Frontend:**
```bash
cd frontend
npm install
npm run dev
```

**Backend (using uv):**

Install uv if you don't have it:
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Set up and run the backend:
```bash
cd backend
uv sync
uv run python app.py
```

### Environment Variables

**Frontend (`frontend/.env`)**

| Variable | Description |
|---|---|
| `VITE_API_URL` | Backend API URL |
| `VITE_SUPABASE_URL` | Supabase project URL |
| `VITE_SUPABASE_ANON_KEY` | Supabase anonymous key |

**Backend (`backend/.env`)**

| Variable | Description |
|---|---|
| `GEN_API2` | Google Generative AI API key |
| `SUPABASE_URL` | Supabase project URL |
| `SUPABASE_SERVICE_KEY` | Supabase service_role key |
| `CORS_ORIGINS` | Comma-separated allowed origins |

## Supported File Formats

`.pdf`, `.docx`, `.txt`, `.jpg`, `.jpeg`, `.png`

## License

MIT
