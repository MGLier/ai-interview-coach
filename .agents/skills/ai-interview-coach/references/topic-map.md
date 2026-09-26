# 技术面试范围与关键区分

按本轮主题读取对应章节。这里定义覆盖面和高价值追问，不是固定题库。

## RAG

覆盖数据清洗、Chunk、Embedding、Dense/Sparse Retrieval、BM25、Hybrid Search、向量数据库与索引、距离度量、TopK、Reranker、Query Rewrite、Prompt、幻觉、检索评估、端到端回答质量、多轮对话和可观测性。

优先验证：切分和召回的耦合；稠密与稀疏检索的互补性；索引、距离度量和归一化的关系；TopK 与延迟、噪声的权衡；召回与排序的职责边界；评估集如何构造；检索指标与回答质量为何不能混为一谈。

## Agent 与协议

覆盖 Agent、Tool Calling、Function Calling、ReAct、Planning、Memory、State、Workflow、Human-in-the-loop、Retry、Timeout、Permission、Safety、Multi-Agent、MCP 和 A2A。

重点区分：

- Agent vs Workflow：动态决策与确定性编排、可控性、可测试性、成本和失败边界。
- Agent vs 普通接口：模型参与决策和参数生成，不代表所有后端逻辑都应 Agent 化。
- Memory vs State：跨轮信息与一次执行状态的职责边界。
- MCP vs Function Calling：连接工具或资源的协议层，与模型表达工具意图的机制不是同一层。
- A2A vs MCP：Agent 间协作与 Agent 连接工具或上下文的关注点不同。

## LangChain

覆盖 Model、Prompt、Output Parser、Runnable、LCEL、Chain、Retriever、Tool、Agent、Memory、Callback、Streaming、顺序与并行组合。

重点围绕真实用法、可组合性、流式链路、回调与观测、异常传播和并发。若答案依赖具体版本，让候选人说明版本语境。

## LangGraph

覆盖 State、StateGraph、Node、Edge、Conditional Edge、Reducer、Checkpoint、Memory、Interrupt、Human-in-the-loop、Loop、Persistence、Agent Workflow 和 Multi-Agent。

优先追问：为什么普通 Chain 不够；State Schema 与更新合并；条件分支；循环与最大步数；Checkpoint 与恢复；Interrupt 前后的持久化；节点幂等和副作用隔离。

## Transformer 与 BERT

覆盖 Encoder/Decoder、Self-Attention、Q/K/V、缩放点积注意力、Multi-Head Attention、Position Encoding、Residual、LayerNorm、FFN、BERT、Mask、MLM、CLS、文本分类、Fine-tuning 和 LoRA。

验证每个设计解决什么问题、与 RNN 的差别、训练与推理代价，以及如何落到文本分类项目。警惕把 BERT 说成 Decoder，或混淆双向注意力与因果 Mask。

## NLP 与分类工程

覆盖 FastText、BERT、数据与标签设计、训练、Loss、Accuracy/Precision/Recall/F1、类别不平衡、阈值、误报漏报成本、去重聚合、上线、漂移和更新。

要求候选人说明模型升级的业务原因、对照实验和成本权衡，而不是笼统说“效果更好”。

## 机器学习、深度学习与时间序列

覆盖监督学习、数据泄漏、偏差与方差、过拟合、正则化、Dropout、Early Stopping、RNN/LSTM、时间窗口、缺失与异常处理、缩放、时间划分、MSE/MAE/RMSE、单步、多步与滚动预测。

重点验证：时间序列为何不能普通随机划分；缩放器为何只能在训练集拟合；多步预测的误差累积；简单基线对照；训练与推理时的特征可用性必须一致。

## Python、FastAPI 与工程化

结合项目追问类型提示、异步 I/O、并发与阻塞、依赖注入、参数校验、异常处理、SSE 断连与背压、超时重试、日志指标与追踪、配置与密钥、连接生命周期、限流、缓存、降级、测试、部署、版本管理和回滚。

工程化问题应要求候选人说明故障边界和可观测证据，不把“用了异步”自动等同于性能更好。
