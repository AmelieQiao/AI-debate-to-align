# ⚒️Duet: AI Debate to align (BYOK)
- 一个HTML小工具：只发一次问题，两个AI模型并行回答，再辩论后达成一个对齐的最终答案 / A small HTML tool: two AI models answer in parallel, then debate to reach a single aligned final answer
- 消耗你自己的 tokens / Uses your own tokens
- 使用你自己的 OpenRouter API key（不发给别人） / Uses your own OpenRouter API key (not shared with anyone)
- 纯前端运行（client-side only）：API key 只保存在你的浏览器 `localStorage`，不会上传到任何服务器。 / Client-side only: your API key is stored only in your browser `localStorage` (no upload).

**Try it live** / **在线使用**  
[https://ai-debate-to-align.vercel.app/](https://ai-debate-to-align.vercel.app/) — open in a browser; no install. Same BYOK + static demos as the local HTML.

## 1. How to use
1. ✅ Open the [live site](https://ai-debate-to-align.vercel.app/) **or** double-click `index.html` locally. / 直接打开 Vercel 链接，或本地双击 `index.html`。
2. 📺 4 个样例问题无需消耗 tokens，点击可运行内置演示。/ Sample questions don't need tokens. With no API key, click 4 sample questions to run built-in static demos (no OpenRouter calls, no tokens).
3. 🔑 使用你自己的 tokens，将 OpenRouter API key（[openrouter.ai/keys](https://openrouter.ai/keys)）粘贴到页面顶部 “Manage API key”。Key 仅存储在你的浏览器，不会发给任何人。 / Use your own tokens: paste your OpenRouter API key into “Manage API key” in the header. Stored only in your browser.

## 2. Version & Features (TL;DR)

v5.2

- 两个模型并行回答 → 辩论 → 一个对齐的最终答案 / Two-model parallel Q&A → debate → one aligned final answer
- ChatGPT 支持模型 / ChatGPT models:
  - gpt-4o
  - gpt-4.1-mini

- Claude支持模型 / Claude models:
  - 3.5 Sonnet
  - 3.5 Haiku

- 支持各种语言 / Multiple languages supported
- 一开始的弹窗demo展示如何使用 / Demo window at start to show how to use
- Prompt支持文字和图片（图片大小由上游 OpenRouter 限制）/ Supports text + images (image limits depend on upstream OpenRouter)
- BYOK：OpenRouter API key 由用户提供 / BYOK: user-provided OpenRouter API key
- 无 Key 静态演示（4 个样例问题，不消耗 tokens）/ No-key static demo (4 sample questions, no tokens)
- 2轮辩论轮次 + 对齐百分比 + 最终对齐答案 / Debate rounds + alignment percentage + the final aligned answer
- 可以调整的输入框和答案框高度 / Adjustable input and answer panel heights
- 可以一键复制答案 / One-click copy for answers
- 可以在 Send 问题后点击 Stop 来停止 / Click Stop after sending to cancel
- 对齐答案底部加入“求同存异”（Remaining nuance）/ “Remaining nuance” is shown at the bottom of the aligned answer

## 3. Repository layout / 仓库结构

Static single-page app — **no** required folder reorganization for GitHub or Vercel.

```
├── index.html          → redirects to duet-v5-2.html
├── duet-v5-2.html      → main app (all UI + logic)
└── assets/             → demo video, static demo .md, optional README
```

You do **not** need to change this layout for deployment; Vercel serves these files as static assets.

## 4. License

MIT
