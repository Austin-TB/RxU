# RxU Platform

A full-stack application for drug research, sentiment analysis, and recommendations. Powered by FastAPI (backend) and React + TypeScript (frontend).

---

## Quick Start

### Backend

1. **Setup**
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   cp .env.example .env  # Configure environment variables
   python run.py
   ```
   API available at `http://localhost:8080`

2. **Docker**
   ```bash
   docker build -t rxu-backend .
   docker run -p 8080:8080 --env-file .env rxu-backend
   ```

### Frontend

1. **Setup**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```
   App available at `http://localhost:5173`

---

## Architecture

```
RxU copy/
├── backend/
│   ├── app/
│   │   ├── main.py              # FastAPI app & routes
│   │   ├── config.py            # Pydantic config
│   │   ├── api/                 # API route modules
│   │   ├── services/            # Business logic
│   │   └── utils/               # Utility functions
│   ├── data/                    # Drug & sentiment data
│   ├── requirements.txt
│   ├── Dockerfile
│   └── run.py
├── frontend/
│   ├── src/
│   │   ├── components/          # React components
│   │   ├── data/                # Static data
│   │   ├── types/               # TypeScript types
│   │   ├── App.tsx              # Main app
│   │   └── main.tsx             # Entry point
│   ├── public/
│   ├── package.json
│   └── vite.config.ts
└── README.md
```

---

## Features

- **Drug Search**: Autocomplete, fuzzy search, relevance scoring
- **Sentiment Analysis**: Interactive charts, historical trends, community insights
- **Drug Information**: Detailed profiles, recommendations, side effects
- **Responsive UI**: Mobile-first, accessible, modern design

---

## API Integration

- **Backend**: FastAPI, CORS enabled, RESTful endpoints
- **Frontend**: React hooks for API calls, error handling, loading states

---

## API Endpoints

- `/api/drugs/search?q=...` — Drug search
- `/api/drugs/sentiment?drug_name=...` — Sentiment analysis
- `/api/drugs/recommend?drug_name=...` — Recommendations
- `/api/drugs/side-effects?drug_name=...` — Side effects
- `/health` — Health check

---

## Development

- **Backend**: Python 3.11+, FastAPI, Pandas, AWS S3 integration
- **Frontend**: React 19+, TypeScript, Vite, Recharts
- **Testing**: Run backend service tests with `python -m app.services.drug_search`
- **Linting**: `flake8 app/`, `black app/`, `mypy app/`

---

## Deployment

- **Docker**: Containerized backend
- **Cloud Run**: Google Cloud deployment supported

---

## Contributing

- Fork, branch, commit, and PR
- Follow PEP 8 (backend) and ESLint (frontend)
- Add type hints and docstrings
- Write tests for new features

---

## License

MIT License

---

## Support

Open an issue or contact the author for help.