# task5

> [!TIP]
> 到这一阶段，你已经完成了平面、排版、界面与 Design System 的基础训练，也可能在 Web 端用过 AI 进行问答或生成方案。
> 本任务不再把 AI 当成一次性的灵感工具，而是以一个需要持续设计、实现、部署和维护的个人博客为载体，学习如何让本地 Agent 读取项目上下文、修改真实文件、运行工具、验证结果，并把有效经验沉淀为可复用的 Skill。

## 学习

### 个人博客

> [!TIP]
> 个人博客是个人品牌的“主阵地”，也是寒假轮所有产出最终汇集的地方。
> 它与你此前做过的海报、界面都不相同：它长期存在、持续更新、公开可见，同时考验你的设计能力与对产品至关重要的工程理解能力。

#### 设计

1. 定位与规划
    - Purpose: 明确博客要传达什么：你是谁、你在做什么、你的设计思考是什么
    - Audience: 考虑潜在读者的身份与场景：可能是面试官、同行设计师或一起学习的同学，他们带着什么目的访问你的博客
    - Context: 考虑访问设备（移动端占比）、网络环境（国内访问速度）、维护成本与更新频率等真实限制
2. 信息架构与导航
    - 划分内容分区：文章 / 作品集 / 关于我 / 友链等，并说明取舍
    - 设计首页信息层级：最新文章、精选内容与个人简介的展示顺序和阅读动线
    - 为文章设计分类、标签、归档与搜索，考虑内容变多之后的扩展
3. 视觉系统
    - 与 term1/task2、term1/task4 的要求一致：建立有限且用途明确的 Grid、Spacing、Typography、Color、Radius 规则
    - 深浅色模式都应主动设计，而不是简单反转颜色
    - 响应式：移动端与桌面端分别验证阅读体验
    - 可读性与无障碍：检查文字与背景对比、字号、焦点可见性，不只依靠颜色区分信息
    - 风格选择：明确参考与理由，避免流行风格词的堆砌（想想 term1/task5 对“风格化”的要求）
4. 内容设计
    - 文章页排版：字号、字重、行高、段间距、引用、代码块与图片说明的规则（可回顾 term1/task3 的排版学习）
    - 图片规则：图床选择、压缩策略、长图与横图的处理
    - 阅读动线：让读者快速了解文章价值并愿意读下去
5. 参考样例
    - [Dribbble/blog design](https://dribbble.com/tags/blog-design)
    - [Vercel/templates](https://vercel.com/templates)
    - etc.
6. etc.

#### 实现

> [!TIP]
> 本阶段默认与 Agent 协作完成实现：代码由 Agent 编写，设计由你把关。
> 你不需要成为前端工程师，但需要理解到能够读懂 Agent 的产出、发现问题并精确描述需求的程度

1. 技术选型（理解概念即可）
    - 静态站点生成器（推荐主线之一）：
        - [Astro](https://astro.build/): 内容优先、性能好、组件化
        - [Hexo](https://hexo.io/): 生态成熟、主题丰富
        - [Hugo](https://gohugo.io/): 构建速度快
        - etc.
    - 也可以自行手写 HTML / CSS / JS：掌控力最强，但需自行处理构建与发布
    - 或使用托管平台系：[Notion](https://www.notion.com/) / 语雀等 + 渲染服务
    - 选型前先确认：你希望多大程度定制设计、能承受多少维护成本、内容是否方便迁移
2. 前端概念（理解即可，用于向 AI 描述需求）
    - 理解网页的基本构成：HTML 结构、CSS 样式与 JS 行为的职责分工
    - 理解常用布局方式：盒模型、Flex / Grid、间距与响应式断点（media query）
    - 理解常用交互状态：hover / active / focus / disabled 等，能指出“这个按钮的 hover 态没做”
    - 理解选择器与伪元素（如 ::before / ::after）：能提出“这个卡片需要在 CSS 层面加个 ::before 实现装饰线”这类具体需求
    - 理解组件与模板：页头、页脚、文章卡片等应是可复用组件，而非复制粘贴
    - 目标不是手写代码，而是能读懂 Agent 生成的关键代码、判断其是否符合预期，并把问题定位到具体元素与样式
3. 内容与样式分离
    - 文章使用 Markdown 编写，主题负责视觉规则，这与 term1/task3 的公众号工作流一脉相承
    - 修改视觉时不应逐篇修改文章，修改内容时不应触碰样式
4. Design Token 与主题定制
    - 将颜色、字体、间距等抽象为变量并集中配置（延续 term1/task4 的 Design System 方法）
    - 设计稿与 Token 是你向 Agent 描述需求的依据：先有明确规则，再让 AI 执行
5. 与 Agent 协作的工作流
    - 给出完整上下文：项目结构、设计稿或截图、Design Token、目标设备与浏览器
    - 使用设计术语 + 前端术语描述需求：层级、间距、断点、状态、伪元素等，避免只说“不好看”“更高级”
    - 把任务拆小：每轮只解决边界明确的问题（先布局、再组件、再状态、再细节）
    - 人工验收：在深浅色、移动端与真实内容下检查视觉结果，指出偏差并让 AI 修复，不以“模型已经完成”作为验收结论
    - 检查 AI 生成的代码、字体、图片的来源与授权，保留关键 Prompt、AI 回复摘要与人工修改记录
6. etc.

#### 部署

> [!TIP]
> 部署环节同样可以交给 Agent 协助完成，但你仍需理解每一步在做什么，以便检查结果与日后交接

1. 版本管理
    - 博客源码与文章内容使用 Git 管理，语义化提交（可回顾 steps/README 的提交流程）
    - `.gitignore` 规范：不提交依赖目录、构建缓存、密钥与凭据
2. 部署平台（自选其一）
    - [GitHub Pages](https://pages.github.com/): 免费、与仓库集成
    - [Vercel](https://vercel.com/): 部署体验好、支持 Serverless
    - [Netlify](https://www.netlify.com/): 老牌静态托管
    - etc.
3. 域名与 HTTPS
    - 可选：绑定自定义域名，并了解 HTTPS 的作用
4. 图床与静态资源
    - 加载速度与图片质量的取舍：了解 .webp / .png / .jpg 的区别
    - 将图片格式转换为 webp 可适量存储在仓库中
    - 图片需公网可访问：使用图床（可回顾 term1/task3）或部署平台托管
    - 图床不保证永久可用，重要图片在仓库中保留可回溯副本
5. etc.

#### 维护

1. 发布工作流
    - 建立从 `写作 -> 排版 -> 检查 -> 发布` 的稳定流程，把更新博客的成本降到足够低
    - 日常细节修改可交由 Agent 完成，但每次改动都需人工检查结果
2. 备份与迁移
    - 文章源文件随仓库备份；选型时确认内容可导出、可迁移，避免被平台锁死
3. 统计与反馈
    - 可选：接入评论、访客统计、SEO 等，并说明取舍
4. 持续检查
    - 定期检查失效链接、丢失图片、深浅色与移动端显示异常
5. etc.

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
    - 尝试两类 AI 工作流：
        - 设计工具连接工作流：( Penpot / Figma / etc. ) + MCP Server
        - 文件、代码或开放设计格式工作流：Open Design / Claude Design / etc.
    - 选择一个确实需要项目上下文的任务，例如新增可复用的文章 Callout、同步深浅色 Token、修复移动端导航并补充验证
    - 对 Web 端对话与本地 Agent 使用相同目标和验收标准，比较上下文获取、多文件一致性、工具调用、错误恢复、验证证据、人工修正成本与最终可维护性
    - 不人为削弱 Web 端，也不以回复长度、生成速度或“看起来完成了”作为结论；说明两者分别适合需求梳理、方案讨论、真实修改或持续维护中的哪些环节
4. 使用设计术语与 Agent 进行可回溯的交互式改进：
    - 使用信息层级、Grid、Spacing、Typography、Color、Responsive Layout、Component、Token、State、Accessibility、Feedback 等能够被检查的设计术语描述问题、约束和预期结果，避免只要求“更高级”“更好看”或无任何专业说明的指定某种流行风格
    - 将任务拆为理解上下文、提出方案、执行修改、自检与验收等可观察阶段，注意引入项目级 git，每轮只解决边界明确的问题，并在重要修改后检查文件结构和视觉结果
    - 保留关键 Prompt、AI 回复摘要、输入附件、工具与模型信息、生成结果和人工修改记录，以便后续参考与复用
    - 对两类工作流使用相同或等价的目标与验收标准，比较其对上下文、布局、组件、视觉风格、交互、文件可编辑性和既有设计系统的保留程度
    - 对 Agent 的提议作出接受、修改或拒绝的判断，说明依据；最终结果应人工检查，不以“模型已经完成”作为验收结论
5. 分析 AI 生成与修改结果：
    - 从目标与限制、视觉层级、一致性、可读性、无障碍、状态完整性、响应式表现、可维护性和交付完整性等方面检查结果
    - 使用真实内容、极端内容、不同尺寸或 Mode 验证结果；能够运行的页面可使用 Playwright 等工具辅助检查，但自动截图、像素差异或评分不能代替设计判断
    - 记录 Agent 对源文件造成的非预期修改、重复图层、散落数值、组件 Detach、Token 覆盖、代码或开放文件结构变化等问题，并说明如何定位、恢复或重构
    - 分析至少一个成功案例和一个失败或不采用的案例，说明结果来自上下文质量、Prompt、工具权限、模型能力、文件格式限制还是自己的判断失误
    - 检查 Agent 生成的字体、图标、图片、代码与文案是否存在来源、授权、隐私、偏见或事实性风险；无法确认时不得直接进入最终交付

### Skill：把一次经验变成可复用工作流

1. 认识 Skill
    - Skill 不是风格关键词或一段很长的 Prompt，而是面向一类任务的可复用约定：触发条件、输入、步骤、工具边界、输出、自检、失败停止与人工确认点
    - 适合博客的方向包括：Editorial Typography、主题与 Token、Frontend Design、Accessibility Review、文章 Frontmatter、资源授权检查、发布与回归检查等
2. 使用与评判他人 Skill
    - 先保留不使用 Skill 的 Baseline，再选择至少一个与博客真实问题相关的第三方 Skill，在相同内容和验收标准下运行
    - 尝试使用 Github 高星 Skill，包括但不限于：
        - 设计类 Skill 合集，以及内置 Skill 的设计工作流
            - [nexu-io/open-design/skills](https://github.com/nexu-io/open-design/tree/main/skills)
            - [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)
            - [anthropics/skills](https://github.com/anthropics/skills/tree/main/skills)
        - 通用设计类 Skill
            - [Nutlope/hallmark](https://github.com/Nutlope/hallmark)
            - [anthropics/skills/canvas-design](https://github.com/anthropics/skills/tree/main/skills/canvas-design)
        - Web UI 与前端视觉实现类 Skill
            - [anthropics/skills/frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design)
            - [jezweb/claude-skills/design-loop](https://github.com/jezweb/claude-skills/tree/main/plugins/frontend/skills/design-loop)
        - 品牌规范与主题系统类 Skill
            - [anthropics/skills/brand-guidelines](https://github.com/anthropics/skills/tree/main/skills/brand-guidelines)
            - [anthropics/skills/theme-factory](https://github.com/anthropics/skills/tree/main/skills/theme-factory)
        - 海报构图类 Skill
            - [LiamGvchi/gc-minimal-zine-poster](https://github.com/LiamGvchi/gc-minimal-zine-poster)
            - [ZzzLc0405/photo-abstract-editorial](https://github.com/ZzzLc0405/photo-abstract-editorial)
            - [Zeejay0/gathered-scenes-zine-skill](https://github.com/Zeejay0/gathered-scenes-zine-skill)
        - 生成艺术与图形实验类 Skill
            - [anthropics/skills/algorithmic-art](https://github.com/anthropics/skills/tree/main/skills/algorithmic-art)
        - 演示文稿与信息叙事类 Skill
            - [anthropics/skills/pptx](https://github.com/anthropics/skills/tree/main/skills/pptx)
            - [op7418/guizang-ppt-skill](https://github.com/op7418/guizang-ppt-skill)
        - 动效与视频设计类 Skill
            - [remotion-dev/skills](https://github.com/remotion-dev/skills)
            - [haidrrrry/claude-remotion-skill](https://github.com/haidrrrry/claude-remotion-skill)
        - 无障碍与界面质量检查类 Skill
            - [mgifford/accessibility-skills](https://github.com/mgifford/accessibility-skills/tree/main/skills)
        - etc.
    - 记录来源、版本或 Commit、License、依赖、权限与修改范围；运行第三方脚本前先阅读说明，不以 Star、展示图或单次成功代替评判
    - 学会客观评判设计类 Skill：
        - 鲁棒性：面对信息缺失、矛盾要求、极端内容、工具失败或无法满足的任务时，能否主动确认、合理降级并避免越界修改，而不是仅在示例输入下成立
        - 泛用性：替换主题、内容、媒介、尺寸或项目后，核心方法是否仍可复用，是否把某个案例中的文案、数值与风格误写为通用规则
        - 模型无关：是否明确依赖的模型、Agent、工具与文件格式；在可用条件允许时尝试更换模型或 Agent，检查流程能否迁移，不因 README 中的宣称直接认定其模型无关
        - 审美水平：结果能否说明构图、层级、网格、留白、字体、色彩和内容之间的关系，并在真实内容下保持清晰；不以堆叠装饰、流行风格词或一次生成的精美展示图代替审美判断
        - 风格化：能否将风格拆为可执行、可复现且与内容相符的视觉规则，在多份内容中保持辨识度与一致性，同时避免机械套版或对在世创作者风格的简单模仿
        - 模块化：目标、输入、步骤、工具调用、输出、自检和异常处理是否能够分开理解、替换与组合，局部修改是否会造成无关内容或源文件的大范围变化
        - 可维护性：指令是否清晰、篇幅与重复是否合理，示例是否服务于规则，外部依赖是否稳定，版本变化后是否容易定位、测试与更新
        - 安全与责任边界：是否合理处理权限、隐私、敏感信息、来源授权、事实核查与人工复核，是否会诱导 Agent 忽略用户要求或执行不必要的高风险操作
    - 最终形成对照结论，说明 Skill 适合与不适合的任务、使用前提、主要风险及改进方向
3. 优化或自行设计 Skill
    - 从本次博客中反复出现的问题出发，优化一个实际使用过的 Skill，或自行设计一个新 Skill
    - 使用 [openai/skills/skill-creator](https://github.com/openai/skills/tree/main/skills/.system/skill-creator) 辅助创建和规范 Skill：从具体使用示例出发，规划 `SKILL.md` 与必要的 `scripts / references / assets`，使用其初始化脚本建立标准目录，并在完成后运行 `quick_validate.py` 检查 Frontmatter、命名与必要字段
    - 根据任务的开放程度与出错风险，使用文字指引、参数化脚本或固定脚本设置适当的高 / 中 / 低自由度；`skill-creator` 用于建立和验证可复用工作流，不代替设计者确定目标、审美取舍、工具权限与人工验收边界
    - 从自己在 task2、task3、task4 或本次 AI 工作流中反复遇到的真实问题出发，设计一个能够辅助风格分析、方案生成、设计检查、交付整理或其他明确环节的 Skill；不应只是流行风格词和通用 Prompt 的堆叠
    - 明确 Skill 的 Purpose / Audience / Context、触发条件、适用与不适用范围、所需输入、预期输出、执行步骤、工具与权限边界、失败或停止条件，以及必须由人完成的判断
    - 将设计原则转化为可以观察和检查的规则，并提供必要的模板、示例、反例或验收清单；若依赖特定模型、Agent、插件、MCP Server 或文件格式，应明确记录而不是隐藏依赖
    - 使用真实任务运行 Skill，保留从首次版本、实际失败或偏差、人工反馈到修改版本的记录，并在新的上下文或素材上至少完成一轮复测
    - 最终产物应具有清晰的目录与说明，使未参与编写的同学能够安装或引用、准备输入、完成核心流程、判断结果是否合格，并在遇到限制时安全退出

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
    - 总结：
        - 设计类 Skill 的优点：
            - 分析它在外化隐性经验、稳定工作步骤、补全检查项、减少重复劳动、保持跨轮次一致性与帮助他人复用工作流等方面的实际价值，并用本次证据说明其成立条件
        - 设计类 Skill 的不足：
            - 分析上下文与模型差异、工具和文件格式限制、审美趋同、错误被流程化放大、维护成本、权限风险以及无法替代真实用户研究和人工设计判断等问题
        - 辅助风格化设计：
            - 说明如何把参考风格拆为构图、字体、色彩、形状、材质、图像处理、动效与内容语气等可执行规则，并通过 Component / Token / 模板或约束维持一致性，而不是只要求“生成某种风格”
            - 区分参考、提炼、迁移与模仿，记录参考来源、授权与人工改动；风格化不得破坏信息层级、可读性、无障碍、品牌目标和媒介限制
        - 建议对比直接 Prompt、他人 Skill、优化后的 Skill 与自行设计 Skill 的适用场景和成本，总结一份心得体会
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
