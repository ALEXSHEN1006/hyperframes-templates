# Third-Party Notices / 第三方声明

This repository is MIT-licensed (see `LICENSE`), **except** for the third-party
components listed below, which keep their own licenses and are **not** covered
by this repository's MIT license.

本仓以 MIT 许可发布（见 `LICENSE`），但下列第三方组件保留其自身许可，
**不在本仓 MIT 覆盖范围内**。

---

## GSAP 3.14.2 (GreenSock)

- **Component / 组件:** `assets/gsap.min.js` (one identical copy in each template:
  `course/assets/`, `short/assets/`, `release/assets/`)
- **Copyright / 版权:** Copyright © GreenSock. All rights reserved.
- **License / 许可:** GreenSock's proprietary standard license —
  https://gsap.com/standard-license

Key points / 要点：

- GSAP is free to use, **including for commercial purposes**, under GreenSock's
  standard license. / GSAP 依 GreenSock 标准许可免费使用，**含商业用途**。
- The copyright and license header inside `gsap.min.js` is retained as-is and
  must not be removed. / `gsap.min.js` 文件内的版权与许可声明头已原样保留，
  不得删除。
- GSAP itself is **not** MIT-licensed and is **not** relicensed by this
  repository. If you redistribute these templates, GSAP remains under
  GreenSock's terms. / GSAP 本身不是 MIT 许可，本仓不对其重新授权；
  再分发本模板时，GSAP 仍适用 GreenSock 的条款。

## Fonts / 字体

- The templates reference **Noto Sans CJK SC** through CSS `@font-face`
  `local()` only. **No font files are included in this repository**, so no font
  redistribution takes place. Install Noto Sans CJK SC on your system before
  rendering, or the layout will fall back to another font and may shift.
  / 模板仅通过 CSS `@font-face` 的 `local()` 引用系统字体 **Noto Sans CJK
  SC**，**仓内不含任何字体文件**，不存在字体再分发。渲染前请在本地安装该
  字体，否则会回退到其他字体、版式可能变化。

## Framework / 框架依赖

- The templates run on the open-source **Hyperframes** framework, invoked at
  runtime via `npx hyperframes@0.8.200` (see each template's `package.json`).
  Hyperframes is an external dependency declared in `hyperframes.json` /
  `package.json`; no Hyperframes code is bundled in this repository.
  / 模板基于开源框架 **Hyperframes** 运行，运行时经
  `npx hyperframes@0.8.200` 调用（见各模板 `package.json`）。Hyperframes 是
  在 `hyperframes.json`／`package.json` 中声明在案的外部依赖，本仓未夹带
  其代码。
