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
- トレーラ形式: `Assisted-by: AGENT_NAME:MODEL_VERSION [TOOL1] [TOOL2]`（〔2026-09 訂正〕v7.3-rc1 以降は `Assisted-by: LLM [TOOL1] [TOOL2]`。下記「2026-09 追補」参照）
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

---

# 2026-09 追補（2026-09-29 検証）

[2026-09-review.md](./2026-09-review.md) の資料。検証水準の定義は冒頭と同じ。今回の調査環境では、直接取得できたのは GitHub 上の公式リポジトリだけで、政府・裁判所・標準化団体のサイトはすべて遮断されていた。そのため、GitHub 以外の項目は最高でも間接確認にとどまる。

## A. 直接確認（一次資料本体を取得）

| 項目 | 資料 |
|---|---|
| Linux `Assisted-by: LLM` への簡素化（816d9992d9、v7.3-rc1） | https://github.com/torvalds/linux/commit/816d9992d9ed434ec52cfbd63080d518e535a41b |
| Linux バグ修正手順の追補（3d7c44f737、v7.2） | https://github.com/torvalds/linux/commit/3d7c44f73765d98665fb97a4fb89c002c88ba1b9 |
| Linux `generated-content.rst` | https://github.com/torvalds/linux/blob/master/Documentation/process/generated-content.rst |
| QEMU `AGENTS.md`（3ab8a155、2026-09-08） | https://github.com/qemu/qemu/commit/3ab8a15569afa9ffd89971dff34d0636d48cae3c |
| QEMU code-provenance.rst（緩和未マージ、master 2026-09-27） | https://github.com/qemu/qemu/blob/master/docs/devel/code-provenance.rst |
| ASF Generative Tooling Guidance の改訂（`Co-authored-by:` 追加、2026-09-29） | https://github.com/apache/www-site/commit/fe7423d8b7d8d70a49249c696e406a5c6bca5717 |
| IETF AIPREF ドラフト（vocab-08、2026-09-14） | https://github.com/ietf-wg-aipref/drafts |
| Cloudflare 2026-07-01 changelog（新規ドメインが対象） | https://github.com/cloudflare/cloudflare-docs |
| CC Signals（v0.1 草案） | https://github.com/creativecommons/cc-signals |
| W3C TDMRep（CG Final Report） | https://github.com/w3c/tdm-reservation-protocol |
| C2PA 2.4 | https://github.com/c2pa-org/specifications |
| llms.txt v2 | https://github.com/AnswerDotAI/llms-txt |
| SPDX 3.x モデル | https://github.com/spdx/spdx-3-model |
| Contributor Covenant 3.0 本文 | https://github.com/EthicalSource/contributor_covenant |
| CC BY 4.0 §2(b)(1)・§8(a)、MPL 2.0、CC BY-SA 4.0 の本文（SPDX 収録） | https://github.com/spdx/license-list-data |
| SemVer 2.0.0 / Conventional Commits 1.0.0 本文 | https://github.com/semver/semver 、https://github.com/conventional-commits/conventionalcommits.org |

Rust、Node.js、CPython、curl、Ghostty、git、Servo、LLVM の AI ポリシーも、各リポジトリ上の原文を直接確認した（URL は各プロジェクトのリポジトリ）。

## B. 間接確認（検索インデックスと複数の独立報道の照合）

### 米国
- In re OpenAI Copyright Infringement Litigation（No. 1:25-md-03143）の司法省意見書（2026-09-01）: https://www.courtlistener.com/docket/69879510/in-re-openai-inc-copyright-infringement-litigation/ 、WaPo 2026-09-02、Axios 2026-09-19
- Doe v. GitHub（9th Cir. No. 24-7700、2026-09-16）: https://www.courthousenews.com/wp-content/uploads/2026/09/doe-vs-github-ninth-circuit.pdf 、https://www.authorsalliance.org/2026/09/23/resolving-an-interlocutory-appeal-ninth-circuit-affirms-dismissal-of-section-1202-dmca-claims-in-ongoing-doe-v-github-litigation/
- Kadrey v. Meta: https://www.courtlistener.com/docket/67569326/kadrey-v-meta-platforms-inc/
- Thomson Reuters v. ROSS: https://www.courtlistener.com/docket/70622297/thomson-reuters-enterprise-centre-gmbh-v-ross-intelligence-inc/
- Concord v. Anthropic / Sony・Warner Chappell の提訴: https://www.courtlistener.com/docket/68889092/concord-music-group-inc-v-anthropic-pbc/ 、TechCrunch 2026-08-29
- NO FAKES Act（S.4591）: https://www.congress.gov/bill/119th-congress/senate-bill/4591

### EU・加盟国
- GPAI 行動規範: https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai （著作権章 Measure 1.3 の文言は、GitHub 上の第三者による全文転載3件の一致で確認）
- AI Act の執行権限: https://ai-act-service-desk.ec.europa.eu/en/ai-act/faq/commissions-enforcement-powers-related-ai-act-obligations-providers-most-advanced-models
- 初の情報提供要求（2026-09-01）: https://agenceurope.eu/en/bulletin/article/13929/31/european-commission-sends-first-requests-for-information-to-more-than-30-ai-providers
- オプトアウト方式の意見募集: https://digital-strategy.ec.europa.eu/en/consultations/commission-launches-consultation-protocols-reserving-rights-text-and-data-mining-under-ai-act-and
- Kneschke v. LAION（OLG Hamburg 5 U 104/24、BGH I ZR 281/25）: https://www.twobirds.com/en/insights/2025/germany/higher-regional-court-hamburg-confirms-ai-training-was-permitted-(kneschke-v,-d-,-laion) 、https://www.profifoto.de/szene/notizen/2026/09/03/bgh-erwaegt-gang-zum-eugh/
- GEMA v. OpenAI（LG München I 42 O 14139/24）: https://www.justiz.bayern.de/gerichte-und-behoerden/landgericht/muenchen-1/presse/2025/11.php
- GEMA v. Suno（LG München I 42 O 763/25）: https://www.justiz.bayern.de/gerichte-und-behoerden/landgericht/muenchen-1/presse/2026/16.php
- デンマーク東部高裁 BS-55572/2025-OLR: https://jura360.dk/artikel/high-court-rules-natural-language-opt-out-of-text-and-data-mining-insufficient
- デンマーク肖像・声法案: https://www.europarl.europa.eu/thinktank/en/document/EPRS_ATA(2026)782611

### 英国
- Getty v. Stability AI（[2025] EWHC 2863 (Ch)）と控訴許可: https://www.hsfkramer.com/notes/ip/2025-12/getty-granted-permission-to-appeal-secondary-copyright-infringement-findings-in-getty-v-stability-ai
- 政府の報告書（2026-03-18）: https://questions-statements.parliament.uk/written-statements/detail/2026-03-18/hcws1416
- CMA の Google 向け行為要件: https://www.gov.uk/find-digital-markets-measures/google-search-publisher-conduct-requirement

### 日本
- プリンシプル・コード（2026-08-25）: https://current.ndl.go.jp/car/284024 、https://www.cas.go.jp/jp/seisakukaigi/titeki2/ai_kentoukai/kaisai/pdf/ai_principle_code.pdf
- 知的財産推進計画2026: https://www.cas.go.jp/jp/seisakukaigi/titeki2/260612/keikaku_all.pdf
- 不正競争防止小委員会（第29回）: https://www.meti.go.jp/shingikai/sankoshin/chiteki_zaisan/fusei_kyoso/029.html
- AI事業者ガイドライン第1.2版: https://www.meti.go.jp/shingikai/mono_info_service/ai_shakai_jisso/20260331_report.html

### OSS・その他
- Debian 一般決議 2026-002（LWN 経由。条文原文と票数は未確認）
- Software Freedom Conservancy の推奨（2026-06-18）: https://sfconservancy.org/llm-gen-ai/llm-backed-generative-ai-recommendations.html
- CC の方針更新（2026-04-23）: https://creativecommons.org/2026/04/23/update-on-cc-signals-what-changed-and-why/

### 非強制ライセンス設計の先行例（[legal-analysis/non-coercive-design-2026.md](./legal-analysis/non-coercive-design-2026.md) の資料）
- Jacobsen v. Katzer, 535 F.3d 1373 (Fed. Cir. 2008)、MDY v. Blizzard, 629 F.3d 928 (9th Cir. 2010)、TransCore v. ETC, 563 F.3d 1271 (Fed. Cir. 2009)
- Open COVID Pledge FAQ: https://opencovidpledge.org/faqs/
- ODC Attribution-Sharealike Community Norms: https://opendatacommons.org/norms/odc-by-sa/
- 東京地判令和3年10月12日（令和3年(ワ)第5285号、CC BY-SA 写真のクレジット欠落で人格権侵害の賠償を認容）: https://www.hanketsu.jiii.or.jp/hanketsu/jsp/hatumeisi/news/202211news.pdf

## C. 未確認（今回確認できなかったもの）

- Cloudflare の 2026-09-15 の既定変更が実施されたことを告げる公式発表
- 欧州司法裁判所 C-250/25 の法務官意見の有無と内容
- BGH（I ZR 281/25）の付託決定・判決
- EU の「一般に合意された機械可読オプトアウト方式」リストの公表
- AI Office の情報提供要求の宛先企業名
- FSF・FSFE・OSI のLLM生成コードに関する見解の中身
- LLM による学習コードの逐語的再現とライセンス汚染に関する研究文献
- Linux Foundation / DCO 側の AI に関する公式見解
- Debian 一般決議の条文原文と票数
- 学説として挙げられた文献（Fauchart & von Hippel 2008、Oliar & Sprigman 2008 等）の書誌
