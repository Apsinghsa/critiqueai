# Critique AI

**Critique AI** is an intelligent answer evaluation tool designed for students. It offers instant grading, feedback, note generation, roadmap creation, and multi-file summarization — all powered by Gemini AI and Supabase.

## Project Link

[Visit Critique AI →](https://critiqueai.dev)

## Project Structure

```
critiqueai/
├── frontend/    # React (Vite) app
├── backend/     # Flask API server
├── docker-compose.yml
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

### Using Docker (recommended)

```bash
docker-compose up --build
```

- Frontend: http://localhost:3000
- Backend: http://localhost:8000

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

## Environment Variables

### Frontend (`frontend/.env`)

| Variable | Description |
|---|---|
| `VITE_API_URL` | Backend API URL (default: `http://localhost:8000`) |
| `VITE_SUPABASE_URL` | Supabase project URL |
| `VITE_SUPABASE_ANON_KEY` | Supabase anonymous/public key |

### Backend (`backend/.env`)

| Variable | Description |
|---|---|
| `GEN_API2` | Google Generative AI API key |
| `SUPABASE_URL` | Supabase project URL |
| `SUPABASE_SERVICE_KEY` | Supabase service_role key (NOT anon key) |

## Supported File Formats

`.pdf`, `.docx`, `.txt`, `.jpg`, `.jpeg`, `.png`

## How It Works

1. Users provide text or upload files.
2. Text is sent to Gemini for processing.
3. Uploaded files are temporarily stored in Supabase Storage.
4. File data is extracted (text, images, tables) using the custom Python engine.
5. Extracted content is passed to Gemini AI for summarization, evaluation, or note-making.
6. Output is shown to the user instantly.
7. Uploaded files are auto-deleted after processing.

## Custom PDF Handler

A custom Python function extracts text, images, and tables from PDFs page-by-page, describes images using Gemini, and formats everything into structured content for AI processing.

## License

MIT
