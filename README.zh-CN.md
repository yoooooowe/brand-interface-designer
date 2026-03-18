# Brand Interface Designer

一个更强调**审美判断**的 UI 设计 agent prompt kit。

它主要想解决一个很具体的问题：

> 大多数设计 prompt 很会产出结构，但不太会产出判断。

它们通常很擅长生成：
- design system
- 组件清单
- accessibility checklist
- developer handoff 结构

但不太擅长生成真正让人觉得：
- 克制
- 高级
- 有品牌感
- 锋利
- 有主次
- 不模板化

**Brand Interface Designer** 这套东西，就是想把 agent 从“普通 SaaS 输出”往更强的层级判断、品牌表达和视觉克制上拉。

---

## 这是什么

**Brand Interface Designer** 是一套给 UI 设计 agent 用的 prompt 基础设施。它的重点不是“生成更多 UI”，而是“做更有判断的 UI”。

它会把 agent 往这些方向推：
- 先定义视觉气质，再定义组件
- 保护品牌气质，不要滑进 generic SaaS 模板
- 用 hierarchy、typography、spacing、restraint 做质量
- 在保持可用、可扩展、可访问的前提下，把界面做得更克制、更像被认真判断过

它**不是**：
- Figma 插件
- 代码生成器
- design token 编译器
- 完整设计系统框架

它本质上是一个：

**更重视审美判断的界面设计 prompt kit**

---

## 为什么要做这个

很多 UI 设计 prompt 最后会掉进两种常见状态：

### 1）Design-system brain
输出很完整、很有条理、很方便实现，
但视觉上经常是：**正确，但普通**。

### 2）Dribbble brain
第一眼看着挺花哨、挺有设计感，
但一旦进入真实产品约束、真实内容、真实状态，就很容易塌。

这个仓库想卡在中间：
- 比纯系统型 prompt 更有审美
- 比纯装饰型 prompt 更能落地
- 比 generic UI kit 更有品牌敏感度
- 比“现代、简洁、高级”这种空 prompt 更有操作性

---

## 适合谁

这套更适合：
- 想减少模板味的产品设计师
- 在意视觉判断和品牌气质的 UI / 品牌设计师
- 在做 AI-assisted design workflow 的团队
- 正在做 fintech / crypto / SaaS，但不想界面看起来都一个样的人
- 已经受够了“clean modern SaaS UI”重复输出的人

---

## 仓库里有什么

### `agents/brand-led-ui-designer.md`
主 agent 文档。

它定义了：
- agent 的角色和立场
- 审美原则
- 工作流程
- hierarchy 规则
- anti-generic 检查
- 怎么把 brand 转成 interface behavior

### `references/taste-reference.md`
审美参考文档。

它主要讲：
- 可以从 Robinhood、Linear、Apple、editorial / luxury commerce 这类参考里提炼什么
- generic SaaS / crypto / UI-kit 常见问题是什么
- 如何用一些 heuristics 去判断一个界面是高级、普通、还是模板化
- 怎么把 taste 真的翻译成界面决策

### `critique-mode.md`
批稿模式。

适合拿来：
- 批已有设计稿
- 找 generic 问题
- 看 hierarchy 为什么弱
- 判断哪些东西该删、该并、该安静
- 把“能用”往“有判断”推进

### `examples/`
一些现成可用的任务 brief，包括：
- login
- dashboard
- asset detail
- landing page
- onboarding
- trading page
- critique-dashboard
- critique-landing-page
- critique-trading-page

### `usage.md`
一个轻量使用说明，讲这些文件怎么组合起来用。

---

## 核心思路

这套东西最核心的一句是：

> 不要先优化“完整度”，先优化“视觉判断”。

翻成人话就是：
- 先定气质，再定组件
- 先做主次，再做装饰
- 先删，再加
- 尽量让 typography 和 composition 多干活
- 让品牌感不只靠颜色存在
- 不要动不动用更多 card、border、container 去硬撑结构

---

## 这套东西和普通 prompt 最大的区别

很多 prompt 会让模型做“beautiful / modern / premium” 的 UI。
但这种词太空，最后经常只会产出一些熟悉的视觉套话。

这个仓库想做的，是把“审美”拆成更能执行的东西，比如：
- hierarchy
- spacing rhythm
- typography load
- tonal restraint
- container reduction
- 品牌感是否能脱离颜色存在
- anti-template heuristics
- 删除是否提升质量

也就是说，它想把 taste 从抽象形容词，变成 agent 真能拿来用的判断框架。

---

## 推荐怎么用

建议这样组合：

1. 用 `agents/brand-led-ui-designer.md` 做 base prompt
2. 用 `references/taste-reference.md` 提供审美参考和判断框架
3. 用 `examples/` 里的 brief 当起点
4. 再补你自己的项目背景、约束和视觉参考

一个简单的使用结构可以是：

1. 加载 `agents/brand-led-ui-designer.md`
2. 加载 `references/taste-reference.md`
3. 提供任务 brief，至少包括：
   - 项目背景
   - 希望的感觉
   - 靠近哪些参考
   - 避免哪些味道
   - 什么必须最先被看到
   - 什么应该安静一点

---

## 一个推荐的 brief 写法

```md
Use the Brand-Led UI Designer perspective.

Project:
[这个页面 / 功能是什么]

Goal:
[用户要完成什么]

This should feel:
- calm
- premium
- sharp
- minimal

Closer to:
- Robinhood restraint
- Linear precision

Avoid:
- generic SaaS
- loud gradients
- too many cards

What must stand out:
- [主视觉重点]

What should stay quiet:
- [次级内容]
```

---

## 适合的场景

- 设计或批 dashboard
- 优化 generic fintech / crypto UI
- 在搭 design system 前先定界面方向
- 复盘一个“没什么错，但也没什么记忆点”的页面
- 训练 design-focused agent 做更好的审美取舍
- 把已有界面往更清晰的 hierarchy 和更安静的 surface 推

---

## 不太适合的场景

- 纯视觉风格探索
- 完全没有产品逻辑的一次性出图 prompt
- 只想要 token spec / component states 的团队
- 已经有非常成熟视觉总监和品牌规范约束的场景

---

## 这套仓库背后的立场

这个仓库是有点主观的。

它默认相信一件事：

很多界面的问题，不是“不够精致”，而是“不够有判断”。

所以它想做的，不是让 agent 再加更多 UI。
而是让它做更好的决定。

---

## 如果你要用它

别把它当成最终答案。
更好的用法是：
- 改它
- 缩紧它
- 用你自己的参考替换里面的参考
- 让它越来越贴近你自己的标准

这套东西最理想的状态，不是保持原样，
而是慢慢长成你自己的 taste system。
