---
title: "Week #6"
---

# **Week #6**

## Links

*Specify here all the necessary links to your website, application installer, final demo, etc.*

- **Deployment**: [http://89.223.121.67:3000/](http://89.223.121.67:3000/).
- **API Docs**: [Endpoints URL](http://89.223.121.67:8000/), [main.py](https://github.com/IU-Capstone-Project-2025/Metalytics/blob/main/backend/main.py).
- **Design**: [Figma design](https://www.figma.com/design/oqrwNbnmT7rRQNl58pdCmO/Metalytics).
- **Demo**: [Link to demo](http://89.223.121.67:3000/)
- **Github repository**: [Metalytics repository](https://github.com/IU-Capstone-Project-2025/Metalytics).

## Final deliverables

## Project Overview

**Metalytics** an analytical system for forecasting the prices of specific metals traded on the Russian financial market using machine learning. The system addresses the challenge of predicting volatile metal markets by combining models with real-time news analysis.

**Problems Solved:**
- Price volatility prediction in metal markets
- Data consolidation from multiple sources
- Real-time market intelligence integration

**Key Implemented Features:**
- LSTM and baseline ML models for Gold and Silver
- Real-time news parsing from financial sources
- Responsive web interface with interactive charts
- PostgreSQL database with RESTful API backend

## Features

**Implemented Features:**
- **Price Prediction**: Short-term forecasting for Gold and Silver using LSTM and baseline models
- **Real-time News Feed**: Automated parsing from metalinfo.ru with source links
- **Interactive Charts**: Dynamic price visualization with zoom/pan capabilities
- **Responsive Design**: Adaptive interface for desktop and mobile devices
- **Database Integration**: PostgreSQL with automated data updates
- **RESTful API**: FastAPI backend for data delivery
- **Docker Deployment**: Containerized application for easy setup

### Tech stack

**Backend & API:**
- FastAPI (Python web framework)
- PostgreSQL (Database)
- Uvicorn (ASGI server)
- psycopg2 (PostgreSQL adapter)

**Machine Learning:**
- TensorFlow/Keras (LSTM neural networks)
- Scikit-learn (Baseline models)
- XGBoost (Gradient boosting)
- Pandas & NumPy (Data processing)
- TA (Technical indicators)
- Joblib (Model serialization)

**Frontend:**
- HTML5, CSS3, JavaScript (Vanilla)
- Chart.js (Interactive charts)
- Swiper.js (News carousel)

**Infrastructure:**
- Docker & Docker Compose (Containerization)
- YFinance (Market data API)
- Python-dotenv (Environment management) 

### Setup instructions

Follow the steps below to run the project locally using Docker or manually.

### ⚙️ Prerequisites

- [Docker](https://www.docker.com/products/docker-desktop) installed and running
- [PostgreSQL](https://www.postgresql.org/) installed.
- Python 3.10+
- (Optional) Live server if running without Docker

### 📥 Step 1 — Clone the Repository

In your terminal:

```bash
git clone https://github.com/IU-Capstone-Project-2025/Metalytics.git
cd Metalytics
```

### 💻 Step 2 — Run with Docker (Recommended)

```bash
docker-compose up --build
```
This will:
- Start the **FastAPI backend** at [http://localhost:8000](http://localhost:8000)
- Start the **Frontend** at [http://localhost:3000](http://localhost:3000)

#### 📋 Managing the Container

To view logs from the running container:
```bash
docker compose logs -f
```

To stop the container without removing it:
```bash
docker compose stop
```

To stop and remove the container:
```bash
docker compose down
```

To rebuild the image after making changes to the code:
```bash
docker compose up -d --build
```

### 🛠 Alternative — Run Manually (Without Docker)
- Clone the repository (follow step 1).
- Make sure you are in the project root folder.
- Follow the steps bellow.

#### ▶️ Backend (FastAPI)
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```
#### 🌐 Frontend
Open frontend/index.html directly in your browser or use a local server (ex. "Live Server" in VS Code)

---


## Presentation draft

*Add here a link to the presentation draft.*

# Weekly commitments

## Individual contribution of each participant

*...*

## Plan for Next Week

*...*

## Confirmation of the code's operability

We confirm that the code in the main branch:
- [ ] In working condition.
- [ ] Run via docker-compose (or another alternative described in the `README.md`).
