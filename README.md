#  AI 智能厨师 Agent

基于大模型构建的 AI 智能厨师 Agent 系统，能够识别用户上传的食材图片或文本清单，自动分析食材种类、新鲜度及可用量，并结合联网搜索能力智能检索相关菜谱。系统通过对营养价值、制作难度、食材利用率等维度进行量化评分，生成结构化菜谱推荐方案，实现“从食材识别到智能做饭决策”的完整 AI Agent 工作流。

---

#  项目亮点

*  **智能食材识别**

  * 支持图片上传与文本输入
  * 自动识别食材种类、数量与状态
  * 基于视觉与语义能力评估新鲜度

*  **大模型 Agent 决策能力**

  * 基于 LLM 实现多步骤推理
  * 自动分析用户意图
  * 动态生成个性化做饭方案

*  **联网搜索菜谱**

  * 实时检索互联网菜谱资源
  * 自动融合多个菜谱信息
  * 提供更加丰富且可靠的推荐结果

*  **菜谱智能评分系统**
  从多个维度对菜谱进行量化评估：

  * 营养价值
  * 制作难度
  * 时间成本
  * 食材利用率
  * 用户匹配度

*  **结构化菜谱生成**
  自动输出：

  * 推荐理由
  * 食材清单
  * 制作步骤
  * 营养分析
  * 注意事项

---

#  Agent 工作流

```text
用户上传图片/文本
        ↓
食材识别与状态分析
        ↓
食材数量与新鲜度评估
        ↓
联网搜索相关菜谱
        ↓
LLM 综合分析与推理
        ↓
菜谱评分与排序
        ↓
生成结构化推荐方案
```

---

#  技术架构

## 后端

* Python
* FastAPI / Flask
* LangChain
* OpenAI / DeepSeek API
* Tavily Search
* Pydantic

## AI 能力

* 多模态图片识别
* 大语言模型推理
* Agent 工具调用
* RAG / 联网搜索增强

## 前端（可选）

* Vue3
* TypeScript
* Element Plus
* Axios

---

#  核心功能

| 功能模块     | 描述           |
| -------- | ------------ |
| 食材识别     | 识别图片中的食材种类   |
| 新鲜度分析    | 判断食材状态与可用程度  |
| 文本解析     | 支持自然语言输入食材清单 |
| 菜谱搜索     | 联网检索相关做法     |
| 智能推荐     | 基于多维度评分生成推荐  |
| 菜谱生成     | 输出完整做饭方案     |
| Agent工作流 | 实现自动化推理与决策   |

---

#  项目效果

### 输入示例

```text
西红柿、鸡蛋、土豆，还有一块牛肉
```

或上传冰箱食材图片。

### 系统输出

```text
推荐菜谱：番茄牛肉汤

推荐原因：
- 食材匹配度高
- 营养均衡
- 制作难度适中

营养评分：9.2
制作难度：★★★☆☆
预计时间：35分钟
```


---

#  环境配置

项目运行前需要自行配置相关 API Key 与云存储服务。

## 必需配置

### 1. DeepSeek API Key

用于大模型推理与 Agent 能力调用。

* DeepSeek 平台：
  [https://platform.deepseek.com/api_keys](https://platform.deepseek.com/api_keys)

### 2. 阿里云 OSS Bucket

用于图片上传与食材图片存储。

* OSS 控制台：
  [https://oss.console.aliyun.com/overview](https://oss.console.aliyun.com/overview)

创建 Bucket 后需要配置：

```env
OSS_ACCESS_KEY_ID=your_key
OSS_ACCESS_KEY_SECRET=your_secret
OSS_BUCKET=your_bucket
OSS_ENDPOINT=your_endpoint
```

### 3. LangSmith（可选）

用于 LangChain Agent 调试、链路追踪与运行监控。

* LangSmith：
  [https://smith.langchain.com](https://smith.langchain.com)

配置示例：

```env
LANGCHAIN_API_KEY=your_key
LANGCHAIN_TRACING_V2=true
LANGCHAIN_PROJECT=AI-Chef-Agent
```

---

#  安装与运行

## 1. 克隆项目

```bash
git clone https://github.com/your-name/AI-Chef-Agent.git
```

## 2. 安装依赖

```bash
pip install -r requirements.txt
```

## 3. 配置环境变量

创建 `.env` 文件：

```env
OPENAI_API_KEY=your_api_key
TAVILY_API_KEY=your_api_key
```

## 4. 启动项目

```bash
python app.py
```

---

#  项目价值

该项目不仅是一个“智能做饭助手”，更是一个完整的 AI Agent 实践案例，涵盖：

* 多模态输入处理
* 大模型工具调用
* 联网搜索增强
* Agent 工作流设计
* Prompt Engineering
* 智能推荐系统

适合作为：

* AI Agent 项目实践
* 大模型应用开发案例
* LangChain 学习项目
* 多模态 AI Demo
* 求职/简历项目展示

---

#  后续优化方向

* [ ] 用户饮食偏好学习
* [ ] 热量与减脂推荐
* [ ] AI 语音助手
* [ ] 冰箱库存管理
* [ ] 个性化营养分析
* [ ] 自动生成购物清单
* [ ] 多语言支持
* [ ] 微信小程序接入

---

#  致谢

感谢以下技术生态支持：

* OpenAI
* DeepSeek
* LangChain
* Tavily
* Vue3
* FastAPI

---


