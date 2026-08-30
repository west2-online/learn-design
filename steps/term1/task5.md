# task5

> [!TIP]
> 到这一阶段，你已经完成了平面、排版、界面与 Design System 的基础训练，也可能在 Web 端用过 AI 进行问答或生成方案。
> 本任务不再把 AI 当成一次性的灵感工具，而是以一个需要持续设计、实现、部署和维护的个人博客为载体，学习如何让本地 Agent 读取项目上下文、修改真实文件、运行工具、验证结果，并把有效经验沉淀为可复用的 Skill。

## 学习

### 个人博客：长期存在的设计与内容产品

1. 定位与信息架构
    - Purpose：明确博客要传达什么，你是谁、正在学习什么、希望留下哪些内容
    - Audience：考虑面试官、同行、同学等读者带着什么目的访问，以及他们首先需要看到什么
    - Context：考虑移动端阅读、国内网络环境、内容更新频率、维护成本与长期迁移
    - 规划首页、文章列表、文章详情、关于我等必要页面，以及分类、标签、归档和搜索的取舍
2. 视觉系统与内容设计
    - 延续 term1/task2、term1/task4：建立用途明确的 Grid、Spacing、Typography、Color、Radius 与 Component 规则
    - 将规则组织为 Design Token，并说明它们如何从 Figma 映射到代码变量
    - 主动设计深浅色模式、桌面端与移动端，不把反色和等比缩放当成适配
    - 为标题、正文、引用、代码块、列表、图片说明、链接与 Callout 建立长文排版规则
    - 使用真实文章和极端内容检查信息层级、行长、换行、图片比例与组件状态
3. 实现与长期维护
    - 理解 HTML 结构、CSS 样式、JavaScript 行为、Component、Template 与 Design Token 的职责边界
    - 文章以 Markdown 等可迁移格式保存，内容与主题分离；修改视觉时不应逐篇修改文章
    - 可选择 Astro / Hexo / Hugo 等静态站点生成器，也可自行实现；选型需说明定制能力、构建部署、维护成本和迁移风险
    - 使用 Git 管理源码与文章，建立构建、检查、部署、备份与失效链接维护流程

### 从 Web 端 AI 到本地 Agent

> [!IMPORTANT]
> Web 端对话擅长解释、发散和提供片段；本地 Agent 的关键价值在于能够进入真实项目，在明确权限内连续完成「读取上下文 -> 修改多处文件 -> 运行命令 -> 观察错误 -> 修复 -> 查看差异 -> 验收」的闭环。
> 这不代表 Agent 的建议天然正确。它获得了更多上下文与工具，也可能更快地放大错误，因此必须限制范围、保留版本并由人验收。

1. 环境与上下文
    - 本地安装并使用至少一种 Agent，如 [Codex](https://github.com/openai/codex)、[OpenCode](https://opencode.ai/) 或 [Claude Code](https://github.com/anthropics/claude-code)
    - 配置项目实际需要的 Node.js / Python / 浏览器检查工具，不为展示工具数量安装无关依赖
    - 让 Agent 先读取 README、目录结构、构建脚本、设计规则和已有改动，再提出计划；不要把整个项目无边界地塞进单轮 Prompt
    - 明确可修改目录、冻结内容、完成标准与禁止事项；API Key、Token、Cookie、`.env` 和私人内容不得写入 Prompt、仓库或公开日志
2. 可回溯的协作闭环
    - 先写清目标、输入、约束、允许修改的范围与验收标准，再让 Agent 执行
    - 将工作拆为边界明确的轮次，如「信息架构」「Token 与主题」「文章组件」「响应式」「无障碍」「部署」，每轮结束后检查结果
    - 使用设计术语与前端术语描述问题，例如层级、Grid、Breakpoint、State、Focus、Selector 与 Component，而不是只说“更高级”“更好看”
    - 在重要修改前后查看 Git 状态与差异；保留自己的既有改动，发现越界修改时能够定位、撤回或重新限定任务
    - 运行真实构建、Lint、链接检查和浏览器流程；自动检查用于发现问题，不能代替视觉判断与真实阅读
3. Agent 与 Web 端的对照
    - 选择一个确实需要项目上下文的任务，例如新增可复用的文章 Callout、同步深浅色 Token、修复移动端导航并补充验证
    - 对 Web 端对话与本地 Agent 使用相同目标和验收标准，比较上下文获取、多文件一致性、工具调用、错误恢复、验证证据、人工修正成本与最终可维护性
    - 不人为削弱 Web 端，也不以回复长度、生成速度或“看起来完成了”作为结论；说明两者分别适合需求梳理、方案讨论、真实修改或持续维护中的哪些环节

### Skill：把一次经验变成可复用工作流

1. 认识 Skill
    - Skill 不是风格关键词或一段很长的 Prompt，而是面向一类任务的可复用约定：触发条件、输入、步骤、工具边界、输出、自检、失败停止与人工确认点
    - 适合博客的方向包括：Editorial Typography、主题与 Token、Frontend Design、Accessibility Review、文章 Frontmatter、资源授权检查、发布与回归检查等
2. 使用与评判他人 Skill
    - 先保留不使用 Skill 的 Baseline，再选择至少一个与博客真实问题相关的第三方 Skill，在相同内容和验收标准下运行
    - 可参考：
        - [anthropics/skills/frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design)
        - [anthropics/skills/brand-guidelines](https://github.com/anthropics/skills/tree/main/skills/brand-guidelines)
        - [mgifford/accessibility-skills](https://github.com/mgifford/accessibility-skills/tree/main/skills)
        - [jezweb/claude-skills/design-loop](https://github.com/jezweb/claude-skills/tree/main/plugins/frontend/skills/design-loop)
        - etc.
    - 记录来源、版本或 Commit、License、依赖、权限与修改范围；运行第三方脚本前先阅读说明，不以 Star、展示图或单次成功代替评判
    - 从鲁棒性、泛用性、模型与工具依赖、审美判断、模块化、可维护性、安全和人工修正成本分析结果
3. 优化或自行设计 Skill
    - 从本次博客中反复出现的问题出发，优化一个实际使用过的 Skill，或自行设计一个新 Skill
    - 可使用 [openai/skills/skill-creator](https://github.com/openai/skills/tree/main/skills/.system/skill-creator) 规划 `SKILL.md` 与必要的 `scripts / references / assets`，并执行其结构校验
    - 明确 Purpose / Audience / Context、适用与不适用范围、输入输出、执行顺序、工具权限、失败停止条件和人工验收点
    - 在原任务之外换一篇文章、一个组件或一个页面复测；保留失败结果与修改依据，证明它能够迁移，而不是只记住本次博客的文案和数值

## 作业

1. 建立项目 Baseline 与实施计划：
    - 明确博客的 Purpose / Audience / Context、内容范围、必要页面、技术限制与不做事项
    - 调研同类博客与可选技术方案，说明借鉴、舍弃和最终选型理由
    - 建立 Git 仓库、README、基础目录与可运行的初始版本；记录初始构建结果，避免在无法运行的起点上继续堆叠修改
    - 将「新增能力 -> 实施步骤 -> 作业证据」写入计划，至少覆盖设计系统、Agent 协作、Agent / Web 对照、Skill、部署与维护
2. 完成个人博客的设计：
    - 完成首页、文章列表、文章详情与关于我页面；内容较多时补充分类、标签、归档或搜索中的必要部分
    - 建立 Grid、Spacing、Typography、Color、Radius、Component 与 State 规则，完成深浅色和桌面 / 移动端设计
    - 至少使用三篇真实文章验证长短标题、代码块、引用、列表、图片和链接等内容，不以 Lorem Ipsum 作为最终验收内容
    - 在 Figma 中使用 Frame、Component 与 Variables 组织设计；视觉过程与最终设计统一通过一个可访问的 Figma 链接展示，不在提交仓库中放置预览图、截图、录屏或设计导出图
3. 使用本地 Agent 完成真实实现：
    - 将设计规则落地为集中管理的 Token / 变量和可复用组件，保持文章内容与主题样式分离
    - 至少完成三次需要读取既有项目并修改多个相关文件的 Agent 协作，每次记录任务边界、关键 Prompt、修改文件、运行命令、验收结果与人工决定
    - 至少保留一个 Agent 首次实现失败、越界或不符合设计的案例，说明如何从日志、浏览器行为或 Git Diff 定位并修复
    - 能够读懂关键结构和样式，解释 Agent 修改了哪里、为什么能解决问题，以及如果失败应如何恢复；不以“Agent 已完成”作为验收结论
4. 完成 Agent 与 Web 端 AI 对照：
    - 选择一个包含真实仓库上下文、跨文件修改与运行验证的小任务，对两者使用相同目标和验收标准
    - 输出对照记录：上下文提供方式、建议或修改内容、能否直接运行、遇到错误后的处理、人工修正次数、最终差异与适用场景
    - 用本次证据说明 Agent 相比 Web 端增加了哪些能力，又增加了哪些权限、误改、依赖与验证风险
5. 使用并沉淀 Skill：
    - 保留无 Skill 的 Baseline，使用至少一个第三方 Skill 解决博客中的真实设计或检查问题，完成来源、License、依赖、权限与结果评判
    - 优化该 Skill 或自行设计一个 Skill，提交完整可复用文件；至少包含触发条件、输入输出、步骤、检查顺序、停止条件、风险与人工确认点
    - 使用新内容或新场景复测原版与修改版，比较结果、失败情况和人工修正成本，并说明它适合与不适合什么任务
6. 部署、验证并维护博客：
    - 将博客部署到公网，保证链接可访问；说明构建、部署、HTTPS、静态资源和回滚方式
    - 使用真实浏览器检查核心页面、导航、链接、深浅色、键盘 Focus 和至少一个窄屏尺寸，并保留文字化结果或测试日志
    - `.gitignore` 不提交依赖、构建缓存、密钥、Token 与 `.env`；检查字体、图片、图标、模板、代码和 AI 生成内容的来源与授权
    - 建立 `写作 -> 检查 -> 构建 -> 发布 -> 回归` 流程，并实际新增或更新一篇文章验证维护成本
7. 提交内容：
    - 可访问的个人博客链接、源码仓库链接与 Figma 设计链接
    - README：博客定位、信息架构、技术选型、目录结构、Design Token、运行与部署、维护与迁移、资产授权和他人交接方式
    - Agent 协作记录与 Agent / Web 对照报告：包含关键输入、实际修改、命令和验证、失败恢复与人工判断，不提交私密对话、凭据或无关完整日志
    - 第三方 Skill 来源与评判报告，以及优化后或自行设计的 Skill 源文件和新场景复测记录
    - 提交仓库不需要任何视觉预览图、截图、录屏或设计导出文件；测试截图如由工具临时生成，仅作为本地检查材料，不代替 Figma、可访问网站和文字化验证结果

> [!NOTE]
> 面试会围绕同一处真实改动追问：你如何定义问题，Web 端与 Agent 分别做了什么，Agent 修改了哪些文件、运行了哪些检查，Skill 如何影响结果，你接受、修改或拒绝了什么，以及网站以后如何维护。
> 评价重点是设计判断、上下文组织、工程闭环、风险控制和可复用性，而不是使用了多少工具或生成了多少页面。
