# 大语言模型局限性
- **幻觉**: 模型可能会生成虚假信息，与现实严重不符。
- **时效性**: 模型训练数据过时，无法反映最新趋势。
- **可靠性**: 面对复杂任务时可能频发错误输出。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent01.png)

# 智能体定义
- **感知**: 感知环境中的动态条件。
- **行动**: 采取行动影响环境中的条件。
- **推理**: 运用推理能力理解信息、解决问题、产生推断、决定行动。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent02.png)

# 智能体组成
- **大脑**: 控制器，负责记忆、思考和决策。
- **感知**: 对外部环境的多模态信息进行感知和处理。
- **动作**: 利用并执行工具以影响环境。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent03.png)

# 智能体范式
- **AutoGPT**: 包含内存、上下文、任务创建、执行、队列管理。
- **ReWoo**: 包含计划拆分、执行工具、结束条件。
- **ReAct**: 包含输入、选择工具、执行工具、结束条件。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent04.png)


# AutoGPT 示例
- **Memory**: 存储任务/结果对。
- **Context**: 查询记忆以获取上下文。
- **TaskCreationAgent**: 创建任务。
- **ExecutionAgent**: 执行任务。
- **TaskQueue**: 管理任务队列。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent05.png)

# ReWoo Planner Worker 示例
- **Context prompt**: 为以下任务提供示例和计划。
- **Exemplars**: 例如，维基百科上的“Hennchata”词条。
- **Plan**: 搜索关于“The Hennchata”的更多信息。
- **Evidence**: Hennessy cognac是“The Hennchata”的主要成分。
- **DAG Solver**: 解决任务给定提供的计划和证据。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent06.png)

# ReAct (Reason + Act) 示例
- **输入**: Hotspot QA问题，例如询问特定酒店的房间数。
- **Thought**: 需要搜索Cirque du Soleil show Mystere所在的酒店及其房间数。
- **Act**: 搜索Cirque du Soleil show Mystere，然后搜索Treasure Island Hotel and Casino。
- **Obs**: 观察到的信息，如Cirque du Soleil是一个加拿大娱乐公司。
- **结束**: 提供了酒店房间数的答案。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent07.png)

# Lagent 框架
- **Agent**: 一个轻量级开源智能体框架。
- **支持**: 多种智能体范式（如AutoGPT、ReWoo、ReAct）。
- **工具**: 支持多种工具（如谷歌搜索、Python解释器等）。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent08.png)

# AgentLego 工具包
- **多模态**: 提供视觉、语音等多个领域的前沿算法。
- **支持**: 多个智能体框架（如Lagent、LangChain、TransformersAgents）。
- **工具集**: 包括目标检测、图像分割、姿态估计等。
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent09.png)

# 作业

## Lagent 

![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent10.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent11.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent12.png)

## AgentLego

![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent13.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent14.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent15.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent16.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/agent17.png)
*感觉什么地方有问题，没有正确检测内容*