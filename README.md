# Fabric for STRIDE Threat Model

[Fabric](https://github.com/danielmiessler/fabric) is framework that enables AI at your fingertips. Instead going into chat (e.g. ChatGPT) or writing custom programs that consume API, you can create prompts as markdown text and get output as markdown. Fabric also maintain database of prompts called [patterns](https://github.com/danielmiessler/fabric/tree/main/patterns).

In this repo, I collected examples of usage of [create_stride_threat_model](https://github.com/danielmiessler/fabric/blob/main/patterns/create_stride_threat_model/system.md) pattern:

| File | Description | Model |
| --- | --- | --- |
| [INPUT.md](INPUT.md) | Example of architecture document of fiction project AI Nutrition-Pro | --- |
| [baseline_threat_modeling_action.md](baseline_threat_modeling_action.md) | Baseline Threat Model from my [ai-threat-modeling-action](https://github.com/xvnpw/ai-threat-modeling-action) | Claude 3 Opus |
| [baseline_threat_scenarios.md](baseline_threat_scenarios.md) | Baseline Threat Model created by fabric using [create_threat_scenarios](https://github.com/danielmiessler/fabric/blob/main/patterns/create_threat_scenarios/system.md) pattern | Claude 3 Opus |
| [threat_model_claude_3_opus.md](threat_model_claude_3_opus.md) | Threat Model created using `create_stride_threat_model` pattern | Claude 3 Opus |
| [threat_model_gpt_4o.md](threat_model_gpt_4o.md) | Threat Model created using `create_stride_threat_model` pattern | GPT-4o |
| [threat_model_gemini_1.5_pro.md](threat_model_gemini_1.5_pro.md) | Threat Model created using `create_stride_threat_model` pattern | Gemini-1.5 Pro Latest |

## How to reproduce

```
# get fabric installed - https://github.com/danielmiessler/fabric
$ wget https://raw.githubusercontent.com/xvnpw/fabric-stride-threat-model/main/INPUT.md
$ cat INPUT.md | fabric --pattern create_stride_threat_model -m claude-3-opus-20240229 > threat_model_claude_3_opus.md
```