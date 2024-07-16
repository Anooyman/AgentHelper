
# 大模型部署面临的挑战

## 计算量巨大
- 20B模型生成1个token需要约406亿次浮点运算。
- 以NVIDIA A100为例，单张理论FP16运算性能为每秒77.97TFLOPs。

## 访存瓶颈
- 大模型推理是“访存密集”型任务，存在严重的访存性能瓶颈。
- RTX4090在推理175B大模型时，显存带宽需求是其处理能力的30倍。

## 内存开销巨大
- 20B模型仅加载参数就需要超过40GB显存，175B模型需要350GB+。
- 消费级显卡如NVIDIA RTX 4060显存仅有8GB，而NVIDIA A100显存为80GB。

## 模型剪枝 (Pruning)
- 非结构化剪枝：移除个别参数，如SparseGPT, LoRAPrune, Wanda。
- 结构化剪枝：根据规则移除连接或层次结构，如LLM-Pruner。

## 知识蒸馏 (Knowledge Distillation, KD)
- 通过学生模型模仿教师模型提高性能，不改变学生模型结构。
- 方法包括上下文学习 (ICL), 思维链 (CoT)，指令跟随 (IF)。

# LMDeploy核心功能
## 模型高效推理
- 使用TurboMind推理引擎，支持LLaMa结构模型，continuous batch推理模式和KV缓存管理。

## 模型量化压缩
- W4A16量化 (AWQ): 将FP16模型权重量化为INT4，大幅降低访存量。
- WeightOnly量化：仅量化权重，数值计算采用FP16。

## 服务化部署
- 将LLM封装为HTTP API服务，支持Triton扩展。

# 量化 (Quantization)

## 量化技术
- 量化感知训练 (QAT): LLM-QAT。
- 量化感知微调 (QAF): PEQA, QLORA。
- 训练后量化 (PTQ): LLM.int8, AWQ。

# 模型部署
## 定义
- 模型部署是将训练好的深度学习模型在特定环境中运行的过程。

## 场景
- 服务器端：CPU部署，单GPU/TPU/NPU部署，多卡/集群部署。
- 移动端/边缘端：移动机器人，手机等。

# LMDeploy推理视觉多模态大模型
## 新功能支持
- 支持多模态大模型LAVA的推理。
- 使用pipeline便捷运行，如图像描述。


# 作业

## 基础截图
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/lmdepoly01.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/lmdepoly02.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/lmdepoly03.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/lmdepoly04.png)
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/lmdepoly05.png)

## 量化+kv cache
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/Basic_Knowledge_InternLM/img/lmdepoly15.png)

