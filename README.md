# 聊天机器人

本项目是一个基于Gradio和Langchain开发的聊天机器人，支持以下四类大模型的调用：

- OpenAI：gpt-3.5-turbo, gpt-3.5-turbo-16k-0613, gpt-3.5-turbo-0613, gpt-4, gpt-4-32k
- 智谱：chatglm_pro, chatglm_std, chatglm_lite, glm-3-turbo, glm-4v, glm-4
- 文心：ERNIE-Bot, ERNIE-Bot-4, ERNIE-Bot-turbo
- 讯飞：Spark-1.5, Spark-2.0

在实际部署的时候需要生成一个.env文件，用于配置各类模型的相应参数，如果只是本地练习，可以在代码run_gradio.py中直接配置。

本项目的启动流程如下所示：

1、python环境配置：

```
pip install -r requirements.txt
```

2、project目录下创建一个名为.env的文件，配置调用每类模型需要的参数，格式如下：

```
ZHIPUAI_API_KEY=""
OPENAI_API_KEY=""
wenxin_api_key=""
wenxin_secret_key=""
spark_api_key=""
spark_appid"]=""
spark_api_secret=""
```

3、运行run_gradio.py

```
python run_gradio.py
```

4、打开 http://localhost:7860 即可看到聊天机器人界面（如果部署在服务器上，就把localhost换成相应IP）：

![image-20240417094802714](figures\界面展示.png)