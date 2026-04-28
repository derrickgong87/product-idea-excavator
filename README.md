# Product Idea Excavator

> An open-source Skill for turning vague product ideas into rigorous product discovery interviews and high-quality PRDs.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Language](https://img.shields.io/badge/language-English%20%7C%20中文-blue.svg)](docs/I18N.md)
[![Output](https://img.shields.io/badge/output-PRD-orange.svg)](product-idea-excavator/references/en/prd-template.md)

Product Idea Excavator is an agent Skill for founders, product managers, indie builders, AI product teams, and anyone who has a product idea that still lives mostly in their head.

It does not start by writing a plan.

It starts by asking better questions.

It extracts the concrete version of the product from your mind.

[中文说明](#中文)

---

# English

## Why This Is Different From Normal Plan Mode

Normal Plan Mode is useful when the goal is already clear. It can break a known task into implementation steps, milestones, and checklists.

Early product work is different. Most early product ideas are not ready to be planned. They need to be excavated.

Product Idea Excavator is built for the stage before planning:

- when the user has a product feeling but not a clear product definition
- when the user asks for a PRD but the core user, pain, and MVP are still unclear
- when the idea sounds exciting but demand evidence is weak
- when the product may need AI, but the AI role, data flow, quality bar, and failure mode are not defined
- when the user needs a sharp product partner, not a passive task planner

The Skill's job is not to immediately create a project plan. Its job is to help the assistant behave like a top-tier product manager:

- lead the product discovery interview
- ask the next strongest question
- challenge weak assumptions
- separate interest from demand
- narrow the product into a concrete wedge
- discuss technical stack and AI feasibility
- synthesize a PRD only after discovery is complete

This is the core difference:

```text
Normal Plan Mode:
User gives a goal -> assistant makes a plan.

Product Idea Excavator:
User gives a rough idea -> assistant excavates the product -> assistant validates assumptions -> assistant narrows the MVP -> assistant produces a PRD.
```

## What This Product Skill Does

Product Idea Excavator turns messy product ideas into structured product thinking.

It helps the assistant:

- identify the first real user
- uncover the actual triggering scenario
- test whether the pain is real or imagined
- understand the current workaround
- distinguish weak interest from strong demand
- force a narrow MVP wedge
- ask what should not be built
- evaluate AI/model usefulness and risk
- recommend a practical technical stack
- surface safety, privacy, identity, and compliance concerns
- generate a detailed PRD when the user confirms the exploration is complete

It is especially useful when the user says things like:

- "I want to build an AI app."
- "I have a startup idea, but it is still vague."
- "Help me write a PRD."
- "I want to make a product like..."
- "I know the feeling, but I cannot describe the product yet."
- "Can you act like a product manager and help me figure this out?"

## Key Features

### 1. Product Discovery Before Planning

The Skill treats unclear ideas as discovery problems, not planning problems.

It does not rush into features, timelines, or implementation tasks. It first asks:

- who the product is really for
- what problem is painful enough to solve
- what users currently do instead
- what behavior proves the need
- what version is small enough to test quickly

### 2. Assistant-Led Interview

The assistant leads the conversation.

The user does not need to know what to say next. The Skill keeps the discovery moving by asking one high-leverage question at a time.

A good response usually does four things:

1. briefly absorbs the user's latest answer
2. extracts one confirmed fact, assumption, or risk
3. gives options or a recommendation when the idea is immature
4. asks the next most important question

### 3. Demand Evidence Over Vibes

The Skill does not treat excitement as demand.

It pushes for stronger signals:

- someone already pays
- someone is willing to prepay
- someone spends time or money on a workaround
- someone shares real data
- someone depends on the workflow
- someone complains when the current process breaks

If the evidence is weak, the Skill does not shame the user. It suggests a practical validation task and then keeps the interview moving.

### 4. Narrow MVP Wedge

Early products often fail because the first version is too broad.

The Skill forces a narrower question:

```text
What is the smallest version that can create real value for one specific user segment?
```

It helps decide:

- which user segment to serve first
- which workflow to own first
- which features are P0
- which features are tempting but distracting
- which parts can be manual or semi-automated in v1

### 5. Technical Product Judgment

This is not just a product strategy prompt.

The Skill explicitly explores technical stack and implementation feasibility:

- target platform: web, mobile, extension, desktop, API-first, bot, or internal tool
- frontend/backend architecture
- database and storage
- authentication and permissions
- AI/model layer
- RAG, Agent, tool calling, multimodal input, or fine-tuning
- latency, cost, observability, and evaluation
- admin tools and operational workflows
- what should be optimized for speed now versus scale later

The goal is practical product execution, not abstract strategy.

### 6. AI Product Sense

For AI products, the Skill asks:

- is AI the core value or only a workflow accelerator?
- what are the inputs and outputs?
- what must be accurate?
- what happens when the model is wrong?
- does the product need citations, confidence, human review, or rollback?
- what data improves the system over time?
- what should be evaluated before users trust it?

This helps prevent vague "AI-powered" ideas from becoming unreliable products.

### 7. Built-In PRD Quality Bar

The Skill includes reference playbooks for:

- discovery questions
- product sense
- technical stack decisions
- AI product judgment
- PRD structure
- example interview patterns

The assistant can load the relevant reference only when needed. This keeps the session focused while preserving depth.

## Bilingual Routing

This repository uses one Skill for both English and Chinese users.

The language behavior is simple:

- English prompt -> English interview -> English PRD
- Chinese prompt -> Chinese interview -> Chinese PRD
- Mixed prompt -> follow the language used for the product idea itself

The Skill keeps each session in one language unless the user explicitly asks for bilingual output.

Why this matters:

- English users should not feel they are using a translated Chinese project.
- Chinese users should not be forced into English unless they want it.
- The project keeps one repo, one issue tracker, one release history, and one community.
- The same product discovery method works across both languages with language-specific references.

See [Bilingual Strategy](docs/I18N.md).

## Detailed Workflow

### Stage 1: Product Origin

The Skill first clarifies where the idea came from.

It asks about:

- the moment that triggered the idea
- whether the idea comes from personal pain, customer requests, market observation, or technical inspiration
- what the product is trying to change
- whether the user is solving a real problem or chasing an attractive concept

### Stage 2: First User

The Skill pushes the user to define the first real user.

It asks:

- who uses it
- who pays
- who decides
- who feels the pain most urgently
- why this user would try an imperfect v1

### Stage 3: Problem Depth

The Skill tests whether the problem is worth solving.

It asks:

- how often the pain happens
- how severe the cost is
- what users do today
- whether the current workaround is painful enough to replace
- what observable behavior proves demand

### Stage 4: Value Proposition

The Skill clarifies the product's core promise.

It asks:

- when the user first feels value
- what behavior changes after using the product
- what outcome the user would pay for
- what would remain valuable if competitors copied most features

### Stage 5: Product Shape And User Flow

The Skill turns the idea into an experience.

It asks:

- where the product starts
- what the user sees first
- what the core workflow is
- what inputs are required
- what output the user receives
- how failure states are handled

### Stage 6: MVP Scope

The Skill narrows the first version.

It asks:

- which three features are truly required
- what should be excluded from v1
- whether the product can be tested manually first
- what makes the MVP successful
- what the smallest paid, repeated, or relied-on version is

### Stage 7: AI And Technical Feasibility

The Skill asks whether AI is necessary and how it should work.

It explores:

- model role
- data sources
- prompt/RAG/Agent/tool-calling needs
- quality metrics
- safety constraints
- human review
- fallback behavior
- cost and latency

### Stage 8: Technical Stack

The Skill asks about the practical implementation path.

It explores:

- team capability
- timeline
- platform
- database
- authentication
- payments
- analytics
- deployment
- integrations
- admin needs
- long-term architectural tradeoffs

### Stage 9: Business Model And Growth

The Skill connects the product to a business loop.

It asks:

- who pays
- why they pay
- how the first 100 users are reached
- what creates retention
- what pricing model fits the value

### Stage 10: Metrics, Risks, And PRD

The Skill defines success and risk before writing the PRD.

It asks:

- which metric proves user value
- which metric may be misleading
- what assumption could kill the product
- what must be tested before building more

When the user confirms there is nothing else to add, the Skill automatically synthesizes a PRD.

## What The Final PRD Covers

The final PRD can include:

- product name
- one-sentence summary
- background and opportunity
- target users and personas
- problem definition
- current alternatives
- demand evidence
- narrowest wedge
- value proposition
- goals and non-goals
- MVP scope
- core user journeys
- functional requirements
- non-functional requirements
- UX requirements
- data requirements
- AI/model requirements
- technical stack recommendation
- system architecture
- roles and permissions
- integrations
- admin and operations requirements
- metrics
- edge cases and failure states
- premise challenges and alternative paths
- risks and validation plan
- roadmap
- open questions

## Example Use Cases

### Example 1: Voice Character App

Input:

```text
I want to build a voice app. Users say who they want to talk to, and the app constructs a character based on public information, background knowledge, voice style, and conversational personality.
```

The Skill explores:

- whether the core use case is entertainment, learning, decision support, history immersion, or emotional companionship
- whether v1 should support any person or a curated library
- how to handle public figures, voice likeness, consent, disclaimers, and safety
- whether characters need a knowledge base, persona card, or hybrid system
- how to evaluate whether the conversation feels deep, useful, and safe
- what the MVP should include before scaling character coverage

Possible PRD direction:

```text
A curated voice-based character intelligence app where users bring real questions and enter immersive conversations with high-quality simulated characters built from public sources, clear boundaries, and non-misleading voice design.
```

### Example 2: AI Customer Feedback Analyst

Input:

```text
I want an AI tool that helps product teams organize customer feedback and generate product requirements.
```

The Skill explores:

- where the feedback comes from
- who currently organizes it
- how much time the workaround costs
- what evidence proves teams need this
- whether v1 should integrate with tools or accept manual uploads
- how to distinguish evidence-backed insights from AI guesses

Possible MVP:

- paste or upload raw feedback
- generate insight cards
- cite representative customer quotes
- let the PM select insights
- generate a PRD draft with assumptions clearly marked

### Example 3: Churn Prediction For Customer Success

Input:

```text
I want to build a SaaS product for customer success teams that predicts churn and tells them what action to take.
```

The Skill explores:

- whether users need prediction, prioritization, playbooks, or workflow automation
- which data source is available in v1
- what signals customer success teams already trust
- what false positives and false negatives cost
- whether the product should start as an alerting tool, dashboard, or action workspace
- what model quality bar is required before users rely on it

Possible MVP:

- connect one source of customer activity data
- show the top accounts needing attention
- explain why each account is risky
- recommend one next action
- let the user mark whether the recommendation was useful

### Example 4: Personal Growth App

Input:

```text
I want to build an app for personal growth, but I do not know the exact product yet.
```

The Skill does not get stuck. It can propose directions:

- daily reflection and journaling
- decision coaching
- goal tracking
- emotional pattern discovery
- habit accountability

Then it recommends a path, asks the user to choose or correct it, and continues into target users, first-use moment, retention loop, safety boundaries, and MVP.

## Quick Start

### Option 1: Ask Your Agent To Install The Skill

Send this prompt to your coding agent:

```text
Please install this Skill from GitHub:
https://github.com/derrickgong87/product-idea-excavator

Clone the repository, copy the product-idea-excavator/ folder into my local  Skills directory, verify that product-idea-excavator/SKILL.md is installed, and then tell me how to start a new session and test it.
```

After installation, start a new session and test it with:

```text
I have a product idea, but it is still fuzzy. Use product-idea-excavator to help me excavate it through questions.
```

### Option 2: Manual Installation

Clone the repository:

```bash
git clone https://github.com/derrickgong87/product-idea-excavator.git
```

Copy this folder into your local  Skills directory:

```text
product-idea-excavator/
```

The installed structure should include:

```text
product-idea-excavator/
  SKILL.md
  references/
  evals/
  demo/
```

Start a new assistant session so the Skill metadata can be discovered.

## Repository Structure

```text
product-idea-excavator/
  SKILL.md
  README.md
  references/
    prd-template.md
    discovery-question-bank.md
    product-sense-playbook.md
    tech-stack-playbook.md
    ai-product-playbook.md
    example-interviews.md
    en/
      prd-template.md
      discovery-question-bank.md
      product-sense-playbook.md
      tech-stack-playbook.md
      ai-product-playbook.md
      example-interviews.md
  evals/
    evals.json
  demo/
    sample-run.md

docs/
  INSTALL.md
  USAGE.md
  README.zh-CN.md
  I18N.md
  EXAMPLES.md
  EVALUATION.md
  SAFETY.md
  ROADMAP.md
  PUBLISHING.md
```

## Commercial Use

This project is open source under the MIT License.

You can use it for personal, commercial, internal, client, educational, or startup work. You can copy it, modify it, package it into your own workflow, and use it to produce PRDs for real products, as long as you follow the license terms.

## Safety And Boundaries

This Skill is designed for product discovery and specification writing.

For products involving public figures, voice, identity, financial decisions, medical advice, legal advice, emotional support, children, or political content, the Skill should surface safety, consent, labeling, and compliance questions early.

Read [Safety](docs/SAFETY.md).

## Evaluation

The repo includes starter evals in:

[product-idea-excavator/evals/evals.json](product-idea-excavator/evals/evals.json)

These evals check whether the Skill:

- asks instead of prematurely writing
- responds in the correct language
- distinguishes demand from interest
- handles vague ideas
- challenges scope
- explores technology and AI implementation
- produces concrete PRD-ready material

Read [Evaluation](docs/EVALUATION.md).

## Contributing

Contributions are welcome. The most valuable contributions are:

- sharper interview questions
- better PRD examples
- stronger eval prompts
- product archetype playbooks
- safety improvements
- real-world transcripts with sensitive details removed

Read [Contributing](CONTRIBUTING.md).

## License

MIT License. See [LICENSE](LICENSE).

---

# 中文

> 一个开源  Skill，用来把模糊的产品想法，挖掘成高质量的产品访谈、产品判断和 PRD。

Product Idea Excavator 是一个用于打磨产品的Skill，适合创业者、产品经理、独立开发者、AI 产品团队，以及任何脑海里有产品想法但还没完全想清楚的人。

它不会一上来就写计划。

它会先问更好的问题。

## 它和普通 Plan Mode 的区别

普通 Plan Mode 适合目标已经清楚的时候。它可以把一个明确任务拆成步骤、里程碑和 checklist。

但早期产品工作不是这样。很多产品 idea 在进入计划之前，还需要被挖掘。

Product Idea Excavator 解决的是“计划之前”的问题：

- 用户有一个产品感觉，但还没有清晰定义
- 用户想写 PRD，但核心用户、痛点和 MVP 还不清楚
- idea 听起来很有趣，但需求证据很弱
- 产品可能需要 AI，但 AI 的角色、数据流、质量标准和失败兜底还没定义
- 用户需要的是一个强产品合伙人，而不是被动任务规划器

这个 Skill 的任务不是立刻生成项目计划，而是让助手像顶级产品经理一样工作：

- 主动带领产品发现访谈
- 问出当前最重要的问题
- 挑战薄弱假设
- 区分兴趣和真实需求
- 把产品收敛到具体 MVP 切口
- 讨论技术栈和 AI 可行性
- 在确认挖掘完成后再生成 PRD

核心区别是：

```text
普通 Plan Mode：
用户给出目标 -> 助手拆成计划。

Product Idea Excavator：
用户给出模糊想法 -> 助手挖掘产品 -> 助手验证假设 -> 助手收敛 MVP -> 助手生成 PRD。
```

## 这个 Product Skill 能做什么

Product Idea Excavator 会把混乱的产品想法变成结构化的产品思考。

它会帮助助手：

- 找到第一批真实用户
- 挖出真实触发场景
- 判断痛点是真实存在，还是只是想象
- 理解用户当前的替代方案
- 区分弱兴趣和强需求
- 强制收敛最窄 MVP 切口
- 追问哪些东西不应该做
- 判断 AI/模型的作用和风险
- 推荐务实的技术栈
- 提前暴露安全、隐私、身份和合规问题
- 在用户确认探索完成后，生成详细 PRD

它特别适合用户说：

- “我想做一个 AI app。”
- “我有一个创业 idea，但还很模糊。”
- “帮我写一份 PRD。”
- “我想做一个类似某某的产品。”
- “我知道那个感觉，但还讲不清产品是什么。”
- “你能不能像产品经理一样帮我把这个想清楚？”

## 核心特点

### 1. 先产品发现，再进入计划

这个 Skill 会把不清楚的想法当成产品发现问题，而不是执行计划问题。

它不会急着进入功能、时间线和开发任务，而是先问：

- 产品到底给谁用
- 什么问题痛到值得解决
- 用户现在怎么解决
- 什么行为能证明需求存在
- 什么版本足够小、可以快速测试

### 2. 助手主动发起访谈

对话由助手推进。

用户不需要知道下一步该说什么。Skill 会一次问一个高价值问题，让访谈持续向前。

一个好的回复通常会做四件事：

1. 简短吸收用户上一轮回答
2. 提炼一个已确认事实、假设或风险
3. 在想法不成熟时给出选项或建议
4. 问出下一个最重要的问题

### 3. 重视需求证据，而不是感觉

这个 Skill 不会把“听起来不错”当成需求。

它会追问更强的信号：

- 已经有人付费
- 有人愿意预付
- 有人正在用笨办法花时间或花钱解决
- 有人愿意提供真实数据
- 有人把工作流建立在这个问题上
- 现有流程出问题时，有人会着急或投诉

如果证据很弱，Skill 不会否定用户，而是会给出一个可执行的验证任务，然后继续推进访谈。

### 4. 强制收敛最窄 MVP 切口

早期产品失败，很多时候不是因为想得不够大，而是第一版太大。

这个 Skill 会不断追问：

```text
对于一个具体用户群体，什么是最小但真正有价值的版本？
```

它会帮助判断：

- 第一批服务哪类用户
- 第一版先吃下哪段工作流
- 哪些功能是 P0
- 哪些功能很诱人但会分散注意力
- 哪些部分在 v1 可以人工或半自动完成

### 5. 有技术型产品判断

这不是一个只讲产品战略的提示词。

Skill 会明确追问技术栈和落地可行性：

- 产品形态：Web、移动端、插件、桌面端、API-first、机器人、内部工具
- 前后端架构
- 数据库和存储
- 登录和权限
- AI/模型层
- RAG、Agent、工具调用、多模态输入、微调
- 延迟、成本、可观测性和评测
- 运营后台和人工处理流程
- 现在应该优先上线速度，还是长期扩展性

目标是推动真实产品落地，而不是停留在抽象策略。

### 6. 有 AI 产品 Sense

对于 AI 产品，Skill 会问：

- AI 是核心价值，还是只是效率增强？
- 输入和输出是什么？
- 哪些结果必须准确？
- 模型错了会发生什么？
- 是否需要引用、置信度、人工审核或回滚？
- 哪些数据能让系统随时间变好？
- 用户信任之前应该如何评测？

这能防止一个模糊的“AI-powered”想法，变成一个不可靠的产品。

### 7. Skill 内置 PRD 质量标准

项目内置了多份参考资料：

- 产品发现问题库
- 产品 Sense playbook
- 技术栈决策 playbook
- AI 产品判断 playbook
- PRD 模板
- 示例访谈模式

助手只会在需要时读取相关资料。这样既能保持对话聚焦，又能保证深度。

## 中英文路由

这个仓库用一个 Skill 同时服务英文和中文用户。

语言行为很简单：

- 英文提示 -> 英文访谈 -> 英文 PRD
- 中文提示 -> 中文访谈 -> 中文 PRD
- 中英混合提示 -> 跟随产品想法本身使用的语言

除非用户明确要求双语输出，否则同一次会话不会混用中英文。

这样做的好处是：

- 英文用户不会觉得自己在使用一个中文项目的机器翻译版
- 中文用户也不会被迫进入英文语境
- 项目可以保持一个仓库、一个 issue 区、一个发布历史和一个社区
- 同一套产品发现方法，可以通过不同语言的参考资料服务不同用户

详见 [Bilingual Strategy](docs/I18N.md)。

## 详细工作流

### 阶段 1：产品原点

Skill 会先弄清楚 idea 从哪里来。

它会问：

- 是哪个具体瞬间触发了这个想法
- 这个 idea 来自亲身痛点、客户请求、市场观察，还是技术启发
- 产品想改变什么
- 用户是在解决真实问题，还是在追逐一个听起来很好的概念

### 阶段 2：第一批用户

Skill 会推动用户定义第一批真实用户。

它会问：

- 谁使用
- 谁付费
- 谁决策
- 谁最痛
- 为什么这个用户愿意尝试一个不完美的 v1

### 阶段 3：问题深度

Skill 会判断这个问题是否值得解决。

它会问：

- 痛点发生频率有多高
- 成本有多严重
- 用户今天怎么解决
- 现有替代方案是否痛到值得替换
- 什么可观察行为证明需求存在

### 阶段 4：价值主张

Skill 会明确产品的核心承诺。

它会问：

- 用户第一次感到“值了”的时刻是什么
- 使用产品后，用户行为发生了什么变化
- 用户到底愿意为什么结果付费
- 如果竞争对手复制 80% 功能，产品还剩什么价值

### 阶段 5：产品形态和用户路径

Skill 会把 idea 变成具体体验。

它会问：

- 产品从哪里开始
- 用户第一眼看到什么
- 核心工作流是什么
- 需要哪些输入
- 用户得到什么输出
- 失败状态如何处理

### 阶段 6：MVP 范围

Skill 会收窄第一版。

它会问：

- 哪 3 个功能是真正必须的
- v1 明确不做什么
- 是否可以先用人工方式验证
- MVP 成功标准是什么
- 什么是最小可付费、可重复使用或可依赖版本

### 阶段 7：AI 与技术可行性

Skill 会判断 AI 是否必要，以及应该如何工作。

它会探索：

- 模型角色
- 数据来源
- prompt/RAG/Agent/工具调用需求
- 质量指标
- 安全边界
- 人工审核
- 失败兜底
- 成本和延迟

### 阶段 8：技术栈

Skill 会追问务实的实现路径。

它会探索：

- 团队能力
- 上线时间
- 产品平台
- 数据库
- 登录和权限
- 支付
- 分析
- 部署
- 第三方集成
- 后台运营需求
- 长期架构取舍

### 阶段 9：商业模式和增长

Skill 会把产品接到商业闭环上。

它会问：

- 谁付费
- 为什么付费
- 第一批 100 个用户从哪里来
- 留存来自哪里
- 什么定价方式和价值最匹配

### 阶段 10：指标、风险和 PRD

Skill 会先定义成功和风险，再写 PRD。

它会问：

- 哪个指标真正证明用户价值
- 哪个指标可能误导团队
- 哪个假设一旦错了会让产品失败
- 继续开发前必须验证什么

当用户确认没有其他补充后，Skill 会自动总结 PRD。

## 最终 PRD 会覆盖什么

最终 PRD 可以包含：

- 产品名称
- 一句话总结
- 背景与机会
- 目标用户与画像
- 问题定义
- 当前替代方案
- 需求证据
- 最窄切口
- 价值主张
- 产品目标与非目标
- MVP 范围
- 核心用户路径
- 功能需求
- 非功能需求
- UX 要求
- 数据需求
- AI/模型需求
- 技术栈建议
- 系统架构
- 角色与权限
- 集成需求
- 后台和运营需求
- 指标体系
- 边界情况与失败状态
- 前提挑战和替代方案
- 风险与验证计划
- Roadmap
- 待确认问题

## 使用案例

### 案例 1：语音人物对话 App

输入：

```text
我想做一个语音类 APP。用户说出想跟谁聊天，系统马上构建一个对应的人物，并用他的背景知识、声音风格和表达方式进行对话。
```

Skill 会探索：

- 核心场景是娱乐、学习、决策支持、历史沉浸，还是情感陪伴
- v1 是支持任意人物，还是先做精选人物库
- 如何处理公众人物、声音相似度、授权、免责声明和安全边界
- 人物应该基于知识库、persona card，还是混合方案
- 如何评估一次对话是否足够深、有用、安全
- 在扩展人物库之前，MVP 应该包含什么

可能的 PRD 方向：

```text
一个精选人物库的语音角色智能产品，让用户带着真实问题进入沉浸式对话。角色基于公开资料、明确边界和非误导性声音设计构建。
```

### 案例 2：AI 客户反馈分析工具

输入：

```text
我想做一个 AI 工具，帮产品团队整理客户反馈，并生成产品需求。
```

Skill 会探索：

- 反馈来自哪里
- 现在谁在整理
- 当前笨办法消耗多少时间
- 什么证据证明团队真的需要
- v1 应该集成工具，还是先支持手动上传
- 如何区分有证据的洞察和 AI 猜测

可能的 MVP：

- 粘贴或上传原始反馈
- 生成 insight cards
- 引用代表性用户原话
- 让产品经理选择洞察
- 生成带有假设标记的 PRD 草稿

### 案例 3：客户成功流失预测 SaaS

输入：

```text
我想做一个 SaaS，帮客户成功团队预测客户流失，并告诉他们下一步该做什么。
```

Skill 会探索：

- 用户真正需要的是预测、优先级排序、playbook，还是工作流自动化
- v1 有哪些数据源可用
- 客户成功团队现在信任哪些信号
- 误报和漏报分别会造成什么成本
- 产品应该先做提醒工具、仪表盘，还是行动工作台
- 用户依赖模型前需要达到什么质量标准

可能的 MVP：

- 接入一个客户行为数据源
- 展示最需要关注的客户列表
- 解释每个客户为什么有风险
- 推荐一个下一步动作
- 让用户标记推荐是否有用

### 案例 4：个人成长 App

输入：

```text
我想做一个帮助个人成长的 app，但还不知道具体是什么。
```

Skill 不会卡住。它会先给出几个方向：

- 日常反思和 journaling
- 决策 coaching
- 目标追踪
- 情绪模式发现
- 习惯陪跑

然后它会推荐一个路径，让用户选择或纠正，并继续推进到目标用户、首次使用时刻、留存循环、安全边界和 MVP。

## 快速开始

### 方式 1：让你的 Agent 帮你安装这个 Skill

把这句话发给你的 coding agent：

```text
请帮我从 GitHub 安装这个  Skill：
https://github.com/derrickgong87/product-idea-excavator

请 clone 这个仓库，把 product-idea-excavator/ 文件夹复制到我本地的  Skills 目录中，确认 product-idea-excavator/SKILL.md 已安装，然后告诉我如何开启一个新会话并测试它。
```

安装完成后，开启新会话，用这句话测试：

```text
我有一个产品 idea，但还不成熟。请用 product-idea-excavator 的方式，通过提问帮我把它挖掘清楚。
```

### 方式 2：手动安装

Clone 这个仓库：

```bash
git clone https://github.com/derrickgong87/product-idea-excavator.git
```

把这个文件夹复制到本地  Skills 目录：

```text
product-idea-excavator/
```

安装后的结构应包含：

```text
product-idea-excavator/
  SKILL.md
  references/
  evals/
  demo/
```

然后开启一个新的助手会话，让 Skill 元数据被重新发现。

## 仓库结构

```text
product-idea-excavator/
  SKILL.md
  README.md
  references/
    prd-template.md
    discovery-question-bank.md
    product-sense-playbook.md
    tech-stack-playbook.md
    ai-product-playbook.md
    example-interviews.md
    en/
      prd-template.md
      discovery-question-bank.md
      product-sense-playbook.md
      tech-stack-playbook.md
      ai-product-playbook.md
      example-interviews.md
  evals/
    evals.json
  demo/
    sample-run.md

docs/
  INSTALL.md
  USAGE.md
  README.zh-CN.md
  I18N.md
  EXAMPLES.md
  EVALUATION.md
  SAFETY.md
  ROADMAP.md
  PUBLISHING.md
```

## 商业使用

本项目基于 MIT License 开源。

你可以把它用于个人、商业、内部团队、客户项目、教育或创业场景。你可以复制、修改、集成到自己的工作流中，也可以用它为真实产品生成 PRD，只要遵守 license 条款即可。

## 安全与边界

这个 Skill 用于产品发现和产品规格撰写。

如果产品涉及公众人物、声音、身份、金融决策、医疗建议、法律建议、情感支持、儿童或政治内容，Skill 应该尽早提出安全、授权、标识和合规问题。

详见 [Safety](docs/SAFETY.md)。

## 评估

仓库中包含 starter evals：

[product-idea-excavator/evals/evals.json](product-idea-excavator/evals/evals.json)

这些 eval 会检查 Skill 是否：

- 先提问，而不是过早写 PRD
- 使用正确语言回应
- 区分兴趣和需求
- 能处理模糊想法
- 会挑战过大的范围
- 会探索技术和 AI 实现
- 能产出具体、可进入 PRD 的材料

详见 [Evaluation](docs/EVALUATION.md)。

## 贡献

欢迎贡献。最有价值的贡献包括：

- 更锋利的访谈问题
- 更好的 PRD 示例
- 更强的 eval prompt
- 产品类型 playbook
- 安全改进
- 去敏后的真实访谈记录

详见 [Contributing](CONTRIBUTING.md)。

## License

MIT License. See [LICENSE](LICENSE).
