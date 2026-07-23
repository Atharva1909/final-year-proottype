# DevInsight AI

DevInsight AI is a production-style final year project prototype for software engineering intelligence. It combines documentation generation and application log analysis in a simple monolithic architecture.

## Current prototype

- React + TypeScript + Vite dashboard with responsive navigation and interactive module states.
- Spring Boot 3 / Java 21 API foundation with stateless security configuration and PostgreSQL wiring.
- Docker Compose configuration for the API and database.
- Package boundaries are ready for `auth`, `documentation`, `logs`, `history`, and `user` features without introducing microservices.

## Run the dashboard

```bash
npm install
npm run dev
```

## Run the backend stack

```bash
docker compose up --build
```

The API health check is available at `http://localhost:8080/api/health`. Set `GEMINI_API_KEY` in the environment before adding the Gemini integration. The next implementation step is to add JWT issuance, multipart upload handlers, ZIP/log parsing services, and a persisted analysis record.

## Suggested 2-3 month delivery plan

1. Weeks 1-2: authentication, users, projects, and dashboard counts.
2. Weeks 3-5: ZIP extraction, Java source summarization, Gemini report generation, and downloads.
3. Weeks 6-7: log parsing, issue categorization, root-cause prompts, and history.
4. Weeks 8-9: testing, limits, error handling, deployment, and evaluation documentation.