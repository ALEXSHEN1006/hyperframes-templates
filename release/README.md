# 产品发布版模板（release）

横屏 1920×1080 · 30 秒 · 结构：版本标题页 → 新功能三卡 → 收束 slogan
风格：与试点样片一脉的深色专业感。样片为**虚构示例**：《魔力喵 Studio 更新：批量生图队列上线》（V1.2），真实发布时换成真版本内容。

## 换内容改哪里（只改 index.html）

文案全部集中在 index.html 里三个标了「文案区」的段落：

1. **版本标题页**（搜「文案区 1/3」）：版本徽章（.badge，如「新版本 · V1.3」）、产品名大标题、主打功能一行（.feature-line）。
2. **新功能三卡**（搜「文案区 2/3」）：每张卡的功能名（.name）与两行说明（.desc，每行 ≤11 字）。
   - 卡高 480px 已按试点溢出教训留足；说明别超过两行。
   - 图标是单个汉字字标（.icon，如 队/续/铃，品牌蓝粗体）——不要换回 emoji：部分 emoji 在渲染环境里是单色字形，官方检查会判对比度 error，样片实测踩过。NEW 角标（.tag）可改「优化」「修复」或整行删掉。
3. **收束页**（搜「文案区 3/3」）：slogan 两行（金色词用 span 包）+ 落款。

## 改时长改哪里

总时长 `#root` 的 `data-duration`（默认 30）= 标题 7s + 功能 16s + 收束 7s；改段长时同步各 section 的 `data-start` 与 script 里的入场时间点。

## 改配色改哪里

`<style>` 顶部「品牌基线」:root 变量，三套模板共用同一套。

## 渲染

```bash
TMPDIR=~/.tmp-hf npm run check
TMPDIR=~/.tmp-hf npm run render   # 出片到 renders/
```

依赖全本地（assets/gsap.min.js），字体走系统 Noto Sans CJK SC 的 @font-face local()，不要改回 CDN。
