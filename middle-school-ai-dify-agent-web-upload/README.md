# 基于 Dify 与 DeepSeek 的中学人工智能项目学习双端智能体

本仓库提供一个面向中学信息科技 / 人工智能课程的 Dify 可复现案例资源包，包括：

- `AI项目学习导师（学生端）`
- `AI课程教学设计与评价助手（教师端）`
- 中学 AI 课程官方依据知识库
- 示例输入、复现步骤和安全使用说明

本仓库仅包含可复现资源，不包含账号、密码、API Key、学生隐私数据、申报 PPT 或演示视频。

## 案例定位

本案例希望把生成式 AI 从普通“答疑工具”升级为“项目学习脚手架”。学生端用于支持学生完成问题定义、数据准备、模型实验、测试评价和伦理反思；教师端用于支持实验单生成、项目评价、课堂问题归纳、教学反思和申报证据整理。

典型应用场景：

> 八年级“校园植物图像分类”项目学习。

技术路线：

```text
Dify 工作流 + DeepSeek 模型 + 官方依据知识库 + RAG 检索增强
```

## 仓库结构

```text
.
├─ dify_apps/
│  ├─ student_app_dsl.yml
│  ├─ teacher_app_dsl.yml
│  ├─ student_draft_workflow.json
│  └─ teacher_draft_workflow.json
├─ knowledge_base/
│  └─ official_sources/
│     ├─ 01_课程政策依据与申报定位.md
│     ├─ ...
│     ├─ expanded/
│     └─ raw_pdfs/
├─ docs/
│  ├─ installation.md
│  ├─ reproduction_steps.md
│  ├─ usage_guide_student.md
│  ├─ usage_guide_teacher.md
│  └─ safety_and_privacy.md
├─ examples/
│  ├─ student_demo_questions.md
│  ├─ teacher_demo_inputs.md
│  └─ application_effect_data_template.csv
├─ screenshots/
│  └─ README.md
├─ NOTICE.md
└─ LICENSE
```

## 快速复现

1. 部署或打开 Dify。
2. 配置 DeepSeek 或其他兼容 Chat Model。
3. 新建知识库，上传 `knowledge_base/official_sources/` 中的 Markdown 文件，必要时同时上传 `raw_pdfs/` 中的官方 PDF。
4. 在 Dify 中导入 `dify_apps/student_app_dsl.yml` 和 `dify_apps/teacher_app_dsl.yml`。
5. 打开两个应用工作流中的“官方依据检索”节点，绑定第 3 步创建的知识库。
6. 使用 `examples/` 中的示例问题测试输出。

详细步骤见：[docs/reproduction_steps.md](docs/reproduction_steps.md)。

## 重要说明

- 导入 DSL 后，原工作流中的知识库 ID 在你的 Dify 环境中通常不可直接使用，需要重新选择你本地创建的知识库。
- 本仓库不提供 DeepSeek API Key，需要你在 Dify 后台自行配置模型服务。
- 所有 AI 生成内容应由教师审核后用于课堂。
- 如用于真实课堂，请遵守学生隐私保护要求，不上传学生姓名、人脸、家庭信息等敏感数据。

## 许可证

仓库中原创的 Dify 工作流、提示词、教学化索引和说明文档采用 MIT License。官方政策文件、课程标准和 PDF 原文归原发布机构所有，详见 [NOTICE.md](NOTICE.md)。

