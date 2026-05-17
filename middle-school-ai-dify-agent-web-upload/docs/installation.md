# 安装与环境准备

## 1. 准备 Dify

你可以使用以下任一方式：

- Dify 云服务
- 本地 Docker 部署的 Dify
- 学校服务器部署的 Dify

本案例需要 Dify 支持：

- DSL 应用导入
- Workflow / Chatflow
- Knowledge 知识库
- Chat Model 配置

## 2. 配置模型

本案例原始环境使用 DeepSeek。复现时建议优先使用：

- DeepSeek Chat
- 或 Dify 支持的其他中文能力较强的 Chat Model

配置位置通常在：

```text
Dify 控制台 → 设置 → 模型供应商
```

注意：本仓库不包含任何模型 API Key。

## 3. 下载本仓库

```bash
git clone https://github.com/czmlog/middle-school-ai-dify-agent.git
cd middle-school-ai-dify-agent
```

也可以直接在 GitHub 页面下载 ZIP。

