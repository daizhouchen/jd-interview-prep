# jd-interview-prep

> 把一份 JD 反推成一张面试作战地图 · 三层结构（战略/战术/话术）· 单文件 HTML 典雅风 · Claude Code skill

把面试还原成"信号博弈"而非"问答考试"——粘贴一份 JD（可选简历），10 分钟内拿到一份**可在面试前 24 小时直接照着背**的高保真准备包。专攻 AI 产品经理（AI PM、AI 应用 PM、AI 解决方案 PM）方向，但通用框架适用于任何技术 / 产品 / 运营岗位。

## 它和"AI 帮我准备面试"的区别

大部分人贴 JD 给 LLM 让它"准备面试"，会得到一份**通用面试题大全**——这是清单，不是地图。

这个 skill 不一样：

- **三层作战地图**——不是堆题目，是把面试拆成战略层（这场面试到底是什么）/ 战术层（每一轮怎么打）/ 话术层（具体怎么说）三层结构
- **元认知诊断开篇**——HTML 第一段不是寒暄，是让你**对这场面试的理解升一个维度**的 200 字诊断
- **三档对比引擎**——所有重要建议给"弱 / 合格 / 惊艳"三档，让你立刻看到天花板
- **反例与失败学**——每个模块都有"做过这事的人 80% 会怎样错"段，反例传递的是判断力
- **认知地图**——eval / RAG / Agent 等 AI PM 高频考点，不只给题，给该领域的思维结构
- **公司情报带置信度**——WebSearch 抓真实情报，标 A/B/C/D 置信度（A=官方源，D=推断）
- **心理学 / 社会学融化进骨架**——Goffman 戏剧论 / Cialdini 影响力 / Bourdieu 场域 / 锚定 / 首因近因 / Big Five / Framing 等 10 个理论支柱**变成观察视角和指令逻辑**，不作为标签出现

## 安装

```bash
# Claude Code 用户
git clone https://github.com/daizhouchen/jd-interview-prep ~/.claude/skills/jd-interview-prep
```

或用 ssh：

```bash
git clone git@github.com:daizhouchen/jd-interview-prep.git ~/.claude/skills/jd-interview-prep
```

装完后在 Claude Code 里直接说："帮我准备这份 JD 的面试" + 粘贴 JD 即可触发。

## 使用

### 最少输入

```
我下周要面 [公司名]，帮我准备面试。下面是 JD：

[完整 JD 文本]
```

### 最佳输入

```
我下周要面 [公司名]，帮我准备面试。

[完整 JD 文本]

我的简历：
- 学历：硕士在读 / CS
- 项目 1：[简介，含技术栈、规模、关键数据]
- 项目 2：[简介]
```

### 输出

一份单文件 HTML 作战地图（典雅风），输出位置：`workspace/battle-map-<公司名>-<时间戳>.html`。可离线打开、可打印、可带去面试现场。

## 三层架构

```
┌─────────────────────────────────────────────────────────┐
│  L0 · 元认知诊断 (200 字)                                │
│  让你对这场面试的理解升一个维度。                        │
├─────────────────────────────────────────────────────────┤
│  L1 · 战略层                                             │
│  - JD 解码：表层 / 隐含 / 避雷信号                       │
│  - 场域分析：公司位置 / 派系 / 最近动作（带置信度）      │
│  - 叙事主轴 + 3 个传递目标形容词                         │
│  - 黑话校准（北美派 / 大厂派 / 创业派）                  │
├─────────────────────────────────────────────────────────┤
│  L2 · 战术层                                             │
│  - 分轮次画像（HR / 技术 / 直属 / skip / 终面）          │
│  - AI PM 经典考题（eval / RAG vs FT / hallucination /    │
│    cost / safety / framing 题）每个含认知地图 + 三档对比 │
│  - 项目深挖（事实 / 方法 / 哲学 三层讲法）               │
│  - 行为题（STAR / CAR / SOAR / SBI / S-CRAFT 模板选择）  │
├─────────────────────────────────────────────────────────┤
│  L3 · 话术层                                             │
│  - 自我介绍 30s / 60s / 2min                             │
│  - 反问清单（4 层 × 4 题 + 反例库）                      │
│  - 谈判剧本（先报价 vs 后报价 + offer 30+ 维度）         │
│  - 面试前 24h / 1h / 中 / 后仪式 + follow-up 邮件模板    │
└─────────────────────────────────────────────────────────┘
```

## 文件结构

```
jd-interview-prep/
├── SKILL.md                          # 主入口 + 三层工作流
├── references/
│   ├── decode-jd.md                  # JD 解码（表层/隐含/避雷）
│   ├── decode-field.md               # 场域分析（位置/派系/动作）
│   ├── narrative-architecture.md     # 叙事主轴 + 项目深挖 + 自我介绍 + 黑话
│   ├── round-strategy.md             # 5 类轮次画像 + 实习场景特化
│   ├── ai-pm-canon.md                # 8 个 AI PM 考题域 + 认知地图
│   ├── behavioral-craft.md           # 行为题工艺 + 失败叙事 S-CRAFT
│   ├── questions-you-ask.md          # 反问 4 层 + 反例库
│   ├── offer-craft.md                # 谈判 3 阶段 + offer 30+ 维度
│   ├── ritual-bookends.md            # 面试前/中/后仪式
│   └── output-spec.md                # HTML 章节结构规范
├── assets/
│   └── battle-map-template.html      # 典雅风模板（可改主色）
└── evals/
    └── evals.json                    # 测试用例
```

## 设计哲学

### 面试不是问答，是双向校准
这一句话决定了所有后续设计。三个推论：
1. 面试官的字面问题 ≠ 真正在评估的东西
2. 你的回答 ≠ 你传递的信号
3. 你问的反问 ≠ 你想知道的事

### 心理学 / 社会学的存在方式
这个 skill 大量调用了 Goffman 戏剧论、Cialdini 影响力六原则、锚定效应、首因近因、Big Five、Framing、Bourdieu 场域 / 文化资本、行为经济学等理论——但它们**不会作为"标签"出现在输出里**。

❌ 不会这样：`反问第 3 题（用 Cialdini 互惠原则）：……`

✅ 会这样：`想被记住为"会成长"的，问"如果我加入 6 个月，你判断我做对了什么/做错了什么的标准分别是什么？"——这一问还顺手激活了对方的"如果他加入"心理画面，把评估从"是否录取"悄悄推到"录取后怎么用"。`

后者通篇没出现 "Cialdini" 三个字，但调动了 4 种心理机制（signaling、impression management、commitment & consistency、prospective imagery）。

**写输出时，理论是骨头，不是装饰。**

### 厚度的 4 个引擎
1. **三档对比** —— 弱 / 合格 / 惊艳，让你看到天花板
2. **反例与失败学** —— 反例传递的是判断力，不是知识
3. **认知地图** —— 不只给题，给该领域的思维结构
4. **元层升维** —— HTML 开篇 200 字让你理解升一个维度

## 红线

- 🚫 不杜撰公司情报（必须 WebSearch 验证或标 D 级推断）
- 🚫 不杜撰用户经历（项目内容只能基于用户提供的简历）
- 🚫 不输出"通用面试题大全"——每条建议必须扣回 JD 或公司
- 🚫 不让用户撒谎或暗示扭曲事实

## 兼容性

- Claude Code（推荐，skill 系统原生支持）
- Claude.ai（手动复制 SKILL.md 内容到对话）
- 其他支持 SKILL.md 格式的 Claude harness

## 致谢

灵感来自：

- [domain-onboarding](https://github.com/daizhouchen/domain-onboarding) — 三层证据链 + A/B/C/D 来源分级的方法论母体
- [book-distiller](https://github.com/daizhouchen/book-distiller) / [movie-distiller](https://github.com/daizhouchen/movie-distiller) — 单文件典雅风 HTML 输出范式
- Goffman, Bourdieu, Cialdini, Kahneman 等社会学 / 心理学经典——它们的工具被融化进 skill 的指令逻辑

## License

MIT
