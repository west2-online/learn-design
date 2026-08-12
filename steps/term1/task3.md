# task3

## 学习

### 公众号排版工作流

> [!TIP]
> 公众号等封闭平台上的内容排版，与网页设计其实高度相似，本质上都是“内容 + 样式”的结构
> 因此本阶段真正要学的，不是某一篇文章怎么排，而是如何把内容与样式分离，让排版规则可以被复用、被检查、被交接

1. 认识 [doocs/md](https://github.com/doocs/md)
    - 本次任务的主要排版工具，先阅读其 [README](https://github.com/doocs/md#readme)、[LICENSE](https://github.com/doocs/md/blob/main/LICENSE) 与主题相关说明
    - 了解它帮你真实完成的流程：
        - Markdown Parser：[markdown-it](https://github.com/markdown-it/markdown-it)
        - 中间层：AST/HTML + Theme Renderer
        - WeChat Adapter：HTML + Inline CSS
    - 工作流起始点是 Markdown，但可能的源文件有docx / txt / pdf / etc.
    - 交付方式：Draft API / 手动复制粘贴到微信公众号后台
2. 运行与自托管
    - 选择 Node.js 或 Docker 任一流程在本机运行：
        - [Node.js](https://nodejs.org/)
        - [Docker](https://docs.docker.com/) / [菜鸟教程/Docker教程](https://www.runoob.com/docker/docker-tutorial.html)
    - 借此了解开源项目自托管的好处与代价，不必迷信某一种部署方式
3. License
    - 了解常见开源协议的区别，可参考 [Choose an open source license](https://choosealicense.com/)
    - 记录第三方代码与资产的来源和授权，学会区分原创、修改与引用的部分
4. etc.

### 排版基础

1. CSS 基础
    - 主题本质上是一组 CSS 规则，通过选择器与 Markdown 解析出的 HTML 结构建立映射，最终被转换为微信公众号支持的 Inline CSS
    - 推荐自选其一阅读：
        - [菜鸟教程/CSS教程](https://www.runoob.com/css/css-tutorial.html)
        - [MDN/CSS](https://developer.mozilla.org/zh-CN/docs/Learn/CSS)
        - etc.
    - 推荐关注：
        - [zhangxinxu](https://space.bilibili.com/31556431)
        - [林想的Web工坊](https://space.bilibili.com/847346)
    - 推荐观看:
        - [合集·CSS 创意实战「无废话 CSS」](https://space.bilibili.com/847346/lists?sid=6848229)
2. 字体选型
    - 衬线 / 无衬线对长文阅读的影响，正文与标题字体的分工
    - 中英文混排的字体选择与回退
    - 公众号等平台对字体的限制（仅系统字体或图片字）本身就是一个真实的 Context 约束
    - 推荐阅读：
        - [MDN/font-family](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-family): 系统字体栈与回退链
        - [Google Fonts](https://fonts.google.com/): 开源字体
        - etc.
3. SVG 矢量图形
    - 标题符号、分隔装饰、背景图形等适合矢量表达的部分，应制作或重构为 svg 而非截图
    - 需要理解 `viewBox`、`path` 与 `fill / stroke`，使颜色、尺寸和描边便于主题复用
    - 相关的工作流，你可以使用 figma，其导出的格式可以是标准 svg；也可以选择性学习一下 Inkscape 这种老牌 svg 编辑器
    - 推荐自选其一阅读：
        - [菜鸟教程/SVG教程](https://www.runoob.com/svg/svg-tutorial.html)
        - [MDN/SVG](https://developer.mozilla.org/zh-CN/docs/Web/SVG)
        - etc.
4. 图床
    - 公众号插图需要公网可访问的图片地址，因此需要图床
    - 推荐：
        - [PicGo](https://github.com/Molunerfinn/PicGo)
        - [SM.MS](https://sm.ms/)
        - etc.
    - 图床不保证永久可用，重要图片仍需在仓库中保留可回溯的副本
5. etc.

## 作业

1. 搭建公众号排版工作流：
    - 使用 [doocs/md](https://github.com/doocs/md) 作为本次任务的主要排版工具，阅读项目的 README、LICENSE 与主题相关说明
    - 根据自己的设备完成本地配置与运行，可选择项目支持的 Node.js 或 Docker 流程，简单记录所用版本、环境、启动步骤、遇到的问题与解决结果
    - 建立从 `原始文稿 / Markdown -> Theme 模板 -> 预览与检查 -> 交付文件` 的完整流程
        - 理解 Markdown 被解析为 HTML、主题选择器匹配内容结构、CSS 被转换为适合微信公众号的样式这一基本过程，能够判断问题来自内容、模板、资产还是平台转换
        - 将 Markdown 作为内容层，将 CSS 作为视觉规则，将 SVG 作为可复用的图形与装饰资产；修改文章内容时，不应重新逐段设置样式
2. 临摹已有的公众号文章，提取主题：
    - 自选你认为有临摹价值的公众号文章排版进行临摹，包括但不限于以下文章：
        - 西二在线服务号
            - [2025纳新｜西二在线：希望你比冬天先来](https://mp.weixin.qq.com/s/XOk5er1MXPWK2e_0msGJUQ)
            - [重生归来，这一次我选择“福uu”作为我的解药](https://mp.weixin.qq.com/s/sVEgk2TF0jYHxsm0-nXLzw)
            - etc.
        - 福州地铁公众号
            - [福州首个地铁站内匹克球馆来了！就在滨海快线南公园站！](https://mp.weixin.qq.com/s/h5NFG53c7RnFoEIZXQuiLA)
            - [榕榕×闽超五福天团双IP联动！“闽超”观赛福利来啦！ | “茉莉服务”⑦](https://mp.weixin.qq.com/s/J3v-i2yNCvEbimHz9tmUyA)
            - etc.
        - etc.
    - 分析参考主题的字号、字重、行高、段间距、颜色、留白、分隔方式、图片规则和阅读节奏，再开始编写样式
    - 至少覆盖标题、二级与三级标题、正文、强调、引用、列表、链接、图片、图片说明、分隔线和文末信息，表格和代码块也需额外注意
    - 使用 CSS 建立元素与样式的稳定映射，避免依靠大量空行、空格、逐段内联样式或只对当前文章有效的选择器完成视觉还原
    - 对参考主题中的边框、标题符号、分隔装饰、背景图形等视觉元素进行拆解，并将适合矢量表达的部分制作或重构为 SVG
    - SVG 应具有正确的 `viewBox`、合理的路径与图层结构，颜色、尺寸和描边应便于主题复用；不得提交不可编辑的截图代替可维护的图形资产
    - 临摹的目标是理解主题的构成与实现方式，而不是宣称原创；需保留参考公众号、对应文章链接、截图和分析记录，不得擅自将其品牌标识或专属资产用于对外发布
3. 尝试优化或重新设计公众号主题：
    - 以临摹成果为起点，指出原主题在可读性、一致性、复用性、实现方式或适用场景上的具体好处与不足
    - 可以在保留原主题视觉方向的基础上进行优化，也可以重新设计一套符合自己审美的主题，但必须说明目标读者、使用场景、视觉方向和主要取舍
    - 建立有限且用途明确的 Typography、Color、Spacing、Radius、边框和装饰规则，使主题能够通过统一变量或集中配置进行调整；其中 Typography 规则需说明正文与标题字体的选择依据与备选方案，以及中英文混排时的回退策略
    - 将高频装饰和结构整理为可复用的 CSS / SVG 模块，避免将只适用于某一句文案、某一张图片的偶然结果包装成主题能力
    - 使用与第一阶段相同的测试文稿生成对照预览，展示临摹版本与优化或重设计版本之间的差异，并说明每项主要变化解决了什么问题
    - 在至少两种移动端宽度下检查长标题、连续英文或链接、列表嵌套、横图、长图、多段正文和字体回退表现，确保没有明显的横向溢出、异常空白、样式丢失或阅读困难
    - 主题建议优先满足真实社团或学校推文的稳定编辑需求，不以装饰数量、视觉复杂度或与参考截图的像素一致性作为目标
4. 提交内容：
    - 至少包括：你临摹的公众号链接、统一测试文稿、临摹主题、优化或重设计主题、CSS、可编辑 SVG、主题所需资产、两阶段预览图、参考分析与工作记录
    - 提供 README，说明目录结构、环境要求、启动方式、主题使用方法、常见内容如何套用、如何替换颜色与 SVG，怎样交付结果等必要说明
    - README 中需记录参考公众号与文章、第三方代码和资产的来源及授权，并说明临摹内容只用于学习与考核；应区分原创、修改和引用的部分
    - 注意 `.gitignore` 的规范性，不提交依赖目录、构建缓存、无必要的重复导出文件、账号密码、Cookie、Token、`.env` 或微信公众号后台凭据；图床与 Draft API 等外部服务应使用占位配置或环境变量说明
