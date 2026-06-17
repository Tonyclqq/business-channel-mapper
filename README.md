# business-channel-mapper

`business-channel-mapper` is a local Codex / Claude Code Skill for analyzing acquisition channels, customer sources, decision chains, trust chains, and channel priorities for any industry, product, service, or target customer.

It creates a structured Chinese report: `商业渠道地图分析报告`.

## What It Produces

- Final customer identification.
- Customer source map.
- Decision-chain analysis.
- Trust-chain analysis.
- Weighted channel scoring.
- Channel contact and cooperation strategy.
- Resource-person interview questions.
- 30-day action plan.

## Minimal Usage

Users only need to provide:

```text
行业/产品/服务:
目标客户:
城市/区域:
客单价/项目金额:
当前资源:
业务目标:
约束条件:
```

Codex should automatically generate the full commercial channel map analysis report and save it under `outputs/`.

## Folder Contents

- `SKILL.md`: Instructions for Codex / Claude Code.
- `prompts/`: Reusable analysis prompts.
- `templates/`: Report and action-plan templates.
- `examples/`: Sample channel maps for common industries.
- `checklists/`: Quality, resource-person, and cooperation checks.
- `scripts/generate_channel_report.py`: Local CLI report generator.

## Local CLI Usage

```bash
python scripts/generate_channel_report.py --industry "奢侈品零售" --service "门店灯光顾问" --target-customer "买手店、高定品牌、设计师品牌、奢侈品集合店" --city "上海" --ticket-price "5万-30万元"
```

Optional:

```bash
python scripts/generate_channel_report.py --industry "AI咨询" --service "企业AI工作流改造" --target-customer "50-300人服务型企业" --city "深圳" --ticket-price "10万-50万元" --output reports/ai_consulting_report.md
```

The script reads local templates only. It does not connect to Feishu, call external APIs, or create any database.
## 案例分享
1、内蒙古特色农产品供应链进入上海 B2B 采购市场
```https://xj1kzcoee8.feishu.cn/wiki/SMuxwkCISig9SDkgQhZc6X7hntb?from=from_copylink```
## 联系我
WeChat：```cc-cuii```
