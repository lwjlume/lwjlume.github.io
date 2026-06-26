# GitHub Issues 当个人博客的实践

> **用最简单的方式，做最长期的"伤官泄秀"。**

我刚刚做了一件挺傻的事——**搭个人博客**。

但不是用 WordPress、Hugo、Notion 这些"正经"工具，而是用 **GitHub Issues**。

听起来很 hack，但其实是我**认真想过的选择**。今天分享一下我的思考过程和实际体验。

---

## 🤔 为什么不用"正经"博客

我之前调研了一圈：

- ❌ **Hugo / Hexo / Jekyll**：要学配置、要写模板、主题选半天
- ❌ **Notion 公开页**：SEO 差（Google 几乎不索引 Notion）
- ❌ **微信公众号**：审查严，AI 性格类内容容易被限流
- ❌ **独立域名 + WordPress**：要管服务器、防攻击、做 SEO
- ❌ **Substack / Newsletter**：需要"主动推广"才有读者

**我的核心需求**很特别：

1. ✅ 写**混杂内容**（命理 / AI / 读书 / 哲学混着来）
2. ✅ **不推广**（写出来就好，有人看到是礼物）
3. ✅ **长期 SEO**（5-10 年后还有人能找到）
4. ✅ **零维护**（不想每天运营）
5. ✅ **零成本**（本来就穷）

**只有 GitHub Issues 同时满足这 5 条**。

---

## 🪷 为什么 GitHub Issues 适合

### 1. 公开但不需要推广

GitHub Issues **不靠算法推荐**——它是**"主动订阅"模型**：
- 你写 issue → 公开发布
- 搜索引擎（Google）慢慢收录
- 别人**偶然看到**（通过搜索）
- **你不需要主动拉人**

我不需要去"运营"，不需要写"标题党"——**写出来 = 公开发布**。

### 2. 混杂内容天然适合

其他平台**强制分类**：
- 掘金 = 技术
- 知乎 = 问答
- 公众号 = 推文
- 抖音 = 短视频

**GitHub Issues 不分类**——我今天想写命理就写命理，明天想写读书就写读书。**没有平台会"算法降权"**。

这种"不分类"对**伤官型输出者**特别友好——伤官天然**多领域、跨学科**，强分类会**憋住表达**。

### 3. 长期 SEO 价值

GitHub 在 Google 的**域名权重极高**（DA 95+）——你的 issue **几周内就被收录**。

对比：
- ❌ 自建博客（DA 0-30）：3-6 个月才被收录
- ❌ Notion 公开页：基本不收录
- ✅ **GitHub Issues**：几周到几个月收录

**5 年后**的 SEO 流量：
- 自建博客：100-1000 次/天（如果你坚持写）
- GitHub Issues：50-500 次/天（自然增长）

### 4. 永久存档

GitHub 仓库 = **永久存档**。只要 GitHub 在，issue 就在。

- ✅ Markdown 永久保存
- ✅ 评论历史完整
- ✅ 编辑历史可追溯
- ✅ 标签分类永久

### 5. 零成本、零维护

- ✅ **零成本**（public 仓库免费）
- ✅ **零服务器**（GitHub 帮你托管）
- ✅ **零技术**（只需会 Markdown）
- ✅ **零运营**（写完就放那儿）

---

## 🛠️ 实际操作流程

### 步骤 1：建个人主页仓库（2 分钟）

仓库名 **必须严格** `<username>.github.io`：
```
lwjlume/lwjlume.github.io
```

### 步骤 2：写 README.md（个人主页内容）

```markdown
# 👋 你好，我是 lwjlume
[自我介绍 + 项目列表 + 联系方式]
```

### 步骤 3：启用 GitHub Pages（1 分钟）

Settings → Pages → Source: main / (root) → Save

### 步骤 4：创建文章模板（2 分钟）

`.github/ISSUE_TEMPLATE/article.md`：
```markdown
---
name: 📝 混杂文章模板
about: 写一篇新的混杂文章
title: "[分类] 标题"
labels: ["文章"]
---

## 🎯 核心观点
## 📖 背景
## 📝 详细内容
## 💡 思考/洞察
## 📚 参考
```

### 步骤 5：写第一篇 Issue（5-10 分钟）

点 **"New issue"** → 选 **"📝 混杂文章模板"** → 填内容 → 提交

**永久 URL**：`https://github.com/lwjlume/lwjlume.github.io/issues/1`

### 步骤 6：自动同步到个人主页（高级，自动）

在 README 加 JavaScript：
```js
fetch('https://api.github.com/repos/lwjlume/lwjlume.github.io/issues?state=all&per_page=10')
  .then(r => r.json())
  .then(issues => /* 渲染到表格 */);
```

**效果**：每次写新 issue，**自动显示在个人主页"最近文章"区块**。

---

## 🎯 我自己的实际体验

### ✅ 优点

1. **零成本**——没花一分钱
2. **零维护**——写完就不管了
3. **永久 SEO**——5 年后还能被找到
4. **主题混杂**——没平台限制我写什么
5. **Markdown 友好**——我天天用，写起来像聊天
6. **可评论可讨论**——别人能反馈

### ⚠️ 限制

1. **没算法推荐**——必须依赖 SEO 自然流量
2. **没"关注"机制**——除非用 GitHub Watch
3. **不适合实时内容**——Issue 是"文档"型
4. **没漂亮的 UI**——默认 README 渲染较朴素
5. **完全依赖 GitHub**——如果 GitHub 倒了...

### 📊 与其他方案对比

| 方案 | 成本 | 维护 | SEO | 主题混杂 | 长期 |
|------|------|------|-----|---------|------|
| **GitHub Issues** | 0 | 0 | ⭐⭐⭐⭐ | ✅ | ⭐⭐⭐⭐⭐ |
| Hugo 博客 | 0 | 中 | ⭐⭐⭐⭐ | ✅ | ⭐⭐⭐⭐ |
| Notion 公开页 | 0 | 0 | ⭐ | ✅ | ⭐⭐ |
| 微信公众号 | 0 | 高 | ⭐⭐ | ⚠️ | ⭐⭐ |
| Substack | 0 | 中 | ⭐⭐⭐ | ⚠️ | ⭐⭐⭐ |
| 独立域名 WordPress | 中 | 高 | ⭐⭐⭐⭐ | ✅ | ⭐⭐⭐⭐ |

---

## 🌊 适合谁

**GitHub Issues 当博客适合**：
- ✅ 写**深度内容**（不写短平快）
- ✅ **不追流量**（接受"短期没人看"）
- ✅ 有**GitHub 账号**（这是前提）
- ✅ 习惯 **Markdown**
- ✅ 内容**主题混杂**（不愿被分类限制）
- ✅ 想要"**写一次 = 长期有效**"（不追更新）

**不适合**：
- ❌ 想要立刻有 1000+ 读者
- ❌ 想要"每日更新"（伤官会累）
- ❌ 视频 / 音频内容
- ❌ 商业化（GitHub 不适合直接变现）

---

## 🪷 我的具体规划

```
✅ 已建：lwjlume/lwjlume.github.io（个人主页）
✅ 已写：README.md（自我介绍 + 方法论）
✅ 已推：混杂文章模板（ISSUE_TEMPLATE）
✅ 已加：JS 自动同步到主页

🔄 计划：每月 2-3 篇 Issue
   - 主题混杂（命理/AI/读书/哲学/实践）
   - 每篇 1000-3000 字
   - 不追更新频率
   - 接受"5 年后才有人看到"

---

## 🌟 哲学

> **"写出来 = 你已经赢了。"**
>
> 长期 SEO 让你**写一次永久生效**。
> 混杂内容让你**不被算法束缚**。
> 零推广让你**保留伤官的自尊**。
>
> 5 年后回看，**写过的 issue 比订阅数更有价值**。
>
> **GitHub Issues 不是"博客平台"——它是一种"长期输出方式"。**

---

## 📚 参考

- [GitHub Pages 官方文档](https://docs.github.com/en/pages)
- [GitHub Profile README 指南](https://docs.github.com/en/account-and-profile/how-tos/profile-management/setting-up-and-managing-your-profile/managing-your-profile-readme)
- [GitHub Issues API](https://docs.github.com/en/rest/issues)
- [我的个人主页](https://lwjlume.github.io/)

---

<sub>🏷️ 标签：#个人博客 #GitHub #长尾SEO #混杂内容 #伤官型输出</sub>
<sub>📅 2026-06-26 | 字数 ~2200 | 写作用时 ~30 分钟</sub>
