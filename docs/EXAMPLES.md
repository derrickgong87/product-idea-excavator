# Examples

## Example 1: Voice Character Intelligence App

Prompt:

```text
我想做一个语音类 APP。用户打开后说想跟谁聊天，系统马上构建出对应人物，用他的声音、语调和背景知识进行沟通。
```

Strong discovery questions:

- 用户打开这个 APP 的真实动机是什么：求知、陪伴、决策、历史沉浸，还是粉丝体验？
- 第一版是任意人物即时生成，还是精选人物库？
- 对在世公众人物，声音和身份边界怎么处理？
- 用户聊完后应该获得什么结果：启发、总结、情绪支持，还是可保存的洞察？
- 人物质量如何评测：知识准确、风格相似、语音沉浸、安全边界？

Likely MVP:

- curated character library
- character cards
- voice conversation
- public-source knowledge grounding
- clear non-impersonation labeling
- post-conversation insight summary

## Example 2: AI Customer Feedback Analyst

Prompt:

```text
我想做一个 AI 工具，帮产品团队整理客户反馈，最后生成产品需求。
```

Strong discovery questions:

- 反馈从哪里来？
- 谁现在手工整理？
- 每周花多少时间？
- 现有流程最痛的一步是什么？
- AI 输出是洞察卡片、需求优先级，还是 PRD 草稿？
- 哪些内容必须引用原始用户反馈？

Likely MVP:

- paste/upload feedback
- generate insight clusters
- cite source quotes
- select insights
- generate PRD draft
- mark AI assumptions

## Example 3: Personal Growth App

Prompt:

```text
我想做一个帮助个人成长的 app，但还不知道具体是什么。
```

Strong discovery behavior:

- accept that the idea is immature
- offer 2-3 possible directions
- recommend one based on pain and retention
- ask about the user's original trigger moment

Possible directions:

- daily reflection coach
- decision journal
- habit accountability partner
- life planning conversation assistant

## Example 4: Internal Knowledge Assistant

Prompt:

```text
帮我做一个给中小企业用的内部知识库产品 PRD。
```

Strong discovery questions:

- 员工找不到什么知识？
- 找不到会造成什么损失？
- 当前用什么工具？
- 权限和数据边界是什么？
- 是搜索、问答、流程自动化，还是专家路由？
- 是否真的需要 RAG？

Likely MVP:

- import a small set of docs
- permission-aware search
- answer with citations
- feedback on answer quality
- admin correction workflow

