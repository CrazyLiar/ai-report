# AI / Agent 趋势周报｜2026-W46

- 精确新闻覆盖：2026-11-08 20:00:00（不含）至2026-11-15 20:00:00（含），Asia/Shanghai。
- 本周日20:00之后的信息不在本次覆盖内，启动延迟不改变截止时间。
- 近30天背景：2026-10-16 20:00:00至2026-11-15 20:00:00；背景与本周变化分别标注。
- 实际生成时间：2026-11-15 20:06:33（Asia/Shanghai）。
- 方法与边界：本期独立中英文检索、打开原始来源，不拼接日报；日期以官方首次公告为准。多数页面未给时区及时分秒，无法精确换算北京首发时刻；本期主要事件在11月9—14日，无需依赖周日日期推定是否入窗。未实测产品、性能或安全结论，厂商指标均不作独立验证。

## 核心判断

**分析：本周更强的信号是，Agent开始围绕“持续修改的共同成果”和“可治理的执行流程”组织产品。** 模型性能与价格仍重要，但用户能否接着编辑、审批、追踪并撤回行动，正在成为工程竞争点。共享白板和表格扩大入口，工具与编排缩短集成链路，部署和停机控制则决定这些能力能否进入真实业务。现有证据支持小范围实践，尚不足以支持全面无人值守或整体迁移技术栈。

## 本周五个相互关联的变化

### 1. 协作成果成为工作入口

**11月10日：Claude Whiteboards、Sheets以beta推出，Dashboards更名为Claude Data并正式可用；其中认证查询、实时共享仍为beta。** 白板、表格允许人与Claude继续修改同一份成果，Sheets目前功能较基础；互动连接器让第三方完整应用在对话旁打开。[产品公告](https://claude.com/resources/articles/sheets-whiteboards-data) · [连接器公告](https://claude.com/resources/articles/interactive-connectors-full-tool)

**11月11日：Google Tabletop以Labs实验推出实时群组协作；11月10日Adobe发布Firefly Graph beta，Builder为私测。** 前者扩展共同规划入口，后者把创作流程做成可重复执行的图。[Tabletop](https://blog.google/innovation-and-ai/models-and-research/google-labs/tabletop/) · [Adobe公告](https://news.adobe.com/news/2026/11/adobe-firefly-expands)

**分析：** “生成一份答案”正扩展为“维护共同工作对象”。开发者要补版本、多人权限、修改归属和导出能力；不能把beta演示当作完整办公软件替代。这一变化与模型榜单同样重要，因为它直接改变分发入口及用户工作方式。

### 2. 模型选择更适合按任务成本衡量

**11月9日：Claude Fable 5.2正式可用，Mythos 5.2仍需验证项目准入。** 官方列标准价格为每百万输入/输出token 8/40美元，速度改善是厂商测试结论。**11月12日：Gemini 4 Hydrogen正式可用，价格为1.5/7.5美元，支持100万token上下文；11月10日Carbon扩大可用范围。** [Claude公告](https://www.anthropic.com/claude-fable-and-mythos-5-2) · [Gemini API日志](https://aistudio.google.com/docs/changelog) · [Carbon公告](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-carbon-now-available/)

**分析：** 同为token标价，实际完成成本还受思考预算、重试、工具调用及失败率影响。应比较同一批任务的验收通过率、总费用和耗时，再决定是否路由到不同模型；不能把更便宜的单价直接解释成更便宜的业务结果。

### 3. 长时运行开始补齐状态与部署边界

**11月12日：自托管Claude Managed Agents进入私测。** 团队可在自己环境运行执行框架、凭据及会话历史，模型请求仍发送到选定提供商，并非离线模型。**11月13日：Antigravity v2.32.0分批推出Dynamic Workflows，用Python组织顺序或并行子Agent；DeepSeek正式开放应用API，由服务端处理部分搜索、文件和链接调用。** [自托管公告](https://claude.com/resources/articles/self-hosted-claude-managed-agents) · [工作流日志](https://antigravity.google/docs/changelog) · [DeepSeek日志](https://api-docs.deepseek.com/updates/)

**分析：** 执行框架负责模型循环、工具、状态和权限，减少自建代码也会改变故障归属。重点能力是事件去重、断点恢复、幂等写入与调用追踪。幂等意味着重复请求不会重复造成业务副作用；增加子Agent数量不能替代这些基础。

### 4. 有权行动之后，授权与停止成为产品能力

**11月13日：ChatGPT Wallet限定向美国Pro用户推出，每次购买需审阅并安全验证。11月9日：OpenAI披露已部署的内部Control Room，称接到停机决定后最多35秒阻止进一步模型输出；这不是公开停机服务，也不等于撤回既有外部操作。** [Wallet](https://openai.com/index/introducing-chatgpt-wallet/) · [Control Room](https://openai.com/index/control-room/)

**11月9日Fireworks更新10月安全事件，确认新增账户、账单及部分客户数据影响；属旧事件实质进展。** [安全公告](https://fireworks.ai/security/bulletins/october-2026-security-incident-update)

**分析：** 最小权限、逐笔授权、凭据隔离与紧急停止须落实在系统层。供应商的零保留或安全声明有具体适用范围，不能自动覆盖开发环境、日志及所有第三方链路。

### 5. 开源底座开始强调接口与数据传递契约

**11月13日：llama.cpp v1.0.0正式发布，删除35个弃用函数，并增强服务器安全与缓存支持。11月10日：MCP文件传输扩展公开探索，仍属实验草案，没有参考实现。** MCP是连接AI与工具的协议；该扩展尝试让文件直接传到目标，避免模型搬运全部字节。[版本记录](https://github.com/ggml-org/llama.cpp/releases/tag/v1.0.0) · [MCP原文](https://blog.modelcontextprotocol.io/posts/exploring-file-uploads-and-downloads-in-mcp/)

**分析：** 可维护性取决于版本兼容、传输授权、取消与失败恢复。已有llama.cpp集成应检查弃用接口；MCP草案适合跟踪和试验，不能先当跨客户端通用能力承诺。

## 趋势强弱与需要修正的判断

**增强：** 人与Agent围绕共享成果协作；执行、身份和状态成为一体化工程问题。**减弱：** 用单次榜单、单价或“多Agent”标签推导整套产品优势的解释力。**待验证：** 长任务成功率、跨工具权限一致性，以及多模型路由扣除调度成本后的净收益。

**近30天背景，非本周新闻：** 10月25日研究预印本[Memory Tax](https://arxiv.org/abs/2610.34073)指出，部分记忆系统在其测试中不如直接检索原始历史。记忆整理可能丢失证据；RAG即先检索材料再生成答案。应修正“记忆越复杂越好”的判断，但该研究也不证明所有复杂记忆无用。

算力侧，**11月9日Google公布TPU 8tx、8i Max系统配置**，不是首次发布第八代芯片；10月27日[Cerebras与Oracle合作](https://investors.cerebras.ai/news-releases/news-release-details/cerebras-and-oracle-team-bring-cerebras-ai-inference-oracle)是背景，不能因本周财报再当新合作。[TPU公告](https://cloud.google.com/blog/topics/ai-infrastructure/tpu-8tx-and-tpu-8i-max)显示长上下文和机密推理需求受到重视，尚不能推出应用成本必然下降。

## 未来3—6个月：条件性预测

- **协作成果会成为更多Agent应用的默认入口，信心中高。** 依据是多家独立产品方向趋同；条件是编辑、分享和权限足够可靠。若留存、团队复用或导出兼容性持续差，应下调判断。
- **按任务路由模型会增加，信心中。** 条件是同任务评测证明确有净节省；若协调、重试和延迟抵消单价优势，单模型方案仍更合适。
- **治理与评估能力会更影响工程交付，信心中高。** 依据是自托管、停机及安全事件；若这些能力只能停留在私测、无法稳定接入现有系统，普及速度将低于预期。这是技能价值分析，不是已验证的岗位增量统计。

## 下周行动：用3小时验证可追溯的共同成果

**立即实践：** 使用现有工具和虚构数据，完成一个“5条事件→共享任务表”的小流程。约45分钟定义字段与验收，75分钟实现，60分钟测试。每行保留来源、状态、修改者与审批记录；同一事件重复输入不得新增重复任务，未经批准不得对外写入。

**交付物：** 一张可编辑任务表、流程说明和测试记录。**验收：** 5条事件均可追溯；重复输入零重复；一次拒绝审批和一次失败重试均有记录；人工修改能保留。加入学习计划的是状态机、权限、观测和同任务成本评测；仅观察私测平台、硬件迁移及未定稿协议，不急于购买或换栈。

**反证检查：** 本周证据偏产品与厂商测试，缺少长期独立可靠性、真实留存、完整成本及系统岗位样本；监管地区差异也可能改变部署选择。信息足够支持上述低成本实验，不足以支持扩大自主付款、全面无人值守或重大基础设施迁移。

<!--
公共检索审计（不计正文目标字数）
独立检索本周及近30天背景，先发现再比较后成稿；成稿前重访OpenAI、Claude产品、DeepMind、MCP与llama.cpp发布索引，并以独立中英文资讯查漏。后读11月15日日报审计重评排除项，未用日报入选项限定候选。
实际查询：
AI week November 9 15 2026 agent models releases collaboration workspace
2026年11月 AI 9日 15日 白板 表格 Claude Sheets Data 智能体 周报
November 2026 AI inference chips regulation agent memory RAG evaluation November 13
site:claude.com "Introducing Claude Whiteboards"
site:deepmind.google "November" "2026" "Hydrogen"
AI workspace collaboration artifacts whiteboards sheets data connectors November 2026
2026年11月 AI 开源 训练 推理 芯片 监管 评估 智能体
site:fireworks.ai November 9 2026 security incident billing
site:cerebras.ai November 2026 Q3 Oracle
site:digital-strategy.ec.europa.eu November 2026 AI Act
November 2026 agent memory RAG evaluation research github 9 15
site:labs.google Tabletop November 2026
site:blog.google Tabletop November 2026
site:elevenlabs.io/blog ElevenAI November 11 2026
site:adobe.com November 10 2026 Firefly Design Graph MCP Creative Agent
2026年11月15日 本周 AI 应用 工作台 模型 监管 新发布
AI November 15 2026 weekly agents collaboration open source news
site:github.com/ggml-org/llama.cpp "v1.0.0" "Nov"
site:cloud.google.com/blog November 2026 eighth generation TPU
site:blog.cloudflare.com "Kitesurf"
site:cloud.google.com/blog "November 10, 2026" "Kubernetes" "reinforcement"

实际成功访问的官方索引：
https://openai.com/news/ （成稿前另访?display=list）
https://www.anthropic.com/news
https://claude.com/resources/articles （成稿前复查）
https://deepmind.google/blog/ （成稿前复查）
https://blog.google/innovation-and-ai/
https://ernie.baidu.com/research/
https://api-docs.deepseek.com/updates/
https://blog.modelcontextprotocol.io/ （成稿前复查）
https://huggingface.co/blog
https://blogs.nvidia.com/
https://investors.cerebras.ai/
https://www.langchain.com/blog
https://aistudio.google.com/docs/changelog
https://github.com/microsoft/agent-framework/releases
https://github.com/langchain-ai/deepagents/releases
https://github.com/ggml-org/llama.cpp/releases
https://github.com/openai/codex/releases
https://github.com/anthropics/claude-code/releases
https://antigravity.google/docs/changelog
原始正文均使用下面候选链接实际打开核实，而非搜索摘要充当打开成功。GitHub部分Compare控件有加载错误，但正文版本记录可读取，不等于整页失败。

关键候选与比较表：
事件 | 首发日期/北京时间 | 状态 | 原始链接 | 实质变化/影响维度 | 决定及理由
Claude Whiteboards/Sheets/Data | 11月10日，原页无时区/时刻，无法精确换算北京首发时刻 | 两项beta；Data正式，部分新功能beta | https://claude.com/resources/articles/sheets-whiteboards-data | 同一成果可多人持续编辑，改变工作方式 | 入选主线1；不被模型榜单挤占，注意Data正式不等于全部新功能正式
Claude互动连接器 | 11月10日，时区时刻未给 | 产品更新 | https://claude.com/resources/articles/interactive-connectors-full-tool | 应用完整界面嵌入，改变集成与入口 | 合并主线1，避免同日组合发布拆多条
Tabletop | 11月11日，时区时刻未给 | Google Labs实验 | https://blog.google/innovation-and-ai/models-and-research/google-labs/tabletop/ | 群组实时共同规划 | 合并主线1，独立验证跨产品协作趋势，非成熟通用办公套件
Adobe Firefly Graph/Builder | 11月10日09:00，页面未给时区，不擅自换算 | Graph beta；Builder私测 | https://news.adobe.com/news/2026/11/adobe-firefly-expands | 可重复创作流程与原型入口 | 合并主线1，仅取已核实状态，非所有工具正式发布
Fable/Mythos5.2 | 11月9日，时区时刻未给 | Fable正式；Mythos验证准入 | https://www.anthropic.com/claude-fable-and-mythos-5-2 | 技术能力与价格边界 | 入选主线2，区分开放范围与厂商测试；不用图表分数直接推导迁移
Carbon扩大可用范围 | 11月10日，时区时刻未给；先前受限发布另属背景 | 扩大开放 | https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-carbon-now-available/ | 高难度长任务 | 合并主线2，不把10月首次受限公告重复当本周首发模型
Hydrogen | 11月12日首次，文章11月13日更新，时区时刻未给 | API正式GA | https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-hydrogen/ ; https://aistudio.google.com/docs/changelog | 快速执行与上下文/定价 | 合并主线2，用API日志核实GA；调度收益仍是厂商测试
自托管Managed Agents | 11月12日，时区时刻未给 | 私测 | https://claude.com/resources/articles/self-hosted-claude-managed-agents | 自主部署控制面、凭据历史 | 入选主线3；不能叫完全离线
Dynamic Workflows | 11月13日，时区时刻未给 | v2.32.0发布/渐进推出 | https://antigravity.google/docs/changelog ; https://antigravity.google/docs/dynamic-workflows | Python显式编排与结构化子Agent | 合并主线3；重评日报补遗，周内正常事件，不用转载日期
DeepSeek应用API | 11月13日，时区时刻未给 | 正式开放API | https://api-docs.deepseek.com/updates/ | 服务端搜索文件链接集成 | 合并主线3；不视为新底模或降价
Always-on Agent | 11月13日，时区时刻未给 | 工程指南 | https://claude.com/resources/articles/building-always-on-agents | 收件箱、计时、记忆、权限、发件箱 | 合并主线3工程判断；重评日报排除，不将指南当新模型能力
ChatGPT Wallet | 11月13日，时区时刻未给 | 限定推出 | https://openai.com/index/introducing-chatgpt-wallet/ | 逐笔授权支付 | 入选主线4；不扩大成任意自主付款
Control Room | 新闻索引11月9日，时区时刻未给 | 内部系统已部署/工程披露 | https://openai.com/index/control-room/ | 推理入口授权与停止输出 | 合并主线4；35秒非通用外部动作回滚保证
Fireworks事件进展 | 原事件10月；11月9日公告更新，时区时刻未给 | 供应商调查披露，仍在调查 | https://fireworks.ai/security/bulletins/october-2026-security-incident-update | 新增数据影响，供应链权限风险 | 合并主线4，明确旧事件实质进展，不概括所有推理数据均泄露
llama.cpp v1.0.0 | 11月13日10:20（发布页未显式展示时区，未推断北京时刻） | 正式版本 | https://github.com/ggml-org/llama.cpp/releases/tag/v1.0.0 | 弃用API删除、安全/缓存维护 | 入选主线5，精确版本页优于滚动列表，提示已有集成检查
MCP文件传输 | 11月10日，时区时刻未给 | 实验草案，无参考实现 | https://blog.modelcontextprotocol.io/posts/exploring-file-uploads-and-downloads-in-mcp/ | 文件数据不必由模型搬运，传输授权 | 合并主线5，非已定稿标准，不将年末计划当保证
ERNIE5.5FlashPreview | 索引11月11日，时区时刻未给 | 后训练中间检查点预览，权重开源仍是计划 | https://ernie.baidu.com/release/ernie-5-5-flash-preview/ | 中文模型、百万上下文、多模态演示 | 不单列；主线2已有更直接可用价格/路由证据，不能把演示当成熟能力、预告权重当已下载
ERNIE Evolve | 索引11月9日，时区时刻未给 | 研究/厂商结果 | https://ernie.baidu.com/research/posts/ernie-evolve/ | 独立评价筛选代码改进，训练及推理优化 | 未入五主线，工程价值高但仍需独立复现；不是所有任务递归自改进成立
ElevenAI | 11月11日，时区时刻未给 | 预览/早期访问 | https://elevenlabs.io/blog/nyc-summit | 会议转行动、语音入口 | 未单列，协作入口已由主线1覆盖，语音同意机制值得后续跟踪
Claude Meetings | 11月12日，时区时刻未给 | beta | https://claude.com/resources/articles/claude-meetings | 会议记录与工作成果 | 与协作主线相关但未单列，避免同厂商占满；不沿用11月10日预告作正式开放日期
Goal Engineering | 11月14日，时区时刻未给 | 工程观点/案例 | https://www.langchain.com/blog/goal-engineering | 按反馈可复用性划分任务 | 不单列，非受控实证；其反馈取向支持实践设计，不能宣告上下文工程过时
Agent Framework1.26.0 | 11月13日，发布页08:28，时区未单独核实 | 库发布/部分实验功能 | https://github.com/microsoft/agent-framework/releases | 输出契约、权限中间件、Hyperlight取消/预算 | 未单列，主线3/5已有代表；现有用户应读破坏兼容变化，非推荐换框架
Deepagents/Modal、Codex、ClaudeCode | 本周各版本见发布页，未逐版本换算时区 | 正式与alpha分开 | https://github.com/langchain-ai/deepagents/releases ; https://github.com/openai/codex/releases ; https://github.com/anthropics/claude-code/releases | 集成与修复 | 重评日报排除项，周报不因日报“旧日期”排除；比较后仍未单列，修复多而对本周核心判断增量较小
Kitesurf开源 | 11月13日由官方作者索引检索指向，正文未显式提供首发时刻 | Apache2.0开源 | https://blog.cloudflare.com/kitesurf-open-source/ | Workers上的Agent浏览器，部署入口 | 读原文确认开源，未入主线；兼容性和真实任务覆盖未测，不能当完整Chromium替代
TPU8tx/8iMax | 11月9日，时区时刻未给 | 系统公告/性能厂商宣称 | https://cloud.google.com/blog/topics/ai-infrastructure/tpu-8tx-and-tpu-8i-max | 长上下文和机密推理配置 | 简短算力信号，明确不是首次第八代芯片；不推断应用降价，不建议买硬件
Kubernetes开放AI原生栈 | 11月10日，时区时刻未给 | 项目组合/工程发布，组件成熟度各异 | https://cloud.google.com/blog/topics/developers-practitioners/the-open-ai-native-stack-on-kubernetes-from-open-models-to-distributed-inference-and-agents | 后训练、分布式推理与Agent执行整合 | 未单列，对已运营大集群者重要；不由平台文章泛化全部开发者需要Kubernetes
Cerebras-Oracle | 10月27日，时区时刻未给 | 合作公告/未来交付安排 | https://investors.cerebras.ai/news-releases/news-release-details/cerebras-and-oracle-team-bring-cerebras-ai-inference-oracle | 算力供给入口 | 近30天背景，财报重提不是本周新合作
Memory Tax | 10月25日05:29:05 UTC＝北京时间13:29:05 | 研究预印本，非本周 | https://arxiv.org/abs/2610.34073 | 记忆整理收益与证据损失 | 近30天背景，修正复杂记忆必优判断，不泛化全部记忆方案
欧盟AI Act | 本次读官方持续更新页，未确认本周新法案里程碑 | 现行监管说明 | https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai | 风险分级/部署约束 | 背景检查，不虚构本周监管新闻；不提供具体合规法律结论

媒体社区路径：中英文搜索实际发现IT之家、AI拍档、TechRadar、New Runtime、AI Atlas、Agentic Weekly、AIMap、AppliedModels等线索。未把它们的摘要当正文原始核验。特别用跨领域汇总发现Tabletop、Adobe、Kitesurf、llama.cpp、TPU系统等，再打开原始页，改变候选池而非只验证预先选定大厂。
反向检查：Claude产品索引实际显示11月10日组合发布；与11月11日中文转载分开；Sheets/Whiteboards beta、Data正式及功能beta分别处理。官方页面与搜索缓存对Enterprise默认开启日出现11月19/20日差异，正文不采用该未来日期。Carbon10月受限发布与11月10日扩大可用分开。TPU第八代4月推出与本周新系统分开。llama.cpp滚动列表没有直接展示v1，改用精确tag原文核实。
日报排除项重评：Claude协作组合在周窗口有重大影响，入选；钱包/自托管/DeepSeek/工作流不因日报已报而排除；框架版本与Goal Engineering仍因边际影响/证据性质不单列。Edge0、HyRealtime、Seedance等日报待核实线索本次未逐一取得新原文，保持未覆盖，不把日报结论当本周证据。
覆盖缺口：没有系统采样岗位招聘、中文独立小团队、各地区监管全部公告，也未独立复现实验/评估/产品可用性；因此不宣称全网无遗漏、不推算岗位数量。多媒体、机器人与科学模型只完成索引/线索扫描，未逐个实证核验，不作本周主导判断。来源显示发布时区不足，边界已明示；不混入11月15日20点后的消息。无关键来源整页访问失败；局部GitHub控件报错已注明。新事实若足以改变成本、权限或可用性，应修正本期判断。
-->
