# 一次資料集と検証状況 / Sources and Verification Status

**作成日**: 2026-08-12

本文書は [2026-review.md](./2026-review.md) の記述の裏付けとなる資料と、その検証状況を記録する。記録として残す文書である以上、精度を最優先し、**確認できなかったものは「未確認」と明記する**。

## 検証の方法と限界

- 検証日: 2026年8月12日
- 検証手段: 本作業環境のネットワークは egress プロキシにより多くの外部ドメインへの直接アクセスが制限されていた。そのため検証水準を項目ごとに明記する：
  - **直接確認**: 一次資料のファイル本体を取得して全文確認したもの（GitHub 上の公式リポジトリ等）
  - **間接確認**: 検索エンジンのインデックス経由で一次資料URLと内容の要旨を取得し、複数の独立した報道・専門解説と照合したもの。URLの生存はインデックス経由の蓋然性確認に留まる
- **推奨**: 間接確認の項目は、通常の閲覧環境からURLへ最終アクセス確認を行うことが望ましい

---

## 1. 米国判例

### Thaler v. Perlmutter 上告棄却 — 検証: ✅ 間接確認（日付・内容とも特定済み）

- 棄却日: **2026年3月2日**（Order List）。Docket No. 25-449
- 維持された判決: Thaler v. Perlmutter, 130 F.4th 1039 (D.C. Cir. 2025)（No. 23-5233、2025年3月18日判決）
- 一次資料:
  - 最高裁 docket: https://www.supremecourt.gov/docket/docketfiles/html/public/25-449.html
  - D.C. Circuit 判決文（Justia 収録）: https://law.justia.com/cases/federal/appellate-courts/cadc/23-5233/23-5233-2025-03-18.html
- 補助資料: Baker Donelson / Mayer Brown / Holland & Knight 各クライアントアラート、IPWatchdog（2026-03-02付）

### Bartz v. Anthropic — 検証: ✅ 間接確認

- 事件: N.D. Cal., No. 3:24-cv-05417
- 2025-06-23: Alsup 判事 summary judgment（合法取得書籍の学習=フェアユース、海賊版取得・保持=フェアユース外）
- 2025-09-05 和解合意（15億ドル+利息）、2025-09-25 予備承認、**2026-07-20 最終承認**（Martínez-Olguín 判事）
- 一次資料に最も近いもの: CourtListener の docket（No. 3:24-cv-05417）— **本環境からアクセス不能のため未確認。掲載時に要確認**
- 補助資料:
  - Authors Guild（最終承認報告）: https://authorsguild.org/news/court-grants-final-approval-anthropic-copyright-settlement/
  - Authors Alliance（2026-07-21）: https://www.authorsalliance.org/2026/07/21/bartz-v-anthropic-settlement-receives-final-approval/
  - TechCrunch（2026-07-20）: https://techcrunch.com/2026/07/20/anthropics-landmark-1-5b-copyright-settlement-is-approved/
- ⚠️ 注記: 対象作品数（約50万件）・1作品約3,000ドルは**概数**。確定値は最終承認命令での確認を推奨

## 2. 日本の法制度

### AI推進法 — 検証: ✅ 間接確認（政府サイトのインデックス情報と複数報道の一致）

- 正式名称: **人工知能関連技術の研究開発及び活用の推進に関する法律**（令和7年法律第53号）
- 2025-05-28 成立、2025-06-04 公布、2025-09-01 全面施行。本則28条の理念法・罰則なし
- 一次資料:
  - e-Gov 法令検索: https://laws.e-gov.go.jp/law/507AC0000000053
  - 内閣府: https://www8.cao.go.jp/cstp/ai/ai_act/ai_act.html
  - 日本法令索引（NDL）: https://hourei.ndl.go.jp/simple/detail?lawId=0000168047

### 法務省 取りまとめ報告書（2026-08-07） — 検証: ✅ 間接確認（PDF本体の直接閲覧は本環境から不可）

- 正式名称: 「肖像、声等の無断利用による民事責任の在り方に関する検討会 取りまとめ報告書 ―生成AIによるパブリシティ権侵害等に関する解釈指針―」（表紙日付は「令和8年8月」）
- 検討会は2026年4月24日〜7月27日の全5回
- 一次資料:
  - 公表ページ: https://www.moj.go.jp/MINJI/minji05_00778.html
  - 報告書PDF: https://www.moj.go.jp/content/001468286.pdf
  - 検討会ページ: https://www.moj.go.jp/MINJI/minji07_00400.html
- 日本俳優連合の見解: https://www.nippairen.com/about/post-moj-guideline-2026.html
- ⚠️ 注記: ページ数（本文136・全143）は報道・解説記事に依拠（PDF本体での直接カウントは未実施）

### 文化庁「AIと著作権に関する考え方について」 — 検証: ✅ 間接確認

- 文化審議会著作権分科会法制度小委員会、令和6年（2024年）3月15日付
- 一次資料:
  - 掲載ページ: https://www.bunka.go.jp/seisaku/chosakuken/aiandcopyright.html
  - PDF本体: https://www.bunka.go.jp/seisaku/bunkashingikai/chosakuken/pdf/94037901_01.pdf

## 3. OSSのAI協働ポリシー

### Linux Kernel — 検証: ✅ **直接確認**（ファイル本体・コミット履歴を取得）

- `Documentation/process/coding-assistants.rst`。初版コミット 78d979db6cef（2026-01-06、作者 Sasha Levin、コミッタ Jonathan Corbet）、Linux 7.0 で正式収録
- トレーラ形式: `Assisted-by: AGENT_NAME:MODEL_VERSION [TOOL1] [TOOL2]`
- 原文: "AI agents MUST NOT add Signed-off-by tags. Only humans can legally certify the Developer Certificate of Origin (DCO)."
- 一次資料:
  - https://docs.kernel.org/process/coding-assistants.html
  - https://github.com/torvalds/linux/commit/78d979db6cef557c171d6059cbce06c3db89c7ee （直接確認）

### LLVM — 検証: ✅ **直接確認**（ポリシー全文・PRを取得）

- 「LLVM AI Tool Use Policy」。PR #154441 が2026-01-16にマージされ採択
- 一次資料:
  - https://llvm.org/docs/AIToolPolicy.html
  - https://github.com/llvm/llvm-project/blob/main/llvm/docs/AIToolPolicy.md （直接確認）
  - https://github.com/llvm/llvm-project/pull/154441 （直接確認）

### QEMU — 検証: ✅ **直接確認**（現行ポリシー本文・コミット履歴を取得）

- 拒否ポリシー明文化: コミット 3d40db0efc22（2025-06-24、Daniel Berrangé）で `docs/devel/code-provenance.rst` に追加
- 緩和提案: Paolo Bonzini「[PATCH] docs/devel: relax policy on AI-generated contributions」（qemu-devel、2026-05-28）— **2026-08-12時点で未マージ。現行ポリシーは全面拒否のまま**（master のファイル本文を直接確認）
- 一次資料:
  - https://www.qemu.org/docs/master/devel/code-provenance.html
  - https://github.com/qemu/qemu/commit/3d40db0efc22520fa6c399cf73960dced423b048 （直接確認）
  - 緩和提案（メーリングリスト）: https://lists.nongnu.org/archive/html/qemu-devel/2026-05/msg07614.html

### Fedora — 検証: ✅ 間接確認

- 「Policy on AI-Assisted Contributions」。Fedora Council が2025-10-22に承認
- 3本柱: 説明責任 / 透明性（`Assisted-by:` トレーラは git 管理下での開示の推奨手段）/ AI利用の制限（評価の最終判断者にしない）
- 一次資料:
  - 提案（Fedora Community Blog）: https://communityblog.fedoraproject.org/council-policy-proposal-policy-on-ai-assisted-contributions/
  - 議論スレッド: https://discussion.fedoraproject.org/t/council-policy-proposal-policy-on-ai-assisted-contributions/165092
- ⚠️ 注記: docs.fedoraproject.org 上の最終ポリシーの正確なパスは本環境から**未確認**

### OpenInfra / WordPress — 検証: ✅ 間接確認

- OpenInfra「Policy for AI Generated Content」: Assisted-By / Generated-By の2層ラベル — https://openinfra.org/legal/ai-policy/
- WordPress「AI Guidelines for WordPress」v0（2026-02-01） — https://make.wordpress.org/ai/handbook/ai-guidelines/

## 4. Web標準・経済的枠組み

### RSL (Really Simple Licensing) — 検証: ✅ 間接確認

- 2025-09-10 ローンチ、2025-12 に RSL 1.0 正式仕様公開。RSL Collective 運営
- 条件項目: free / attribution / subscription / pay-per-crawl / pay-per-inference
- 一次資料:
  - 仕様: https://rslstandard.org/rsl
  - ローンチ発表: https://rslstandard.org/press/rsl-standard
  - 1.0 正式仕様: https://rslstandard.org/press/rsl-1-specification-2025

### Cloudflare — 検証: ✅ 間接確認

- Pay Per Crawl（HTTP 402）: https://developers.cloudflare.com/ai-crawl-control/features/pay-per-crawl/what-is-pay-per-crawl/
- Human Native 買収発表（2026-01-15）: https://blog.cloudflare.com/human-native-joins-cloudflare/
- 2026-07-01 発表（Search/Agent/Training 3分類、2026-09-15 以降広告掲載ページで Training/Agent をデフォルトブロック）: https://blog.cloudflare.com/content-independence-day-ai-options/

### IETF AIPREF WG — 検証: ✅ 間接確認

- WG: https://datatracker.ietf.org/wg/aipref/about/
- draft-ietf-aipref-vocab: https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/
- draft-ietf-aipref-attach: https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/
- 2026-08 時点で RFC 未発行

### 学習データのライセンス情報欠落（Data Provenance Initiative） — 検証: ✅ 間接確認

- Longpre et al., "A Large-Scale Audit of Dataset Licensing & Attribution in AI"（Nature Machine Intelligence, 2024）
- 集約プラットフォーム上で人気データセットの70%超がライセンス未指定、50%超が誤分類。再注釈により未指定率30%まで低減
- 一次資料:
  - https://arxiv.org/pdf/2310.16787
  - https://www.nature.com/articles/s42256-024-00878-8

### 「主要AI企業の正式表明はない」 — 検証: ⚠️ 消極的確認のみ

- 「ない」ことの証明は原理的に不可能。2026-08-12時点の検索で、主要モデル提供者が RSL 等の宣言を尊重すると正式表明した報道・公式発表は**確認されていない**、という消極的確認に留まる
- 補助資料: Digiday（「これらの標準には強制力がなく、AI企業が尊重しない限り機能しない」）、Venable の分析（2026-06、「コミットしたモデル提供者はゼロ」）

---

## 検証ステータス一覧（引き継ぎ文書 §3 のチェックリストに対応）

| 項目 | 状態 |
|---|---|
| Thaler 最高裁上告棄却 | ✅ 確認（日付を 3/3→**3/2** に修正） |
| AI推進法（2025年成立） | ✅ 確認（令和7年法律第53号） |
| 法務省 解釈指針（2026-08-07） | ✅ 確認（ページ数のみ二次資料依拠） |
| 文化庁「AIと著作権に関する考え方について」 | ✅ 確認 |
| Fedora / Linux Kernel / LLVM の AI ポリシー原文 | ✅ 確認（Kernel・LLVM は原文直接確認。Fedora の3本柱の内容を修正） |
| QEMU | ✅ 確認（**「方針転換済み」→「緩和提案中・未マージ」に修正**） |
| RSL 仕様 | ✅ 確認（1.0 正式仕様は 2025-12 と補足） |
| Cloudflare Pay Per Crawl / 2026-09-15 変更 | ✅ 確認（デフォルトブロックの対象記述を修正） |
| Bartz v. Anthropic 和解 | ✅ 確認（最終承認 2026-07-20 を補足。作品数等は概数） |

---

*本文書は Claude Code による並行調査（2026-08-12）の結果を人間創作者の確認用に整理したものである。間接確認の項目は、公開環境からの最終アクセス確認を経てから確定扱いとすることを推奨する。*
