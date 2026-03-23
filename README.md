# threads-algorithm

Threads/Meta 社群經營顧問 — Claude Code Skill

基於 darkseoking 對 26 個 Meta 演算法專利機制的深度研究與實戰驗證，萃取成可操作的經營顧問 skill。

## 安裝

```bash
claude install-skill azuma520/threads-algorithm-skill
```

或手動複製到 `~/.claude/skills/threads-algorithm/`。

## 能力

| 模式 | 觸發情境 | 做什麼 |
|------|---------|--------|
| **帳號健檢** | 首次諮詢、帳號定位問題 | 問診 → 分析 Creator Embedding → 給主題規劃 |
| **策畫** | 「幫我規劃這週發文」 | 判斷狀態 → 給節奏時間表 → 建議內容方向 |
| **建議** | 具體決策問題 | 路由到對應框架 → 用反問句引導思考 |
| **診斷** | 「我的文沒流量」 | 六關排查流程 → 找到原因 → 具體行動 |

## 知識架構

```
references/
├── distribution-lifecycle.md   # 擴散三階段、Low Signal、發文節奏
├── account-authority.md        # Creator Embedding、Social Graph、蜜月期
├── engagement-economics.md     # 互動權重（私訊>留言>按讚）、Audience Affinity
├── content-strategy.md         # 爆文後路徑、測水溫、外部連結、刪文重發
└── naturalness-principle.md    # 自然感法則、Google/Meta 反操控偵測

templates/
├── pre-post-checklist.md       # 發文前/後 checklist
└── post-diagnosis.md           # 「沒流量」六關診斷流程
```

5 個框架從 26 個演算法機制重新分類萃取，按「用戶面對的問題」組織，不是按原始來源。

## 涵蓋的演算法機制

- **Meta 專利**：語意向量推薦（US10579688B2）、Low Signal 偵測（US-20190095961-A1）、Diversity Enforcement（US9336553B2）、Audience Affinity（US8402094B2）、Creator Embedding（US10558714B2）等 15+ 個專利
- **Google 反壟斷訴訟**：Navboost、Chrome 瀏覽數據、IS4 真人評分（交叉對照用）
- **實戰驗證**：darkseoking 從 6K 到 20K 追蹤的經營經驗

## Eval 結果

| 指標 | With Skill | Baseline | 差異 |
|------|-----------|----------|------|
| Pass Rate | 100% (13/13) | 40% (5/13) | +60% |

3 個測試用例：帳號健檢、爆文後策畫、沒流量診斷。Baseline 在爆文後策畫中會給出**錯誤建議**（同主題延伸文），skill 版本正確建議休息 + 換角度。

## 設計原則

- **顧問，不是教科書**：先問問題了解狀況，再給建議
- **可操作優先**：每次對話結束都有具體下一步
- **承認不確定性**：演算法是幾十個參數交叉，不保證單一答案
- **不鼓勵過度優化**：發文是為了寫自己開心的內容，不是為了爆文而活

## 素材來源

- [darkseoking Threads 貼文系列](https://www.threads.net/@darkseoking)：5 篇演算法專利深度解析
- 萃取方法論參考：[glebis/claude-skills](https://github.com/glebis/claude-skills)

## License

MIT
