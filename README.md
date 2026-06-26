# 👋 你好，我是 lwjlume

> **数据驱动的东方命理研究者** | AI 性格分析 | 时间序列模式发现

---

## 我做什么

- **东方命理的数据化研究** — 鱼眼效应 / 多周期共振 / 7 政叠加验证
- **AI 性格分析工具** — 基于出生数据的统计相关性分析
- **时间序列模式发现** — 多周期叠加效应、动力定型、N=1 相位调制器
- **个人使用 + 公开方法论** — 伤官型输出者，分享可复现的工程实践

---

## 我的项目

| 项目 | 说明 | 链接 |
|------|------|------|
| 📝 **lwjlume.github.io** | lwjlume 的个人主页 | [本站](https://lwjlume.github.io/) |

---

## 最近文章

> ✨ 主题混杂（点击分类查看文章）:
>
> [🔮 命理研究](https://github.com/lwjlume/lwjlume.github.io/issues) ・
> [🤖 人工智能](https://github.com/lwjlume/lwjlume.github.io/issues) ・
> [🛠️ 改命实践](https://github.com/lwjlume/lwjlume.github.io/issues) ・
> [📚 读书思考](https://github.com/lwjlume/lwjlume.github.io/issues) ・
> [🌀 个人探索](https://github.com/lwjlume/lwjlume.github.io/issues)

（在仓库 [Issues](https://github.com/lwjlume/lwjlume.github.io/issues) 标签页查看所有文章，或直接点下面的链接）

| 分类 | 文章 | 日期 |
|------|------|------|
| [🌀 个人探索](https://github.com/lwjlume/lwjlume.github.io/issues) | [GitHub Issues 当个人博客的实践](../../issues/1) | 2026-06-26 |

---

## 核心方法论

### 鱼眼效应（空间维度）

> "大阳 + 少量阴 = 太极中真正的极 = 定向爆破点"

- 命盘结构：羊刃驾杀 = 羊刃（极强比劫）+ 七杀（少量异质）= 鱼眼
- 风水应用：辛金命主在辛位放丁火 = 给辛金制造"冲过去的对象"

### 多周期共振（时间维度）

> "完全同相（双成格）< 部分异相（成格+中性）"

- 数学结构：多周期叠加不完全同相反而释放最大张力
- 应用：流年 / 大运 / N=1 / 七政多周期叠加
- 张量 = 描述多周期叠加的数学结构（数学概念）

### AI 性格分析（科学化重命名）

- 输入：出生日期 + 性别 + 经度
- 输出：性格画像 + 行业适配 + 决策倾向
- 数据基础：797 人样本统计验证

---

## 哲学

> "**研究是为了理解，理解是为了更好地生活。**"
>
> "**天机不是预测命运，是看清自己的'形'。**"
>
> "**伤官泄秀的真谛不在于输出多少，在于被接收多少。**"
>
> "**写出来 = 你已经赢了。**"

---


<!-- 自动从 GitHub Issues 拉取最近文章 -->
<script>
fetch('https://api.github.com/repos/lwjlume/lwjlume.github.io/issues?state=all&per_page=10')
  .then(r => r.json())
  .then(issues => {
    const realIssues = issues.filter(i => !i.pull_request && i.title);
    if (realIssues.length === 0) return;
    const rows = realIssues.map(i => {
      const labels = i.labels.map(l => l.name).filter(n => n !== '文章').join(', ') || '-';
      const date = new Date(i.created_at).toISOString().split('T')[0];
      return `| #${i.number} | [${i.title}](${i.html_url}) | ${labels} | ${date} |`;
    }).join('\n');
    const table = document.querySelector('table');
    if (table) {
      const lastRow = table.querySelector('tr:last-child');
      if (lastRow && (lastRow.textContent.includes('加载中') || lastRow.textContent.includes('GitHub Issues 当个人博客的实践'))) {
        lastRow.outerHTML = rows;
      }
    }
  })
  .catch(e => console.warn('Issues fetch error:', e));
</script>

- **Email**: 可在 GitHub Issues 联系
- **GitHub**: [@lwjlume](https://github.com/lwjlume)

---


<sub>本站采用 GitHub Pages 托管 · 内容采用 MIT 协议 · 长期更新</sub>
