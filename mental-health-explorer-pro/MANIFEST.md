# Mental Health Explorer Pro Manifest

## Package

- Name: `mental-health-explorer-pro`
- Version: `v2.2-public-bundle`
- Purpose: 心理支援式陪談系統 × 創傷知情陪談模式 × 情緒模式探索助手 × 自我覺察與穩定化輔助工具
- Primary Entry: `SKILL.md`
- Original Trauma Workbook SHA256: `06b827ec102c188c95ff8ce13bba87b4ff94883aa2d5787cf1b022a7f0478dce`

## File Tree

```txt
mental-health-explorer-pro/
├── README.md
├── MANIFEST.md
├── SKILL.md
├── PROMPT_BUNDLE.md
├── LAYER_ARCHITECTURE.md
├── BUILD_REPORT.json
├── modules/
│   ├── depression.md
│   ├── anxiety.md
│   ├── panic.md
│   ├── ocd.md
│   ├── bipolar-mood-support.md
│   ├── social-anxiety.md
│   ├── ptsd.md
│   ├── trauma-trigger-explorer.md
│   ├── long-term-emotion-tracker.md
│   ├── relationship-trigger-tracker.md
│   └── weekly-review.md
├── safety/
│   ├── crisis-router.md
│   ├── self-harm-method-boundary.md
│   ├── safeguarding-boundary.md
│   ├── global-resources.md
│   ├── contraindications.md
│   ├── diagnosis-boundary.md
│   └── privacy-boundary.md
├── prompts/
│   ├── system-prompt.md
│   ├── companion-mode.md
│   ├── stabilization-mode.md
│   ├── explorer-mode.md
│   ├── trauma-trigger-mode.md
│   └── review-mode.md
├── protocols/
│   ├── session-flow.md
│   ├── mood-check-in.md
│   ├── trigger-session-protocol.md
│   └── closure-protocol.md
├── tracking/
│   ├── daily-log-template.md
│   ├── trigger-database-template.md
│   ├── core-belief-map.md
│   ├── 14-day-tracker.md
│   ├── 30-day-summary.md
│   └── 90-day-review.md
├── layers/
│   ├── include-map.md
│   ├── layer-contract.md
│   └── md-embed-patterns.md
├── source/
│   └── trauma-trigger-workbook-original.md
├── references/
│   ├── global-clinical-guidelines.md
│   └── citation-map.md
└── tests/
    └── red-team-safety-tests.md
```

## Layer IDs

| Layer ID | File | Role |
|---|---|---|
| `MHE.SKILL` | `SKILL.md` | Main router and runtime rule |
| `MHE.PROMPT_BUNDLE` | `PROMPT_BUNDLE.md` | Single-file flattened runtime for Poe / GPTs / Claude Project |
| `MHE.SAFETY.CRISIS` | `safety/crisis-router.md` | Green / Yellow / Orange / Red Zone routing |
| `MHE.SAFETY.CONTRA` | `safety/contraindications.md` | Do-not-enter rules |
| `MHE.SAFETY.SELF_HARM_METHOD` | `safety/self-harm-method-boundary.md` | Refuse self-harm method details and route to immediate safety |
| `MHE.SAFETY.SAFEGUARDING` | `safety/safeguarding-boundary.md` | Minor / abuse / violence / coercive control / immediate danger boundary |
| `MHE.SAFETY.RESOURCES` | `safety/global-resources.md` | Global resource layer |
| `MHE.PROMPT.SYSTEM` | `prompts/system-prompt.md` | Agent system prompt |
| `MHE.MODULE.TRAUMA_TRIGGER` | `modules/trauma-trigger-explorer.md` | Full Trauma Trigger OS |
| `MHE.TRACKING.LONG_TERM` | `modules/long-term-emotion-tracker.md` | Daily / weekly / monthly tracking |
| `MHE.TRACKING.RELATIONSHIP` | `modules/relationship-trigger-tracker.md` | Relationship trigger pattern tracking |

## No Missing Info Notice

The full uploaded Trauma Trigger workbook is preserved exactly in `source/trauma-trigger-workbook-original.md` and embedded into `modules/trauma-trigger-explorer.md` after the layer wrapper.
