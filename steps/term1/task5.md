# task5

## 学习

### AI 融合工作流

> [!TIP]
> 由于我们并不禁止在考核中对 AI 的合理使用，因此你在这时可能已经有一定的使用心得了，
> 不过我们这里做的事情仍然有价值：
> 我们期望你们对 AI 在设计工作流中的真实能力与局限做到“知其所以然”，
> 以及知晓如何面对、吸纳和评判他人 AI 出的设计相关的视觉成果。

1. 前期准备
    - 本地安装常用 Agent（自选其一安装即可）:
        - [Codex](https://github.com/openai/codex)
        - [Opencode](https://opencode.ai/)
        - [Claude Code](https://github.com/anthropics/claude-code)
        - etc.
    - 配置环境与 PATH:
        - [Python](https://www.python.org/)
        - [Node.js](https://nodejs.org/)
        - [Playwright](https://playwright.dev/)
        - etc.
2. AI 工作流尝试 1: [Penpot](https://penpot.app/)（不强制，可用 Figma AI 完成）
    - 学会使用设计术语撰写 prompt 对项目进行交互式改进
    - 尝试在项目中使用 Skill 获得与你期望从其演示效果中获得的效果
3. AI 工作流尝试 2: Open Design / Claude Design / Codex / etc.
    - 了解其编辑文件的方法区别
    - 尝试自行对“风格化”这个概念进行与 Skill 进行比较，分析其异同
    - 学会客观的评判 Skill
    - 尝试自行设计一个 Skill
4. etc.

## 作业

1. 完成 Github 个人主页的设计，并保留后续优化的空间。推荐至少完成以下功能：
    - 简单明了，得体美观的自我介绍卡片
    - Github Stats 类似物（自部署 / 在自己电脑上跑CI / etc）
    - 技术栈展示卡片
    - 本次完成的 Skill 的 展示卡片
    - （可选）个人博客和作品集入口或展示卡片
    - （可选）自己的贡献过的仓库
    - 你或许可以参考的 Github 个人主页：
        - [Seeridia](https://github.com/Seeridia)
        - etc.
    - 注意：
        - 不要使用 emoji → 使用合规 / 自建 icon 库
        - 要考虑到深浅色切换
        - 不要太繁复，要考虑移动端设备的阅读体验
        - 不要局限于 github 上展示的 README.md，这里只是提供一个载体供你自由的完成个人展示的组件设计
        - 如果你想提前完成一些寒假轮内容，可以直接设计个人博客而无需完成本任务
2. 部署本地 AI 工作流：
    - 本地安装并使用至少一种常用 Agent，如 Codex / Opencode / Claude Code / Pi / etc.
    - 配置 Python、Node.js、Playwright、MCP Server 等本地必要环境与 PATH，验证 Agent 能够读取预期上下文、调用预期工具并输出到正确位置
    - 尝试两类 AI 工作流：
        - 设计工具连接工作流：( Penpot / Figma / etc. ) + MCP Server
        - 文件、代码或开放设计格式工作流：Open Design / Claude Design / etc.
    - 注意不要将 API Key 等配置文件与示例中的私有凭据或密钥暴露到公网上，而是使用环境变量、凭据存储或占位值说明
3. 使用设计术语与 AI 进行可回溯的交互式改进：
    - 使用信息层级、Grid、Spacing、Typography、Color、Responsive Layout、Component、Token、State、Accessibility、Feedback 等能够被检查的设计术语描述问题、约束和预期结果，避免只要求“更高级”“更好看”或无任何专业说明的指定某种流行风格
    - 将任务拆为理解上下文、提出方案、执行修改、自检与验收等可观察阶段，注意引入项目级 git，每轮只解决边界明确的问题，并在重要修改后检查文件结构和视觉结果
    - 保留关键 Prompt、AI 回复摘要、输入附件、工具与模型信息、生成结果和人工修改记录，以便后续参考与复用
    - 对两类工作流使用相同或等价的目标与验收标准，比较其对上下文、布局、组件、视觉风格、交互、文件可编辑性和既有设计系统的保留程度
    - 对 AI 提议作出接受、修改或拒绝的判断，说明依据；最终结果应人工检查，不以“模型已经完成”作为验收结论
4. 分析 AI 生成与修改结果：
    - 从目标与限制、视觉层级、一致性、可读性、无障碍、状态完整性、响应式表现、可维护性和交付完整性等方面检查结果
    - 使用真实内容、极端内容、不同尺寸或 Mode 验证结果；能够运行的页面可使用 Playwright 等工具辅助检查，但自动截图、像素差异或评分不能代替设计判断
    - 记录 AI 对源文件造成的非预期修改、重复图层、散落数值、组件 Detach、Token 覆盖、代码或开放文件结构变化等问题，并说明如何定位、恢复或重构
    - 分析至少一个成功案例和一个失败或不采用的案例，说明结果来自上下文质量、Prompt、工具权限、模型能力、文件格式限制还是自己的判断失误
    - 检查 AI 生成的字体、图标、图片、代码与文案是否存在来源、授权、隐私、偏见或事实性风险；无法确认时不得直接进入最终交付
5. 尝试使用他人 Skill 辅助设计：
    - 使用：
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
    - 使用符合自己审美的 Skill，完成你想完成的个人主页的某个或某些小组件，比如设计对应风格的卡片、放置对应风格的动态字体或艺术字等
    - 评判：
        - 选择至少一个边界明确的真实设计任务，保留不使用 Skill 时的 Baseline，再使用至少两个目标、产物或工作方式具有可比性的 Skill 完成相同或等价任务
        - 记录 Skill 的来源、版本或 Commit、License、适用 Agent、依赖工具、输入材料、实际调用过程与输出结果；运行第三方脚本或授予写入、联网等权限前，应先检查其说明与修改范围
        - 不以 Github Star、作者知名度、README 展示图或单次成功结果代替评判，应在相同或等价的上下文、内容和验收标准下进行对照，并区分 Skill、模型、工具权限与人工修改分别产生的影响
        - 记录你自己在使用过程中的心得体会
        - 学会客观评判设计类 Skill：
            - 鲁棒性：面对信息缺失、矛盾要求、极端内容、工具失败或无法满足的任务时，能否主动确认、合理降级并避免越界修改，而不是仅在示例输入下成立
            - 泛用性：替换主题、内容、媒介、尺寸或项目后，核心方法是否仍可复用，是否把某个案例中的文案、数值与风格误写为通用规则
            - 模型无关：是否明确依赖的模型、Agent、工具与文件格式；在可用条件允许时尝试更换模型或 Agent，检查流程能否迁移，不因 README 中的宣称直接认定其模型无关
            - 审美水平：结果能否说明构图、层级、网格、留白、字体、色彩和内容之间的关系，并在真实内容下保持清晰；不以堆叠装饰、流行风格词或一次生成的精美展示图代替审美判断
            - 风格化：能否将风格拆为可执行、可复现且与内容相符的视觉规则，在多份内容中保持辨识度与一致性，同时避免机械套版或对在世创作者风格的简单模仿
            - 模块化：目标、输入、步骤、工具调用、输出、自检和异常处理是否能够分开理解、替换与组合，局部修改是否会造成无关内容或源文件的大范围变化
            - 可维护性：指令是否清晰、篇幅与重复是否合理，示例是否服务于规则，外部依赖是否稳定，版本变化后是否容易定位、测试与更新
            - 安全与责任边界：是否合理处理权限、隐私、敏感信息、来源授权、事实核查与人工复核，是否会诱导 Agent 忽略用户要求或执行不必要的高风险操作
        - 最终形成对照结论，说明各 Skill 适合与不适合的任务、使用前提、主要风险及改进方向，而不是只给出笼统分数或主观排名
6. 尝试自己设计 Skill 辅助设计：
    - 优化已有 Skill：
        - 优化方向：
            - 从前述评判中选择一个实际使用过且问题明确的 Skill，至少针对鲁棒性、泛用性、模型无关、审美水平、风格化、模块化、可维护性或安全边界中的一项提出改进
            - 说明原 Skill 的适用范围、问题证据、希望保留的能力与本次修改边界，避免因为个人偏好将其无目标地全部重写
        - 具体措施：
            - 可通过重组步骤、补全输入与输出约定、增加上下文检查和追问条件、拆分可复用模块、减少互相矛盾或重复的指令、补充反例与极端案例、限制工具权限、增加失败处理与人工验收清单等方式进行优化
            - 保留原 Skill 的来源、版本、License 与修改说明；若包含脚本、模板或资产，应同时检查路径、依赖、敏感信息与再分发条件
            - 修改结果应是可以由他人读取和复用的完整 Skill，而不是只在一次对话中追加的临时 Prompt
        - 评估优化：
            - 使用相同任务比较原版与优化版的输入、过程、输出和人工修正成本，再使用至少一个未直接参与 Skill 改写的新内容或新场景复测
            - 根据预先写明的验收标准说明哪些问题得到改善、哪些没有改善或产生了新的副作用；保留失败结果，不为了证明优化有效而只展示最佳一次
    - 自行设计 Skill：
        - 使用 [openai/skills/skill-creator](https://github.com/openai/skills/tree/main/skills/.system/skill-creator) 辅助创建和规范 Skill：从具体使用示例出发，规划 `SKILL.md` 与必要的 `scripts / references / assets`，使用其初始化脚本建立标准目录，并在完成后运行 `quick_validate.py` 检查 Frontmatter、命名与必要字段
        - 根据任务的开放程度与出错风险，使用文字指引、参数化脚本或固定脚本设置适当的高 / 中 / 低自由度；`skill-creator` 用于建立和验证可复用工作流，不代替设计者确定目标、审美取舍、工具权限与人工验收边界
        - 从自己在 task2、task3、task4 或本次 AI 工作流中反复遇到的真实问题出发，设计一个能够辅助风格分析、方案生成、设计检查、交付整理或其他明确环节的 Skill；不应只是流行风格词和通用 Prompt 的堆叠
        - 明确 Skill 的 Purpose / Audience / Context、触发条件、适用与不适用范围、所需输入、预期输出、执行步骤、工具与权限边界、失败或停止条件，以及必须由人完成的判断
        - 将设计原则转化为可以观察和检查的规则，并提供必要的模板、示例、反例或验收清单；若依赖特定模型、Agent、插件、MCP Server 或文件格式，应明确记录而不是隐藏依赖
        - 使用真实任务运行 Skill，保留从首次版本、实际失败或偏差、人工反馈到修改版本的记录，并在新的上下文或素材上至少完成一轮复测
        - 最终产物应具有清晰的目录与说明，使未参与编写的同学能够安装或引用、准备输入、完成核心流程、判断结果是否合格，并在遇到限制时安全退出
    - 总结：
        - 设计类 Skill 的优点：
            - 分析它在外化隐性经验、稳定工作步骤、补全检查项、减少重复劳动、保持跨轮次一致性与帮助他人复用工作流等方面的实际价值，并用本次证据说明其成立条件
        - 设计类 Skill 的不足：
            - 分析上下文与模型差异、工具和文件格式限制、审美趋同、错误被流程化放大、维护成本、权限风险以及无法替代真实用户研究和人工设计判断等问题
        - 辅助风格化设计：
            - 说明如何把参考风格拆为构图、字体、色彩、形状、材质、图像处理、动效与内容语气等可执行规则，并通过 Component / Token / 模板或约束维持一致性，而不是只要求“生成某种风格”
            - 区分参考、提炼、迁移与模仿，记录参考来源、授权与人工改动；风格化不得破坏信息层级、可读性、无障碍、品牌目标和媒介限制
        - 建议对比直接 Prompt、他人 Skill、优化后的 Skill 与自行设计 Skill 的适用场景和成本，总结一份心得体会
7. 提交内容
    - 由于本次考核内容非常自由，我们推荐你在自己的 github 仓库上自行维护本次你选题所做的项目
    - 在提交到 collection-design 时，仅需带有你评测的 skill 源文件或项目地址、评测报告和心得体会
    - 对于你改进的 skill 或你原创的 skill，我们推荐你同样在自己的 github 仓库上自行维护
    - 推荐将项目链接放在提交到 collection-design 时的 README 中，也可选择在面试时自行讲解与展示
