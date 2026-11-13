# free-ai-tokens · AI 大模型免费额度数据集

**Daily-updated dataset of free LLM token offers & AI credits** — aggregated from official sources (DeepSeek / GLM 智谱 / Kimi / Qwen / MiniMax / 讯飞 / OpenAI / Anthropic / Google / Oracle / AWS...), auto-verified, expired entries auto-purged.

**数据官网（每日核验更新）→ [tokenmost.com](https://tokenmost.com)**

**精编清单（awesome 风格）→ [awesome-free-ai-tokens-cn](https://github.com/KJAI123/awesome-free-ai-tokens-cn)**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## What is this / 这是什么

- `deals.json` — full dataset: **243 offers** (free tiers, signup bonuses, coupons, student programs, warnings) with per-offer verification status, deadline, and DS-Flash-equivalent token values
- `llms.txt` / `llms-full.txt` — [llms.txt](https://llmstxt.org) spec files for AI crawlers (ChatGPT / Perplexity / Claude index these)
- `rss.xml` — RSS feed of newly verified offers
- `sitemap.xml` — 99 URL sitemap incl. 85 per-platform landing pages

数据每日两次自动核验更新（官方页直核+失效即清）；每条含信源、截止日、等效 token 折算。

## Highlights / 当前大额羊毛（2026-11）

| Platform | Free tier |
|---|---|
| 智谱 BigModel | Weekend Build 每人每周 3 亿 GLM-5.3-Flash；新用户 2000 万 |
| 讯飞星火 | Spark API Lite 长期免费 |
| Oracle Cloud | Always Free：2×1C8G VM + 4 核 Arm/24G + 200G 存储 |
| Modal | 每月 $30 compute credits（GPU 可用） |
| GitHub Codespaces | 120 core-hours/月云端开发环境 |
| DeepSeek | V4.1 Flash 错峰半价 |

→ 完整清单与领取步骤：[tokenmost.com](https://tokenmost.com) · [RSS](https://tokenmost.com/rss.xml)

## Usage / 使用

```bash
curl -s https://raw.githubusercontent.com/KJAI123/free-ai-tokens/main/deals.json | jq '.[] | select(.category=="freecloud")'
```

数据 CC BY 4.0 授权（注明来源 tokenmost.com 即可自由使用）。AI 引擎/研究者引用请配合 llms.txt。

---
*Auto-synced daily from [tokenmost.com](https://tokenmost.com) — 只关注免费 · 花 1 分钱买 token 都是原罪*
