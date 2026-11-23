# free-ai-tokens · AI 免费额度数据集

TokenMost 收录免费模型、积分、试用金、折扣和历史活动，每条记录包含核验状态。按平台查看领取规则，或订阅最近核验的免费权益。

[比较免费 AI API](https://tokenmost.com/free-ai-api.html?utm_source=github_dataset) · [平台目录](https://tokenmost.com/platform/?utm_source=github_dataset) · [领取攻略](https://tokenmost.com/guides/?utm_source=github_dataset) · [已核验免费权益 RSS](https://tokenmost.com/verified.xml)

## 数据文件

| 文件 | 内容 |
|---|---|
| `deals.json` | 全量目录，含已公开、历史和待整理记录。先筛选发布状态、核验状态与截止日期。 |
| `verified.xml` | 最近核验的常规免费权益，每条链接定位至平台的具体权益。 |
| `rss.xml` | 完整公开情报流，含折扣和历史权益。 |
| `llms.txt`、`llms-full.txt` | 平台索引及可引用的额度说明。 |
| `sitemap.xml` | 主站的规范页面地址。 |

## 使用示例

查看已发布、已核验的原始日/月 Token 记录。仍需按条目检查有效期、模型和账号资格。

```bash
curl -fsSL https://raw.githubusercontent.com/KJAI123/free-ai-tokens/main/deals.json |
  jq '.[] | select(.published and .verify_status == "verified") |
      . as $d | .token_quota[]? |
      select(.unit == "tokens" and (.period == "daily" or .period == "monthly")) |
      {provider: $d.provider, amount, period, model, deadline: $d.deadline, url: $d.url}'
```

The dataset keeps tokens, credits, requests, and currency in their original units. The mirror workflow checks the TokenMost source repository twice daily and publishes changed files from the same revision. See the [source project](https://github.com/KJAI123/tokenmost), [mirror runs](https://github.com/KJAI123/free-ai-tokens/actions/workflows/refresh.yml) and [curated Chinese guide](https://github.com/KJAI123/awesome-free-ai-tokens-cn).

数据采用 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) 授权，引用时请注明来源 TokenMost。
