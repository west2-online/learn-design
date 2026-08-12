# task4

## 学习

> [!TIP]
> task2 里的基础平面设计，本质上是在要你回答“如何把一张画面排得好看”
> 而从本阶段开始，你要面对的问题变成了“如何设计一个好用且可持续演进的软件页面”
> 两者最大的差别在于：画面的内容与尺寸是固定的，软件的内容、尺寸与形态却总在变化
> 因此本章不再重复那些基础概念，而是围绕这些差别组织你需要新掌握的能力

1. 从“一个画面”到“一条流程”
    - 海报上的信息一览无余，软件中的用户却要一步一步完成任务，因此需要先设计信息结构与流程，再开始画界面
    - Information Architecture / User Flow：
        - 学会利用思维导图等工具将需求拆为用户目标、入口、主路径、分支与退出条件
        - 学会从用户角度看待自己的设计，在“产品-设计-用户”间寻找平衡点
        - 先验证信息结构与任务流程，再进入高保真视觉设计
        - 补全权限、加载、空状态、错误、中断与恢复等边界流程
    - 推荐观看：
        - [设计思维天花板！这1个视频让你超越99%的设计师](https://www.bilibili.com/video/BV1p6gD65Edw/)
        - [设计稿有多惊艳，上线后就有多打脸 - 猫sir]( https://www.bilibili.com/video/BV1aA3c6JELi/)
        - etc.
2. 从“固定画布”到“弹性布局”
    - 海报尺寸一旦确定就不再变化，界面却要面对不同屏幕尺寸、内容长度、本地化文本、深浅色模式与安全区域
    - Responsive Layout：
        - 组合使用嵌套 Auto Layout、Hug / Fill / Fixed、Min / Max、Wrap 与 Constraints，让布局规则可以被他人理解和继续修改
        - 使用真实内容和极端内容进行测试，而不只让标准样例成立
3. 从“一次性设计”到“可复用系统”
    - 海报做完就结束了，界面则要应对持续的修改、复用与交接，需要把重复出现的元素沉淀为组件与系统
    - Component System：
        - Main Component / Instance / Nested Instance：理解组件继承、Override 与 Detach 的使用边界
        - Variants：使用 Type / Size / State / Theme 等相互独立的属性描述组件
        - Component Properties：Text / Boolean / Instance Swap / Slot
        - Interactive Components：将常见交互与状态变化封装进组件
    - Design System：
        - Styles / Variables / Collections / Modes：区分样式、原始值与语义 Token
        - Primitive -> Semantic -> Component Token：避免在业务界面中直接使用散落数值
        - 使用 Modes 管理 Light / Dark、多品牌、多语言或不同设备下的取值
        - Typography Token：将字族、字重与字号阶 Token 化，数字场景使用等宽数字（tabular figures），并考虑系统字体栈、回退链与字体嵌入授权
        - 为 Component / Token 建立命名、说明、使用边界与 Deprecated 策略
        - Library：发布、Review、更新与记录变更，理解更新对下游文件的影响
4. 从“静态呈现”到“可感知交互”
    - 海报的信息是静态的，界面则需要通过状态变化与反馈告诉用户发生了什么、接下来能做什么
    - Prototyping：
        - Flow Starting Point / Navigate / Back / Scroll to / Overlay：组织完整任务流
        - Interactive Components：覆盖 hover / focus / pressed / disabled 等状态与过渡
        - Variables / Expressions / Conditionals / Multiple Actions：表达输入、判断、计数与分支结果
        - Smart Animate / Easing / Duration：让动效说明层级、方向、因果与反馈，而不是只作装饰
        - 使用尽量少且可维护的 Frame 表达完整交互，避免难以修改的连线网络
5. 从“交付即完成”到“验证与迭代”
    - 海报印出来就算完成，界面好不好用却需要真实用户来验证，再根据问题修改并复测
    - UX 验证与迭代：
        - 为 Prototype 编写真实任务与观察目标，邀请目标用户完成而不是只观看演示
        - 检查任务是否易发现、状态是否易理解、反馈是否及时、软件内流程是否闭环
        - 检查键盘操作、Focus、触控目标、色彩对比与缩放后的可用性
        - 考虑目标群体用户的习惯，多适应用户，少明显引导
6. 从“个人作品”到“团队协作”
    - 海报可以一个人完成，软件则需要与实现侧及其他成员交接，文件结构本身就是交付的一部分
    - Collaboration / Handoff：
        - 使用 Pages / Sections / 命名规则 / Comments / Version History 维持文件可读性与协作上下文
        - 使用 Dev Mode 或通过 Annotations / Export Settings 交付规格、状态、资产和交互说明
        - 与实现侧对齐 Component / Token 命名及代码映射，并在多尺寸和真实内容下进行验收
    - 插件与 Community 资源：
        - 根据真实问题选择插件，检查来源、权限、维护状态、套餐限制与 License
        - 理解插件的输入、输出与修改范围，对生成结果进行人工检查
        - 插件用于加速重复工作，不代替设计判断与可维护的文件结构
7. etc.

参考样例：

- [Figma Learn](https://help.figma.com/hc/en-us): Figma 官方文档与教程
- etc.

推荐关注:

- [猫sir不吃鱼](https://space.bilibili.com/3537108423674097)
- etc.

## 作业

1. 在 Figma 中完成真实软件场景的 UI / UX 设计，可从如下方向中自行选题：
    - 优化你认为需要优化的应用场景的对应软件
    - 自行寻找或虚构一个应用场景的对应软件
    - 该软件界面可以是任意类别：
        - Web 端界面
        - 客户端界面
        - 小程序界面
        - 游戏内界面
        - 特定嵌入式软件界面：
            - 公司打卡
            - 摄影软件
            - etc.
        - etc.
    - 选题需具有明确的目标用户、使用环境与核心任务，能够支持从进入软件到完成任务并得到结果反馈的完整流程；不建议只完成登录页、展示页或彼此无关的界面集合
    - 若优化已有软件，需记录原流程、实际体验或用户反馈中存在的问题，说明哪些部分保留、哪些部分调整以及理由；若虚构软件，需明确需求假设、业务规则与本次设计边界
    - 不要求页面数量越多越好，应根据核心任务与必要边界状态决定范围，优先保证一个主要流程完整、可交互、可验证
2. 除 task2 中学到的知识外，你还需要展示的能力如下：
    - 前期构思：
        - 明确 Purpose / Audience / Context：软件需要解决的问题、目标用户、使用场景、设备与输入方式、业务目标以及必要限制
        - 通过访谈、问卷、观察、应用商店评论、竞品分析或公开资料等适合选题的方法收集依据，区分事实、他人反馈与自己的假设
        - 利用思维导图等工具将需求拆为用户目标、入口、主路径、分支与退出条件
        - 确认权限、加载、空状态、错误、中断与恢复等边界流程
        - 尝试优化期望业务流程到用户友好的高效率动线上，以此为基础进行页面分级
        - 考虑目标群体用户的习惯，多适应用户，少明显引导
        - 在进入高保真设计前，完成 Information Architecture、User Flow 与低保真原型，先确认信息结构、操作顺序和页面之间的关系
        - etc.
    - 中期设计：
        - 弹性适配不同屏幕尺寸、确保高低亮度、亮暗模式下的可读性
        - Responsive Layout：
            - 组合使用嵌套 Auto Layout、Hug / Fill / Fixed、Min / Max、Wrap 与 Constraints，让布局规则能够被他人理解和继续修改
            - 使用真实内容与极端内容检查长文本、本地化文本、图片比例变化、数据为空或过多、安全区域等情况，不应只让标准样例成立
        - Component System：
            - 使用 Main Component / Instance / Nested Instance 组织重复界面，合理使用 Override，避免为了局部修改大量 Detach
            - 使用 Type / Size / State / Theme 等相互独立的 Variants 与 Text / Boolean / Instance Swap / Slot 等 Component Properties 表达组件差异
            - 为输入、选择、导航、反馈等重要组件补全 default / hover / focus / pressed / disabled / loading / error 等与场景有关的必要业务状态及其间过渡态
        - Design System：
            - 使用 Styles / Variables / Collections / Modes 管理颜色、字体、间距、圆角等规则，区分 Primitive、Semantic 与必要的 Component Token
            - 为 Component / Token 使用语义清晰的命名，记录用途、使用边界与必要的变更说明；业务界面中不应散落大量无规律数值
            - Typography Token 需说明字族、字重与字号阶的定义，数字场景的等宽数字（tabular figures）处理，以及跨端字体回退策略
            - 设计系统的规模以本项目实际使用为准，不要求为了数量制作与项目无关的组件
        - Prototyping（原型动画，UX 初步）：
            - Flow Starting Point / Navigate / Back / Scroll to / Overlay：填充完整任务流
            - 可交互组件要覆盖 hover / focus / pressed / disabled 等常见状态及其间过渡态
            - Variables / Expressions / Conditionals / Multiple Actions：表达输入、判断、计数与分支结果
            - Smart Animate / Easing / Duration：让动效说明层级、方向、因果与反馈，而不是只作装饰
            - 使用尽量少且可维护的 Frame 表达完整交互，避免难以理解与维护的连线网络
        - 使用 Pages / Sections / 图层命名与必要注释组织需求、草稿、组件、正式界面和交付内容，删除或归档无意义的重复版本，使其他成员能够快速理解文件
        - 根据真实问题选择插件与 Community 资源，检查来源、权限、维护状态、套餐限制与 License，并人工检查插件生成或修改的结果
        - etc.
    - 后期验证与交付：
        - UX 验证与迭代：
            - 为 Prototype 编写接近真实场景的任务和观察目标，邀请目标用户或符合目标用户特征的同学直接完成任务，而不是先讲解操作方法或只让其观看演示
            - 检查任务是否易发现、状态是否易理解、反馈是否及时、软件内流程是否闭环
            - 检查键盘操作、Focus、触控目标、色彩对比与缩放后的可用性
            - 记录测试者的操作路径、停顿、误解、失败与反馈，区分观察事实和自己的解释，并根据较重要的问题至少完成一轮修改与复测
            - 在目标设备或合理模拟环境中，使用多种尺寸、真实内容和极端内容验收主要流程与边界状态
        - 项目交付：
            - 使用 Dev Mode 或通过 Annotations / Export Settings 交付规格、状态、资产和交互说明
            - 与实现侧对齐 Component / Token 命名及代码映射，并在多尺寸和真实内容下进行验收
            - 对无法仅从界面看出的业务规则、响应式变化、动效、错误处理和资源使用方式补充说明，使实现侧不需要猜测关键设计意图
    - etc.
3. 提交内容：
    - 一份涵盖可正常访问并具有查看权限的 Figma 链接的 README，说明选题背景、目标用户、核心任务、项目范围、文件结构、Prototype 入口、建议体验顺序、主要设计取舍以及如何查看和复用本项目等关键信息
    - 前期调研与问题定义记录；优化已有软件时需附原流程或原界面分析，虚构软件时需附需求假设与业务规则
    - 完整表示核心任务及必要边界状态的 Prototype 的思维导图；可附关键界面预览图，必要时可增加简短录屏帮助审核者理解交互
    - 简单记录你设计的 UX 测试任务、观察记录、发现的问题、修改前后对照与复测结论
    - 资产与第三方内容清单，记录字体、图标、图片、插件、UI Kit、Community 文件等内容的来源、授权与修改情况，并区分原创、修改和引用的部分；字体需额外说明嵌入与分发授权
    - Figma 需保证链接权限长期有效，并通过 README、预览图与必要导出内容保留能够被审核和回溯的版本证据
