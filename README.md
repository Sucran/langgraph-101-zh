# LangGraph 101 中文 Notebook（Colab）

本仓库是 [langchain-ai/langgraph-101](https://github.com/langchain-ai/langgraph-101) 的**简体中文翻译版** notebook，方便在 Google Colab / Jupyter 中学习。

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

## Colab 使用提示

1. 点击上表 **在 Colab 中打开** 链接，或将对应 `.zh.ipynb` 从本仓库在 Colab 中打开。
2. **代码单元格保持英文原样**（标识符、字符串、system prompt 未翻译），仅 Markdown 与 `#` 注释为中文。
3. notebook 依赖原仓库的 `utils/`、图片路径与部分环境变量（如 Tavily、模型 API Key）。建议先 clone [langgraph-101](https://github.com/langchain-ai/langgraph-101)，把本中文 notebook 放到对应目录旁，或按需调整 `sys.path` 与图片路径。
4. 输出已清空，需自行运行单元格。

## 原仓库

- <https://github.com/langchain-ai/langgraph-101>
