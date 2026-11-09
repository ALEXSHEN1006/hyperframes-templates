# 科普短视频版模板（short）

竖屏 1080×1920 · 26 秒 · 结构：钩子大字 → 三点快切（每点 6 秒）→ 结论字幕
风格：节奏快、大字醒目，适合抖音/小红书。样片选题：《AI 视频为什么会崩脸？三个原因》。

## 换内容改哪里（只改 index.html）

文案全部集中在 index.html 里五个标了「文案区」的段落：

1. **钩子**（搜「文案区 1/5」）：顶部小字（kicker）、三行大字（.hook，金色那行是问题点）、副行（.hook-sub）。
   - 钩子大字固定三行、每行 ≤5 字，168px 字号装得下，别加长。
2. **要点一/二/三**（搜「文案区 2/5、3/5、4/5」）：每点的标题（.p-title，≤6 字）与一句说明（.p-desc，≤26 字、自动折两行）。
3. **结论**（搜「文案区 5/5」）：两行结论（金色行可拆两行）+ 落款。

固定 3 个要点；增减要点需同步改各 section 的 `data-start`（每点 6 秒等距）和 `#root` 的 `data-duration`，以及 script 里 points 数组的时间点。

## 改配色改哪里

`<style>` 顶部「品牌基线」:root 变量，三套模板共用同一套；大数字与结论金句用 --accent（琥珀），钩子顶部小字用 --accent2（蓝）。

## 渲染

```bash
TMPDIR=~/.tmp-hf npm run check
TMPDIR=~/.tmp-hf npm run render   # 出片到 renders/
```

依赖全本地（assets/gsap.min.js），字体走系统 Noto Sans CJK SC 的 @font-face local()，不要改回 CDN。
