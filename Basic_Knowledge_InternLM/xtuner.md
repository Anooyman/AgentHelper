
# 数据准备

- 按照以下数据格式构建数据集
- 目的是为了模拟模型过拟合的情况

```python3
"messages": [
                {
                    "role": "user",
                    "content": "请做一下自我介绍"
                },
                {
                    "role": "assistant",
                    "content": "我是{}的小助手，内在是上海AI实验室书生·浦语的1.8B大模型哦".format(name)
                }
        ]
```

# 模型微调

## 基础模型评估结果截图
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/weitiao01.png)

## 300 轮评估结果截图

![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/weitiao02.png)

## 600 轮评估结果截图

![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/weitiao03.png)

## 微调结束评估结果截图

![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/weitiao04.png)

## 文件夹截图
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/weitiao05.png)

# 微调结果展示

## 基础模型对话内容截图
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/weitiao06.png)

## 微调之后对话内容截图
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/weitiao07.png)

## web demo 对话内容截图
![image](https://github.com/Anooyman/AgentHelper/blob/main/Basic_Knowledge_InternLM/img/weitiao08.png)