# awesome-codex-usecases

一个专门整理 **Codex 使用案例（Use Cases）** 的仓库。

目标不是简单搬运 skills，而是把外部 skill / workflow / automation 里真正有价值、并且 **可以转换为 Codex 场景** 的能力，整理成清晰、可复用、可直接照着跑的案例。

## 仓库定位

这个仓库专门回答一个问题：

> skillsmp / skills.sh / GitHub 上的 skill，哪些真的值得转成 Codex 用例？

这里不追求“把所有 skill 都收集进来”，而是只做三件事：

- 判断一个 skill 是否适合迁移到 Codex
- 把 skill 背后的工作流改写成 Codex 场景
- 给出一个可以直接复用的案例名称、提纲和拆解方式

## 目录

- [判断标准：能不能转成 Codex Use Case](#判断标准能不能转成-codex-use-case)
- [当前收录的案例方向](#当前收录的案例方向)
- [第一批正式案例名称](#第一批正式案例名称)
- [案例模板](./templates/usecase-template.md)
- [浏览器自动化案例](./usecases/browser-automation.md)
- [PDF 处理案例](./usecases/pdf-processing.md)
- [前端设计案例](./usecases/frontend-design.md)
- [视频工作流案例](./usecases/video-workflow.md)

## 这个仓库整理什么

这里主要整理三类内容：

1. **可以直接在 Codex 里做的案例**
2. **可以通过 skill / 插件 / MCP 扩展后在 Codex 里做的案例**
3. **看起来很强，但实际上不适合直接迁移到 Codex 的案例**

## 判断标准：能不能转成 Codex Use Case

并不是 skillsmp 里的每个 skill 都值得转成 Codex 案例。这里采用下面的判断标准：

### A. 可以直接转换

满足以下任意一类，通常就适合转为 Codex 用例：

- 主要依赖代码生成、文档生成、工作流拆解、搜索总结
- 主要依赖本地文件、命令行、Git、网页访问、脚本执行
- 可以用 Codex 内置工具、浏览器能力、图片能力、shell、MCP 来替代 skill 本身
- skill 背后其实表达的是一种工作方法，而不是绑定某个私有 SaaS

### B. 可以部分转换

这类通常可以变成“半自动 Codex 案例”：

- 原 skill 依赖第三方 API
- 原 skill 依赖某个平台账号/登录态
- 原 skill 依赖浏览器自动化、云端工作流、外部服务

这种案例依然值得保留，但要明确写清：

- Codex 能做哪一段
- 外部服务负责哪一段
- 哪些步骤需要用户自己登录或配置

### C. 不建议直接转换

这类通常不适合直接写成 Codex 案例：

- 强依赖封闭平台内部能力，Codex 无法替代
- 没有公开接口，也没有浏览器路径
- skill 只是一个很薄的壳，没有稳定 workflow
- 只能在某个特定宿主环境里运行，脱离原平台就没有意义

## 当前收录的案例方向

### 1. 浏览器自动化

参考技能方向：

- `sickn33/antigravity-awesome-skills@browser-automation`
- `claude-office-skills/skills@browser-automation`

在 Codex 中可转成：

- 网页自动填写表单
- 后台系统数据录入
- 页面抓取与结果汇总
- 浏览器回归测试

详见：[浏览器自动化案例](./usecases/browser-automation.md)

### 2. PDF / 文档处理

参考技能方向：

- `openai/skills@pdf`
- `claude-office-skills/skills@pdf-extraction`
- `anthropics/knowledge-work-plugins@view-pdf`

在 Codex 中可转成：

- PDF 内容提取
- PDF 转结构化摘要
- 合同 / 报告 / 论文快速审阅
- PDF 转 DOCX 工作流设计

详见：[PDF 处理案例](./usecases/pdf-processing.md)

### 3. 前端设计与页面生成

参考技能方向：

- `anthropics/skills@frontend-design`
- `leonxlnx/taste-skill@design-taste-frontend`

在 Codex 中可转成：

- 落地页生成
- SaaS 后台页面生成
- UI 重构建议
- 前端视觉优化与组件落地

详见：[前端设计案例](./usecases/frontend-design.md)

### 4. 视频工作流

参考技能方向：

- `agentspace-so/runcomfy-agent-skills@video-edit`
- `agentspace-so/runcomfy-agent-skills@image-to-video`
- `agentspace-so/runcomfy-agent-skills@ai-video-generation`

在 Codex 中可转成：

- 视频脚本与分镜生成
- 图生视频工作流设计
- 视频编辑提示词整理
- 多平台短视频生产 SOP

详见：[视频工作流案例](./usecases/video-workflow.md)

## 第一批正式案例名称

下面这些名称优先采用“任务导向”写法，适合直接作为 README、文章标题或子目录名：

### 浏览器自动化

- Codex 做网页自动化回归测试
- Codex 做后台系统表单填写
- Codex 做网页抓取与结果汇总

### 文档 / PDF

- Codex 做 PDF 合同审阅与摘要
- Codex 提取 PDF 结构化要点
- Codex 设计 PDF 转 DOCX 工作流

### 前端 / 设计

- Codex 生成 SaaS 后台前端页面
- Codex 重构产品官网视觉层
- Codex 生成 React 业务页面骨架

### 视频工作流

- Codex 设计图生视频工作流
- Codex 生成短视频分镜脚本
- Codex 组织 AI 视频生产 SOP

## 收录规则

一个案例想进入这个仓库，至少要满足下面 3 条中的 2 条：

1. 能在 Codex 中独立完成主要步骤
2. 即使依赖外部平台，也能由 Codex 负责拆解、组织和输出
3. 输出结果可以被验证，而不是纯概念描述

不优先收录这类案例：

- 只有平台入口，没有工作流
- 强依赖私有环境，无法迁移
- 名字很强，但没有实际执行路径

## 推荐的案例名称格式

建议统一写成：

- `Codex + 场景`
- `Codex 做什么`
- `用 Codex 完成什么任务`

例如：

- Codex 做网页自动化回归测试
- Codex 做 PDF 合同审阅与摘要
- Codex 生成 SaaS 后台前端页面
- Codex 设计图生视频工作流

## 后续可以继续扩展的方向

- GitHub / PR 自动审查
- DevOps 发布与回滚流程
- 飞书 / Lark 自动化
- 股票 / 金融研究
- PPT / Word / Excel 生成
- MCP + 浏览器 + 本地脚本混合工作流

## 说明

这个仓库不是技能市场镜像，而是 **Codex 场景化案例库**。

重点是：

- 这个能力能不能在 Codex 上跑
- 需要哪些前置条件
- 任务应该怎么拆
- 最终案例该怎么命名、怎么复用

后面会继续补：

- GitHub 工作流案例
- DevOps / 发布案例
- 飞书 / Lark 自动化案例
- 金融 / 研究分析案例
- MCP 混合工作流案例
