# 📈 Real-Time Stock & IPO Price Prediction Platform

A full-stack machine learning platform for real-time stock price prediction, historical analysis, and IPO tracking.

## 🏗️ Architecture

```
┌─────────────┐     ┌─────────────┐     ┌──────────────┐
│   React +   │────▶│   FastAPI   │────▶│  PostgreSQL  │
│   Vite UI   │◀────│   Backend   │◀────│   Database   │
└─────────────┘     └──────┬──────┘     └──────────────┘
                           │
                    ┌──────▼──────┐
                    │  ML Engine  │
                    │ Random Forest│
                    └─────────────┘
```

## 🚀 Tech Stack

| Layer       | Technology                        |
|-------------|-----------------------------------|
| Frontend    | React, Vite, Tailwind CSS, Recharts |
| Backend     | Python, FastAPI, SQLAlchemy        |
| ML/AI       | Scikit-learn, Pandas, NumPy       |
| Database    | PostgreSQL                        |
| DevOps      | Docker, Docker Compose, Jenkins   |
| Monitoring  | Prometheus, Grafana               |
| VCS         | GitHub                            |

## 📁 Project Structure

```
real-time-stock-predictor/
├── frontend/                # React + Vite frontend
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   ├── pages/           # Page-level components
│   │   ├── services/        # API integration
│   │   ├── hooks/           # Custom React hooks
│   │   └── utils/           # Utility functions
│   ├── Dockerfile
│   └── package.json
├── backend/                 # FastAPI backend
│   ├── app/
│   │   ├── api/routes/      # API endpoints
│   │   ├── core/            # Config & database
│   │   ├── models/          # SQLAlchemy models
│   │   ├── schemas/         # Pydantic schemas
│   │   ├── services/        # Business logic
│   │   └── ml/              # ML model code
│   ├── Dockerfile
│   └── requirements.txt
├── ml/                      # ML workspace
│   ├── notebooks/           # Jupyter notebooks
│   ├── data/                # Training data
│   └── models/              # Saved models
├── devops/                  # DevOps configs
│   ├── jenkins/             # Jenkins pipeline
│   ├── prometheus/          # Prometheus config
│   └── grafana/             # Grafana dashboards
├── docker-compose.yml
└── README.md
```

## 🛠️ Getting Started

### Prerequisites
- Node.js 18+
- Python 3.11+
- Docker & Docker Compose
- PostgreSQL (or use Docker)

### Run Frontend (Development)
```bash
cd frontend
npm install
npm run dev
```
Frontend runs at: http://localhost:3000

### Run Backend (Development)
```bash
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```
Backend runs at: http://localhost:8000
API docs at: http://localhost:8000/api/docs

### Run with Docker Compose
```bash
docker-compose up --build
```

## 📡 API Endpoints

| Method | Endpoint                        | Description              |
|--------|--------------------------------|---------------------------|
| GET    | `/api/health`                  | Health check              |
| GET    | `/api/stocks`                  | List all stocks           |
| GET    | `/api/stocks/{symbol}`         | Get stock details         |
| GET    | `/api/stocks/{symbol}/history` | Get price history         |
| GET    | `/api/predictions`             | Get all predictions       |
| POST   | `/api/predictions/{symbol}`    | Generate prediction       |
| GET    | `/api/predictions/{symbol}/history` | Prediction history   |
| GET    | `/api/ipo`                     | List IPOs                 |
| GET    | `/api/ipo/{id}`                | Get IPO details           |
| GET    | `/metrics`                     | Prometheus metrics        |

## 🔬 ML Model

- **Algorithm**: Random Forest (Regressor + Classifier)
- **Features**: Moving averages, RSI, volatility, volume ratios
- **Predictions**: Next-day price & UP/DOWN direction
- **Confidence**: Probability-based confidence score

## 📊 Monitoring

- **Prometheus**: http://localhost:9090
- **Grafana**: http://localhost:3001 (admin/admin)

## 👥 Authors

College DevOps + ML Project

## 📄 License

MIT
