<div align="center">
<p align="center">
  <a href="https://www.bright.cn/">
    <img src="https://mintlify.s3.us-west-1.amazonaws.com/brightdata/logo/light.svg" width="300" alt="Bright Data 标志">
  </a>
</p>

# AI 驱动的线索生成智能体

一款新一代线索生成工具：利用 Bright Data 抓取最新的 B2B 联系方式数据，并使用 OpenAI 进行资格评估、数据丰富与外联策略建议——全部在无缝的 Streamlit 界面中完成。

<img src="https://img.shields.io/badge/python-3.9+-blue" /> <img src="https://img.shields.io/badge/OpenAI-API-blueviolet" /> <img src="https://img.shields.io/badge/License-MIT-blue" />

<img src="https://media.brightdata.com/2025/09/image-78.png" />
</div>

---

## 功能

- 🕵️‍♂️ 自动化网页抓取：通过 Bright Data 抓取 API，瞬时从 LinkedIn 等来源获取最新线索。
- 📈 AI 资格评估：使用 OpenAI 分析、打分并丰富线索——告别盲猜与丢单。
- 💡 自然语言输入：只需描述你的理想线索；智能体会提取结构化筛选条件并执行完整流程。
- 🤝 外联建议：为邮件或 LinkedIn 互动提供现成、个性化的建议，针对每个线索量身定制。
- 🖥 交互式界面：在友好的 Streamlit 控制台中管理管道与设置。

---

## 前置条件

- Python 3.9+
- 拥有 [Bright Data 账号](https://www.bright.cn/)（含 API Token）
- [OpenAI API Key](https://platform.openai.com/api-keys)
- 安装 [Streamlit](https://streamlit.io/)
- 具备 [Bright Data Datasets 访问权限](https://docs.brightdata.com/api-reference/datasets)
- （可选）dotenv 以便更易管理 API Key

---

## 安装

1. 克隆仓库
   ~~~bash
   git clone <repository-url>
   cd ai-leadgen-agent
   ~~~

2. 创建并激活 Python 虚拟环境
   ~~~bash
   python -m venv venv
   # macOS/Linux: source venv/bin/activate
   # Windows: venv\Scripts\activate
   ~~~

3. 安装依赖
   ~~~bash
   pip install -r requirements.txt
   ~~~

4. 设置 API 凭据
   - 创建 `.env` 文件：
     ~~~env
     OPENAI_API_KEY=your_openai_api_key_here
     BRIGHT_DATA_API_KEY=your_bright_data_api_key_here
     ~~~
   - 或在 Streamlit 侧边栏中直接输入。

---

## 使用

1. 启动应用
   ~~~bash
   streamlit run app.py
   ~~~

2. 在浏览器中打开
   - 访问 `http://localhost:8501`（将自动打开）

3. 描述你的线索需求
   - 输入自然语言查询，例如：  
     `Find marketing managers in fintech companies in Kenya.`
   - 点击 Generate Leads。

4. 查看丰富后的结果
   - 查看已打分、排序并完成丰富的线索。
   - 每条线索包含 AI 摘要、相关性评分与外联建议。

---

## 工作原理

1. 自然语言查询：直接输入你的需求（岗位、行业、地域等）。
2. 筛选提取：系统使用 OpenAI 将你的查询解析为 API 过滤参数。
3. 线索采集：Bright Data 的 API 触发定向抓取（如 LinkedIn 职位或个人资料）。
4. AI 丰富：将每条线索交给 OpenAI 分析：打分、总结，并建议最佳触达渠道。
5. 交互探索：所有结果在 Streamlit 中以卡片与可视化方式呈现。

---

## 输出特性

- AI 打分线索：即时排名与洞察——无需再用电子表格！
- 相关性与外联建议：了解每条线索为何契合，以及如何有效触达。
- 可定制流程：调整线索数量、丰富深度，或根据你的 ICP 微调提示词。
- 调试模式：追踪每一步决策与 API 调用，透明可查。

---

## 配置

### .env 文件  
安全管理你的 API Key：
~~~env
OPENAI_API_KEY=your_openai_api_key_here
BRIGHT_DATA_API_KEY=your_bright_data_api_key_here
~~~

### 侧边栏设置
- Bright Data API Key：粘贴密钥（或使用 .env）
- OpenAI API Key：粘贴密钥（或使用 .env）
- 模型选择：如 GPT-3.5、GPT-4O 等
- 最大线索数：设置抓取的线索数量（默认：10）

---

## 故障排查

- 未找到线索
  - 检查 API Key 与数据集访问权限
  - 放宽筛选条件（岗位、地域等）
  - 使用调试模式查看详细错误

- 丰富失败
  - 确保 OpenAI API Key 有效且未触发限流
  - 检查 API 与网络连接

- Bright Data 报错
  - 确保你的 Token 拥有正确的权限
  - 查阅 [Bright Data 文档](https://docs.brightdata.com/introduction)

---

## 许可证

本项目仅用于教育与内部演示目的。

---

## 了解更多

- [Bright Data Datasets 工作原理](https://docs.brightdata.com/api-reference/datasets)
- [Streamlit 文档](https://docs.streamlit.io/)
- [OpenAI 平台文档](https://platform.openai.com/docs)

---

准备好为你的销售拓客加速了吗？立即启动你的 AI 驱动线索生成智能体，把繁琐的手动找客转化为即时、可筛选的高质量商机！

<p align="center">
  <a href="https://www.bright.cn/cp/start" target="_blank" style="text-decoration:none;">
    <img src="https://img.shields.io/badge/Get%20Started-%233D7FFC?style=for-the-badge&logo=rocket&logoColor=white" alt="Get Started" style="height: 48px; border-radius: 8px;">
  </a>
</p>

---

**由 Bright Data 与 OpenAI 倾情打造 ❤️**
