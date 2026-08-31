# A 股虚拟炒股平台（MVP）

一个可本地运行、可继续扩展的虚拟炒股系统，支持 A 股模拟行情与交易，不连接真实券商账户。

## Features

- 用户注册/登录（JWT）
- 自动初始化 100 万虚拟资金（可配置）
- 股票搜索、行情查看、历史价格
- 市价买入/卖出
- T+1 限制
- 手续费计算
- 持仓、订单、成交、资产曲线、排行榜
- Docker Compose 一键启动
- GitHub Actions CI

## Tech Stack

- Backend: FastAPI, SQLAlchemy 2.x, Pydantic v2, Alembic, pytest
- Frontend: React, TypeScript, Vite, React Router, TanStack Query, Axios, Recharts, Tailwind CSS
- DB: SQLite (dev), PostgreSQL (prod)

## Quick Start

```bash
cp .env.example .env
docker compose up --build
```

- Frontend: http://localhost:5173
- Backend: http://localhost:8000
- Swagger: http://localhost:8000/docs

## Local Dev

Backend:
```bash
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload
```

Frontend:
```bash
cd frontend
npm install
npm run dev
```

## Environment Variables

见 `.env.example`。

## Testing

```bash
cd backend && pytest
cd frontend && npm run build
```

## Project Structure

- `/backend` 后端服务
- `/frontend` 前端应用
- `/docs` 文档
- `docker-compose.yml` 本地编排

## Roadmap

- V1.1 限价单与撤单
- V1.2 完整交易日历
- V1.3 模拟比赛与好友系统
- V1.5 对比沪深300
- V2 策略回测与 AI 研究助手（仅研究，不自动实盘）

## Screenshots

- TODO

## Disclaimer

本平台仅用于学习、研究和模拟交易，不构成任何投资建议，不连接真实证券账户。
