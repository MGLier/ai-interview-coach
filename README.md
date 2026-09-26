# ai-interview-coach

面向 2～5 年经验 AI 应用算法工程师的中文技术面试训练 Skill。它可以模拟真实技术面试，围绕 RAG、Agent、LangChain、LangGraph、LLM 应用、NLP、Transformer/BERT、机器学习、深度学习、时间序列、Python、FastAPI 与 AI 系统工程化进行单题提问、动态追问、回答点评和口语化优化。

## 特点

- 一次只问一道主要问题，根据回答继续追问
- 支持综合面试、项目面、专题面、压力面和八股模式
- 区分项目事实与通用技术原理，不替用户编造项目数据或指标
- 可通过 `knowledge/` 添加自己的项目资料、复盘笔记和技术笔记
- 默认按主题按需加载资料，避免一次读入整个知识库

## 仓库结构

```text
ai-interview-coach/
├── .agents/
│   └── skills/
│       └── ai-interview-coach/
│           ├── SKILL.md
│           ├── agents/
│           │   └── openai.yaml
│           ├── knowledge/
│           │   └── README.md
│           └── references/
│               ├── project-templates.md
│               └── topic-map.md
├── .gitignore
├── LICENSE
└── README.md
```

## 安装

### 在某个项目中使用

克隆仓库，然后用 Codex 打开仓库根目录：

```bash
git clone https://github.com/<你的用户名>/ai-interview-coach.git
cd ai-interview-coach
```

Codex 会从 `.agents/skills/ai-interview-coach/` 发现这个 Skill。

如果要把它加入已有项目，将下列目录完整复制到目标项目的同名位置：

```text
.agents/skills/ai-interview-coach/
```

### 作为个人 Skill 使用

将 `.agents/skills/ai-interview-coach/` 整个目录复制到个人 Skill 目录。常见位置为：

```text
~/.agents/skills/ai-interview-coach/
```

重新打开 Codex 会话后即可使用。

## 使用示例

```text
使用 ai-interview-coach，开始面试。
```

```text
使用 ai-interview-coach，进行 RAG 面试。一次只问一道题，不要提前给答案。
```

```text
使用 ai-interview-coach，进行 Agent 项目压力面，按 3 年经验控制难度。
```

```text
使用 ai-interview-coach，看看我的回答：
（粘贴你的回答）
```

也可以直接说“项目面”“LangGraph 面试”“算法基础面试”“给标准回答”或“优化我的回答”。

## 新增知识库

把 Markdown 文件放入：

```text
.agents/skills/ai-interview-coach/knowledge/
```

建议按主题或项目拆分，例如：

```text
knowledge/
├── rag.md
├── agent.md
├── langgraph.md
├── my-rag-project.md
└── interview-notes.md
```

每份项目资料建议包含：已确认事实、本人负责部分、真实技术栈、关键选择及原因、遇到的问题与处理、已验证效果，以及仍待补充的内容。具体模板见 [`knowledge/README.md`](.agents/skills/ai-interview-coach/knowledge/README.md)。

## 隐私与公开分享

本仓库只包含通用面试规则、公开技术主题和可替换的项目模板，不包含任何用户的真实业务指标、客户信息、公司内部架构、密钥或私有项目资料。

公开提交前，请检查 `knowledge/` 中是否含有：

- 客户、公司、人员或系统的真实名称
- 内网地址、账号、令牌、密钥或连接信息
- 未公开的数据规模、性能指标、业务收益或故障记录
- 受保密协议约束的架构、代码、截图或文档

个人知识库可放在仓库外，或使用 `.gitignore` 中提供的 `knowledge/private/` 目录。

## License

[MIT](LICENSE)
