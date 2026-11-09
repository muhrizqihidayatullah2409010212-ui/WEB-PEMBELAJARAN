# tahap perbaikan website pembelajaran

## 🏗️ Architecture

```
┌─────────────┐     HTTP/WS     ┌──────────────┐     SQL/Storage    ┌───────────┐
│   Frontend   │ ◄─────────────► │   Backend    │ ◄────────────────► │  Supabase │
│   (Next.js)  │                 │   (FastAPI)  │                    │ (Postgres │
│   Vercel     │                 │   Railway    │                    │ + Storage)│
└─────────────┘                  └──────────────┘                    └───────────┘
```

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Next.js, TypeScript, Tailwind CSS, Framer Motion |
| Backend | FastAPI (Python) |
| Database | Supabase PostgreSQL |
| Realtime | Supabase Realtime + WebSocket |
| QR Code | `qrcode` (Python), `html5-qrcode` (JS) |
| Storage | Supabase Storage |

## 📁 Project Structure

```
smart-parking-umsu/
├── backend/              # FastAPI backend
│   ├── app/
│   │   ├── core/         # Security, logging, exceptions
│   │   ├── models/       # Pydantic schemas
│   │   ├── routers/      # API endpoints
│   │   ├── services/     # Business logic
│   │   └── utils/        # Helpers
│   ├── Dockerfile
│   └── requirements.txt
├── frontend/             # Next.js frontend (Phase 3)
├── docker-compose.yml
└── README.md
```

## 🚀 Quick Start

### Prerequisites

- Python 3.11+
- Node.js 18+ (Phase 3)
- Supabase account

### 1. Setup Database

1. Create a new Supabase project
2. Open SQL Editor
3. Copy and paste `database/schema.sql`
4. Execute

### 2. Setup Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
# Edit .env with your Supabase credentials
uvicorn app.main:app --reload --port 8000
```

### 3. API Documentation

Once the backend is running, visit:
- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

> ⚠️ **Change the admin password immediately after first login.**

## 📄 License

This project is developed for academic purposes at UMSU.
