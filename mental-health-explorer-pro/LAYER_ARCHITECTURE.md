# Layer Architecture

> 目的：讓這套 MD 可以被其他 `.md`、SkillOS、Codex、Agent runtime 或人手複製時作為「可嵌入層」使用。

---

## 1. Load Order

```txt
0. safety/diagnosis-boundary.md
1. safety/privacy-boundary.md
2. safety/crisis-router.md
3. safety/self-harm-method-boundary.md
4. safety/safeguarding-boundary.md
5. safety/contraindications.md
6. safety/global-resources.md
7. protocols/session-flow.md
8. prompts/system-prompt.md
9. modules/*.md
10. tracking/*.md
11. protocols/closure-protocol.md
```

---

## 2. Layer Contract

任何子模組必須遵守：

1. 不診斷。
2. 不提供藥物或劑量建議。
3. 不替代醫生、臨床心理學家、輔導員或危機熱線。
4. 任何深層探索前必須先經 Safety Router。
5. Yellow / Orange / Red Zone 不做深挖。
6. OCD 模組不提供保證式 reassurance。
7. 鬱躁模組不鼓勵衝動決策或高刺激行為。
8. PTSD / Trauma 模組不逼迫敘述創傷細節。
9. 自傷 / 輕生方法細節要求必須拒絕，並轉向即時安全支援。
10. 未成年人、家暴、性暴力、被控制 / 威脅 / 跟蹤、即時人身危險必須啟動 safeguarding。
11. 每次探索必須 closure。
12. 如出現自傷、輕生、他傷、失控或精神病性症狀，立即轉危機支援。

---

## 3. Embed Patterns

### Pattern A：Markdown include comment

```md
<!-- @include mental-health-explorer-pro/SKILL.md -->
<!-- @include mental-health-explorer-pro/safety/crisis-router.md -->
<!-- @include mental-health-explorer-pro/modules/trauma-trigger-explorer.md -->
```

### Pattern B：SkillOS-style layer reference

```md
[[layer:MHE.SKILL]]
[[layer:MHE.SAFETY.CRISIS]]
[[layer:MHE.MODULE.TRAUMA_TRIGGER]]
```

### Pattern C：Manual import block

```md
## Imported Layer: Trauma Trigger Explorer

Source: `modules/trauma-trigger-explorer.md`
Load condition: only after Green Zone check.
```

---

## 4. Router Logic

```txt
User Input
↓
Crisis / Safety Check
↓
If Red → Crisis Router
If Orange → Stabilization Mode + professional escalation
If Yellow → Grounding + light record only
If Green → Companion / Explorer / Trauma Trigger / Tracking
↓
Closure Protocol
↓
Long-Term Tracking Update
```


## Single-File Platform Layer

`PROMPT_BUNDLE.md` 是給 Poe / GPTs / Claude Project / Gemini Gems 等單檔平台使用的 flattened runtime。它不取代 SkillOS 多檔 runtime，但包含核心 identity、safety router、self-harm method boundary、safeguarding boundary、diagnosis / medication boundary、Trauma Trigger Mode 與 closure protocol。
