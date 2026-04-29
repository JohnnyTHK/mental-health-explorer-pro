# Mental Health Explorer Pro

> **中文定位**：心理支援式陪談系統 × 創傷知情陪談模式 × 情緒模式探索助手 × 自我覺察與穩定化輔助工具  
> **English Positioning**：Mental Health Pattern Explorer × Trauma-Informed Emotional Support Companion  
> **Package Type**：SkillOS / Codex / Git / Poe / Agent Markdown Package  
> **Medication Policy**：不提供藥物建議、不比較藥物、不建議劑量、不處理停藥或改藥。  
> **Clinical Boundary**：不是診斷、不是正式心理治療、不是危機熱線、不是醫療服務替代品。

---

## 1. 這個 package 是什麼

這是一套可模組化載入的 **創傷知情心理支援式陪談與長期情緒模式追蹤系統**。核心任務不是「診斷使用者」或「治療使用者」，而是：

1. 陪伴使用者安全描述目前狀態。
2. 透過安全分流判斷是否可探索。
3. 在安全時進行情緒模式、身體反應、想法、行為衝動與 trigger pattern 追蹤。
4. 在不安全時轉入 grounding、穩定化、危機升級或真人支援。
5. 長期建立資料化的 mood / trigger / core belief / protective response database。
6. 將原本的 Trauma Trigger 工作簿完整保留並嵌入為深層子模組。

---

## 2. 核心架構

```txt
Mental Health Explorer Pro
├─ Safety Router：先判斷 Green / Yellow / Orange / Red Zone
├─ Companion Layer：陪伴聊天、反映、澄清、穩定
├─ Symptom / Pattern Modules：抑鬱相關困擾、焦慮模式、驚恐反應、強迫循環、情緒高低波動、社交焦慮、創傷後困擾
├─ Trauma Trigger OS：完整嵌入原始 Trauma Trigger 探索手冊
├─ Self-Harm Method Boundary：拒絕自傷 / 輕生方法細節，轉向即時安全支援
├─ Safeguarding Boundary：未成年人、家暴、性暴力、被控制 / 威脅 / 跟蹤、人身危險分流
├─ Long-Term Tracking：每日、14 天、30 天、90 天追蹤
├─ Review Layer：週期性 pattern review
└─ Global Resources：全球化危機與支援資源
```

---

## 3. 重要保證：原始 Trauma Trigger MD 沒有刪減

原始文件已完整保留於：

```txt
source/trauma-trigger-workbook-original.md
modules/trauma-trigger-explorer.md
```

原始文件 SHA256：

```txt
06b827ec102c188c95ff8ce13bba87b4ff94883aa2d5787cf1b022a7f0478dce
```

`modules/trauma-trigger-explorer.md` 前段加入 layer wrapper 與 activation / block rules，後面完整嵌入原始工作簿全文。

---

## 4. 建議用法

### SkillOS / Codex

把整個資料夾放入：

```txt
skills/mental-health-explorer-pro/
```

入口檔：

```txt
SKILL.md
```

### Poe / GPT / Claude Project

優先貼入：

```txt
prompts/system-prompt.md
```

如果平台支援多文件，載入：

```txt
SKILL.md
safety/crisis-router.md
safety/self-harm-method-boundary.md
safety/safeguarding-boundary.md
safety/contraindications.md
modules/trauma-trigger-explorer.md
tracking/daily-log-template.md
```

---

## 5. 最重要安全原則

> 先穩定，再探索。  
> 先分流，再陪談。  
> 先記錄 pattern，不推論創傷源頭。  
> 不診斷、不開藥、不深挖記憶、不取代真人專業支援。  
> 遇到自傷 / 輕生方法細節、未成年人危險、家暴、性暴力、被控制 / 威脅 / 跟蹤或即時人身危險，停止探索並轉向即時安全支援。


## Single-File Platform Bundle

如果平台只方便貼入一個 prompt，請使用 `PROMPT_BUNDLE.md`。
