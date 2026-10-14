# bass-tab-ai

BassTab AI — local-first open-source app to create, transcribe and export electric bass tablature from audio (MP3/WAV/M4A).

## Repository layout

- `apps/web` — Next.js frontend
- `services/api` — FastAPI API
- `services/worker` — transcription/processing worker
- `packages/schemas` — shared schemas/events
- `tests` — unit/integration tests
- `docs` — architecture and deployment notes

## Requirements

- Ubuntu 22.04+ recommended
- Docker Engine + Docker Compose
- Node.js 20+
- Python 3.11+
- FFmpeg installed and available on PATH

## Quick start

```bash
make dev
```

Then open:
- Frontend: http://localhost:3000
- API: http://localhost:8000/health

## Useful commands

```bash
docker compose up --build
make dev
make test
make lint
```

## Environment variables

Copy `.env.example` to `.env` and adjust the values as needed.

```bash
cp .env.example .env
```

Example values:

```dotenv
APP_ENV=development
API_HOST=0.0.0.0
API_PORT=8000
WEB_PORT=3000
WORKER_WORKDIR=/workspace
FFMPEG_PATH=ffmpeg
```

## Notes

This repository is intentionally scaffolded to support the MVP backlog described in `BassTab_AI_BACKLOG.md` and to be ready for incremental implementation of the user stories.
