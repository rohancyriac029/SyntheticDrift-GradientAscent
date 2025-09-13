# AI-Driven Inventory Arbitrage System

Transform retail inventory into a dynamic, self-optimizing profit generator using AI-driven autonomous agents for real-time inventory arbitrage across store locations.

**Live Demo**: [Frontend Deployment](https://thefrontend-neon.vercel.app/)  
**Pitch Deck**: [Presentation Link](https://app.presentations.ai/view/nfGYt4DOur)

---

## Overview

This system leverages autonomous AI agents, real-time analytics, and a self-healing supply chain to identify and execute profitable inventory transfers between store locations. By combining CrewAI orchestration with Gemini’s advanced reasoning models, the system creates an internal AI-powered marketplace for products, driving profitability and efficiency.

---

## Features

- AI Product Agents for continuous monitoring and negotiation  
- Real-time Internal Marketplace for inventory transfers  
- Modern Dashboard for analytics, opportunities, and trade insights  
- Modular AI Architecture with CrewAI and Gemini API  

---

## Architecture

### Agents
- **Inventory Analyst** – Monitors stock levels, identifies over/understock  
- **Arbitrage Specialist** – Finds profitable opportunities, executes trades  
- **Risk Manager** – Evaluates risks, rejects unsafe strategies  

### Components
- `gemini_agent.py` – AI agents with Gemini API integration  
- `crew_orchestrator.py` – CrewAI workflow manager  
- `ai_agent_api.py` – FastAPI service for backend integration  
- `backend/` – Node.js/Express REST API  
- `frontend/` – React/TypeScript dashboard  

---

## Technology Stack

- **Frontend:** React, TypeScript, TailwindCSS  
- **Backend:** Node.js, TypeScript, Express  
- **AI Agents:** Python, CrewAI, Gemini API  
- **Database:** MongoDB Atlas, KeyDB (Redis-compatible)  

---

## Prerequisites

- Node.js 18+  
- Python 3.8+  
- MongoDB Atlas & KeyDB (Redis)  
- Gemini API key → [Get from Google AI Studio](https://makersuite.google.com/app/apikey)  

---

## Getting Started

### 1. Frontend (Dashboard)
```bash
cd frontend
npm install
npm run build
npm start
```

### 2. Backend (API Layer)
```bash
cd backend
npm install
npm run dev
```

### 3. AI Agents (CrewAI + Gemini)
```bash
cd ai-agents
./setup.sh          # Run setup script
source ai-agents-env/bin/activate
python ai_agent_api.py
```

---

## Backend Integration

The backend exposes AI agent endpoints at `/api/v1/ai-agents/`:

```bash
# Get status
curl http://localhost:3001/api/v1/ai-agents/status

# Trigger product analysis
curl -X POST http://localhost:3001/api/v1/ai-agents/analyze   -H "Content-Type: application/json"   -d '{"product_ids": ["PRD-12345", "PRD-67890"]}'

# Run full cycle
curl -X POST http://localhost:3001/api/v1/ai-agents/cycle
```

---

## How It Works

1. **Data Collection** – Inventory & pricing data retrieved from MongoDB/Redis  
2. **AI Analysis** – Gemini models analyze supply-demand imbalances  
3. **Opportunity Identification** – Detect arbitrage & optimization opportunities  
4. **Risk Assessment** – Risk Manager validates safe, profitable actions  
5. **Execution** – Backend executes inventory transfers  
6. **Learning** – Agents adapt based on trade outcomes  

---

## Example Agent Responsibilities

- **Inventory Analyst** → Low/overstock detection, demand forecasting  
- **Arbitrage Specialist** → Price gap detection, profit calculation, execution  
- **Risk Manager** → Policy compliance, exposure tracking, trade approval  

---

## Frontend Dashboard

- Real-time agent activity & status  
- Opportunity detection & profit tracking  
- AI-driven insights & recommendations  
- Trade execution history  


## License

This project is proprietary and intended for research, prototyping, and enterprise innovation.  
