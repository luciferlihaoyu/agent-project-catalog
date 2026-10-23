# fastapi/fastapi

> 仓库：https://github.com/fastapi/fastapi · ⭐ 103,747（2026-10-23 API 实测） · Python · License: MIT

**一句话：** 高性能 Python API 框架 —— 类型注解直接生成 OpenAPI 文档，Pydantic 校验，异步原生，生产可用。

## 核心能力
- **类型即契约**：`def get_user(user_id: int) -> User:` 一行签名同时产出 **请求校验 + 响应序列化 + OpenAPI/Swagger 文档 + IDE 补全**
- **Pydantic v2 驱动**：数据模型即校验层，`Field` 约束、validator、序列化别名开箱即用
- **原生 async**：基于 Starlette + Uvicorn/uvloop，ASGI 标准，不阻塞事件循环
- **自动文档**：内置 Swagger UI（/docs）与 ReDoc（/redoc），零配置
- **依赖注入**：`Depends()` 声明式依赖（数据库连接、鉴权、分页），可嵌套可覆盖
- **WebSocket / SSE / 流式响应**：`StreamingResponse`、`yield` 依赖做长连接
- **ORM 无关**：SQLModel / SQLAlchemy / Tortoise 都能接，不绑架你的数据层
- **中间件生态**：CORS、GZip、限流、鉴权（OAuth2/JWT）都有官方或成熟三方实现

## 关键数据（2026-10-23 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 103,747 |
| 🍴 Forks | 10,087 |
| Open Issues | 57 |
| Watchers | 777 |
| 创建时间 | 2018-12-08 |
| 最后推送 | 2026-10-22T22:21:50Z |
| 主页 | https://fastapi.tiangolo.com/ |
| Topics | api, async, asyncio, openapi, openapi3, pydantic, python, python-types, rest, starlette, swagger, uvicorn, web |

## 适用场景
- AI 应用后端（OpenAI 兼容接口、LLM 网关、Agent 编排服务）
- 内部微服务 / BFF 层（前后端分离的 API 网关）
- 数据校验严格的对外 API（金融、医疗、政企）——类型即契约的价值最大场景
- 需要自动出 API 文档的交付型项目

## 为什么值得关注
- **Open Issues 仅 57、Stars 破 10 万**：这个比例极其罕见 —— 说明 issue 区干净、维护响应及时，是"成熟但不官僚"的库。
- **它是 LLM 应用后端的事实标准之一**：Tiangiang、vLLM、ComfyUI、各类 Agent 框架的 HTTP 层大量基于 FastAPI 生态（Starlette/uvicorn/Pydantic）。想理解 AI 基建怎么"被调用"，读它的中间件栈比读文档快。
- **类型注解的双赢设计**：把"写类型"从可选的成本变成免费的收益（文档 + 校验 + 补全三合一），这是少数能同时讨好前端、后端和 AI 辅助工具的设计。
- **MIT 协议 + 极低的依赖数**：没有 license 陷阱，没有重型依赖，嵌入商业系统无后顾之忧。

## 参考资料
1. [GitHub 仓库](https://github.com/fastapi/fastapi)
2. [官方文档](https://fastapi.tiangolo.com/)
3. [FastAPI 教程（中文）](https://fastapi.tiangolo.com/zh/tutorial/)
