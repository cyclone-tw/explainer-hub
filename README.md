# explainer-hub

Cyclone 的 **素材圖解專區**：把外部來源（開源 repo、文件、軟體介紹、Markdown、長文）做成可分享的 HTML visualizer，掛在 GitHub Pages。

不限 GitHub——任何值得對照／拆解的公開素材都可以進這裡。

- **Hub**: https://cyclone-tw.github.io/explainer-hub/
- **Issue tracker**: https://github.com/cyclone-tw/explainer-hub/issues

> 舊名 `github-analyzation` 已更名；GitHub 會把舊 URL redirect 過來。

## 現有分析

| Slug | 主題 | 頁面 |
| --- | --- | --- |
| `illustrated-guide-to-ai-agents` | Newsletter《A Visual Guide to LLM Agents》↔ HandsOnLLM TinyAgent repo | [open](https://cyclone-tw.github.io/explainer-hub/analyses/illustrated-guide-to-ai-agents/) |

## 目錄慣例

```text
docs/
  index.html                          # hub
  analyses/<slug>/index.html          # 單篇 visualizer（自包含）
  assets/                             # 共用 CSS／圖（可選）
```

新增一篇時：

1. 開 issue，寫清來源 URL（或附件說明）、範圍、驗收。
2. 在 `docs/analyses/<slug>/` 放自包含 `index.html`。
3. 更新 `docs/index.html` 的卡片清單與本 README 表格。
4. PR 用 `Closes #N`；Pages 來源是 `/docs` on `main`。

## 邊界

- 不 fork、不 vendoring 上游；只連出去原網址（或說明來源）。
- 不放 secrets、學生可識別資料。
- 深度知識進 Cyclone-Wiki `_inbox/`；本站負責可分享的視覺解說。

## 本機預覽

```bash
cd docs && python3 -m http.server 8765
# open http://127.0.0.1:8765/
```
