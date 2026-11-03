<div align="center">
<p align="center">
  <a href="https://www.bright.cn/">
    <img src="https://mintlify.s3.us-west-1.amazonaws.com/brightdata/logo/light.svg" width="300" alt="Bright Data 徽标">
  </a>
</p>

# AI 驱动的潜在客户开发智能体

一款新一代潜在客户开发工具，利用 Bright Data 抓取最新的 B2B 联系人数据，并通过 OpenAI 筛选和丰富数据、提供外联策略：所有操作均可在流畅的 Streamlit UI 中完成。

<img src="https://img.shields.io/badge/python-3.9+-blue" /> <img src="https://img.shields.io/badge/OpenAI-API-blueviolet" /> <img src="https://img.shields.io/badge/License-MIT-blue" />

<img src="https://media.brightdata.com/2025/09/image-78.png" />
</div>

---

## 功能

- 🕵️♂️ **自动网页爬虫：** 通过 Bright Data 的爬虫 API，即时从 LinkedIn 等来源采集最新潜在客户。
- 📈 **AI 驱动的客户筛选：** 使用 OpenAI 分析、评分并丰富潜在客户信息，告别人工猜测，不再错失潜在客户。
- 💡 **自然语言输入：** 只需描述你的理想潜在客户，智能体便会提取结构化筛选条件并运行完整工作流。
- 🤝 **外联建议：** 获取针对每位潜在客户量身定制的现成个性化建议，用于电子邮件或 LinkedIn 互动。
- 🖥 **交互式 UI：** 通过易于使用的 Streamlit 控制面板管理工作流和设置。

---

## 前提条件

- Python 3.9+
- [Bright Data 账户](https://www.bright.cn/)（含 API 令牌）
- [OpenAI API 密钥](https://platform.openai.com/api-keys)
- 已安装 [Streamlit](https://streamlit.io/)
- [Bright Data 数据集访问权限](https://docs.brightdata.com/api-reference/datasets)
- （可选）安装 dotenv，以便更轻松地管理 API 密钥

---

## 安装

1. **克隆代码仓库**
   ~~~bash
   git clone <repository-url>
   cd ai-leadgen-agent
   ~~~

2. **创建并激活 Python 虚拟环境**
   ~~~bash
   python -m venv venv
   # macOS/Linux: source venv/bin/activate
   # Windows: venv\Scripts\activate
   ~~~

3. **安装依赖项**
   ~~~bash
   pip install -r requirements.txt
   ~~~

4. **设置 API 凭据**
   - 创建一个 `.env` 文件：
     ~~~env
     OPENAI_API_KEY=your_openai_api_key_here
     BRIGHT_DATA_API_KEY=your_bright_data_api_key_here
     ~~~
   - 或者，直接在 Streamlit 侧边栏中输入。

---

## 使用方法

1. **启动应用程序**
   ~~~bash
   streamlit run app.py
   ~~~

2. **在浏览器中打开**
   - 访问 `http://localhost:8501`（将自动打开）

3. **描述你的潜在客户**
   - 输入如下自然语言查询：  
     `Find marketing managers in fintech companies in Kenya.`
   - 点击 **生成潜在客户**。

4. **查看丰富后的结果**
   - 查看经过完整评分、排序和信息丰富处理的潜在客户。
   - 每位潜在客户均包含 AI 摘要、相关性评分和外联建议。

---

## 工作原理

1. **自然语言查询：** 只需输入你的要求（职位、行业、地点等）。
2. **筛选条件提取：** 系统使用 OpenAI 解析你的查询，并将其转换为 API 筛选条件。
3. **潜在客户数据采集：** Bright Data API 会触发定向抓取（例如 LinkedIn 职位或个人资料）。
4. **AI 信息丰富：** 每位潜在客户的信息都会发送至 OpenAI 进行分析，包括评分、总结以及推荐最佳互动渠道。
5. **交互式探索：** 所有结果均通过 Streamlit 中易于使用的卡片和可视化图表展示。

---

## 输出功能

- **AI 评分的潜在客户：** 即时获得排名和洞察，无需使用电子表格！
- **相关性与外联建议：** 查看每位潜在客户为何匹配，以及如何与其互动。
- **可自定义工作流：** 调整潜在客户数量、信息丰富深度，或针对你的 ICP 优化提示词。
- **调试模式：** 追踪每项决策和 API 调用，确保完全透明。

---

## 配置

### .env 文件  
妥善保护你的 API 密钥：
~~~env
OPENAI_API_KEY=your_openai_api_key_here
BRIGHT_DATA_API_KEY=your_bright_data_api_key_here
~~~

### 侧边栏设置
- **Bright Data API 密钥：** 粘贴密钥（或使用 .env）
- **OpenAI API 密钥：** 粘贴密钥（或使用 .env）
- **模型选择器：** 例如 GPT-3.5、GPT-4O 等
- **潜在客户数量上限：** 设置要获取的潜在客户数量（默认值：10）

---

## 故障排除

- **未找到潜在客户**
  - 检查 API 密钥和数据集访问权限
  - 放宽搜索筛选条件（职位、地点等）
  - 调试模式会提供详细错误信息

- **信息丰富处理失败**
  - 确保你的 OpenAI API 密钥有效且未受到速率限制
  - 检查 API 和网络连接

- **Bright Data 错误**
  - 确保你的令牌拥有正确的权限
  - 查看 [Bright Data 文档](https://docs.brightdata.com/introduction)

---

## 许可证

本项目仅用于教育和内部演示。

---

## 了解更多

- [Bright Data 数据集的工作原理](https://docs.brightdata.com/api-reference/datasets)
- [Streamlit 文档](https://docs.streamlit.io/)
- [OpenAI 平台文档](https://platform.openai.com/docs)

---

**准备好全面提升销售线索挖掘效率了吗？立即部署你自己的 AI 驱动潜在客户开发智能体，将手动搜索潜在客户转化为即时获取的优质商机！**

<p align="center">
  <a href="https://www.bright.cn/cp/start" target="_blank" style="text-decoration:none;">
    <img src="https://img.shields.io/badge/Get%20Started-%233D7FFC?style=for-the-badge&logo=rocket&logoColor=white" alt="立即开始" style="height: 48px; border-radius: 8px;">
  </a>
</p>

---



**使用 Bright Data 和 OpenAI 倾情打造 ❤️**
