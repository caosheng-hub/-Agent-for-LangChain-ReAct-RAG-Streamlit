# Sweeper ReAct RAG Agent - 扫地机器人智能客服系统

一个基于 **LangChain + ReAct** 架构的智能 Agent 系统，结合 **RAG（检索增强生成）** 和自定义工具链，为扫地/扫拖一体机器人提供专业智能客服能力。

### ✨ 项目亮点（简历重点写这里）

- **ReAct Agent 完整实现**：支持多工具并行调用、动态提示词切换（报告模式 vs 普通模式）
- **RAG 知识库系统**：基于 Chroma + DashScope Embedding，包含 500+ 条扫地机器人专业问答、故障排除、维护保养等知识
- **个性化使用报告生成**：通过外部 CSV 数据 + 中间件动态切换 Prompt，实现用户专属月度报告
- **中间件设计**：实现了工具监控、日志记录、动态 Prompt 切换等高级功能
- **Streamlit 可视化界面**：支持流式输出，交互友好
- **模块化架构**：清晰的 agent / rag / tools / utils 分层设计，便于扩展

### 🛠️ 核心技术栈

- **LLM 框架**：LangChain / LangGraph
- **Agent 架构**：ReAct + Custom Middleware
- **向量数据库**：Chroma
- **嵌入模型**：DashScope (text-embedding-v4)
- **大模型**：Qwen3-Max (Tongyi)
- **前端**：Streamlit
- **其他**：YAML 配置管理、日志系统、MD5 去重、工具装饰器

### 🎯 主要功能

1. **通用咨询**：回答扫地机器人使用、维护、保养、故障排除、选购等问题
2. **天气适配建议**：根据用户实时位置和天气给出针对性保养建议
3. **个性化使用报告**：输入“生成我的使用报告” → 自动获取用户ID、月份、外部数据，生成 Markdown 格式专业报告
4. **知识库检索**：RAG 精准召回专业资料并总结回答

### 🚀 快速启动

```bash
# 1. 克隆仓库
git clone https://github.com/caosheng-hub/sweeper-reAct-rag-agent.git
cd sweeper-reAct-rag-agent

# 2. 安装依赖
pip install -r requirements.txt

# 3. 启动服务
streamlit run app.py
