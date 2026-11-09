# ppt-agent

PPT 生成 Agent。仓库是前后端一体：后端 FastAPI，前端 React + Vite。

## 目录

```text
ppt-agent/
├── backend/     # FastAPI（uv 管理依赖）
├── frontend/    # React 19 + TypeScript + Vite 8
└── .gitignore
```

## 环境要求

- [uv](https://docs.astral.sh/uv/)（会使用 Python 3.12，不必改系统里的 `python` 命令）
- Node.js 20.19+（当前前端基于 Node 22 初始化）

## 启动后端

```bash
cd backend
uv run fastapi dev app/main.py
```

- 服务：http://127.0.0.1:8000
- 接口文档：http://127.0.0.1:8000/docs
- 健康检查：`GET /api/health`

后端已允许来自 `http://localhost:5173` 的跨域请求。

## 启动前端

另开一个终端：

```bash
cd frontend
npm install
npm run dev
```

页面默认：http://localhost:5173

## 常用命令

| 位置 | 命令 | 说明 |
|---|---|---|
| `backend/` | `uv add <包>` | 添加 Python 依赖 |
| `backend/` | `uv run fastapi dev app/main.py` | 开发模式启动 API |
| `frontend/` | `npm run dev` | 启动 Vite 开发服务 |
| `frontend/` | `npm run build` | 生产构建 |
| `frontend/` | `npm run lint` | ESLint |
