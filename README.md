# LangGraph 101 中文 Notebook（Colab）

本仓库是 [langchain-ai/langgraph-101](https://github.com/langchain-ai/langgraph-101) 的**简体中文翻译版** notebook，方便在 Google Colab / Jupyter 中学习。

`utils/` 与 `images/` 自上游 [langgraph-101](https://github.com/langchain-ai/langgraph-101) 同步 vendoring，便于在 Colab 中独立运行（见下方说明）。

## 内容

| 文件 | 主题 | 在 Colab 中打开 |
|------|------|-----------------|
| `notebooks/101/101_langchain_langgraph.zh.ipynb` | LangChain / LangGraph 入门：模型、消息、工具、`create_agent`、记忆、流式、手写 ReAct | [打开](https://colab.research.google.com/github/Sucran/langgraph-101-zh/blob/main/notebooks/101/101_langchain_langgraph.zh.ipynb) |
| `notebooks/101/102_middleware.zh.ipynb` | 人机协同（HITL / interrupt）与中间件（middleware） | [打开](https://colab.research.google.com/github/Sucran/langgraph-101-zh/blob/main/notebooks/101/102_middleware.zh.ipynb) |
| `notebooks/201/deep_agents.zh.ipynb` | Deep Agents：驾驭层、后端、子智能体、HITL、长期记忆、AGENTS.md / Skills | [打开](https://colab.research.google.com/github/Sucran/langgraph-101-zh/blob/main/notebooks/201/deep_agents.zh.ipynb) |
| `notebooks/201/deep_agents_extra.zh.ipynb` | Deep Agents 进阶：拆解实现、自定义文件系统 / task、StateGraph 子智能体、MCP、沙箱 | [打开](https://colab.research.google.com/github/Sucran/langgraph-101-zh/blob/main/notebooks/201/deep_agents_extra.zh.ipynb) |

## 建议学习顺序

1. `101_langchain_langgraph.zh.ipynb`
2. `102_middleware.zh.ipynb`
3. `deep_agents.zh.ipynb`
4. `deep_agents_extra.zh.ipynb`

## 在 Google Colab 中运行

从 GitHub 打开 Colab 链接时，Google 通常**只下载单个 `.ipynb` 文件**，不会带上同仓库的 `utils/`。每个 notebook 在「环境准备」部分都有 **Colab 一键环境** 代码单元格，请按顺序操作：

1. 点击上表中的 **在 Colab 中打开**（或上传 / 打开对应 `.zh.ipynb`）。
2. **先运行「Colab 一键环境」单元格**（在导入 `utils` 之前）：
   - 安装所需 Python 包（101：`langchain`、`langchain-anthropic`、`langchain-openai`、`python-dotenv`；Deep Agents 另需 `deepagents`、`tavily-python`）。
   - 在 Colab 中若检测不到 `utils/`，会浅克隆本仓库到 `/content/langgraph-101-zh` 并把仓库根目录加入 `sys.path`。
3. **设置 API Key**（不要写在 notebook 里提交到 Git）：
   - **推荐**：Colab 左侧 **密钥**（🔑）→ 添加 `ANTHROPIC_API_KEY` 和/或 `OPENAI_API_KEY`。
   - 或在运行时：`import os; os.environ["ANTHROPIC_API_KEY"] = "..."`。
   - Deep Agents 还需 `TAVILY_API_KEY`（[Tavily](https://tavily.com)）。
4. 运行后续单元格。默认 LLM 在 `utils/models.py` 中配置为 **Anthropic `claude-haiku-4-5`**；换供应商请改该文件（与上游说明一致）。

本地完整 clone 本仓库时，可在项目根目录用 Jupyter 打开 notebook；仍建议先运行一键环境单元格（或自行 `pip install`），路径逻辑同时支持本地与 Colab。

## 本地开发

```bash
git clone https://github.com/Sucran/langgraph-101-zh.git
cd langgraph-101-zh
pip install --pre -U langchain langchain-anthropic langchain-openai python-dotenv
# Deep Agents notebooks 另需：pip install deepagents tavily-python
export ANTHROPIC_API_KEY=...
jupyter notebook notebooks/101/101_langchain_langgraph.zh.ipynb
```

## 其他说明

- **代码单元格保持英文原样**（标识符、字符串、system prompt 未翻译），仅 Markdown 与 `#` 注释为中文。
- 输出已清空，需自行运行单元格。

## 原仓库

- <https://github.com/langchain-ai/langgraph-101>
