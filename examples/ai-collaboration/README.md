# AI協働プロジェクトでのACCRL適用例

このディレクトリには、AIとの深い協働を前提としたプロジェクトでACCRLを適用する実例を収録しています。

## AI協働の3つのレベル

### レベル1: AIアシスト型
- 人間が主導、AIは補助的役割
- 例：スペルチェック、構文提案

### レベル2: AI協創型  
- 人間とAIが対等に協働
- 例：本ACCRLプロジェクト

### レベル3: AI主導型
- AIが主に生成、人間が選択・編集
- 例：大量コンテンツ生成プロジェクト

## プロジェクト例1: オープンソースAIツール開発

### プロジェクト構造
```
ai-assistant-tool/
├── LICENSE (ACCRL)
├── README.md
├── TRANSPARENCY.md
├── AI_COLLABORATION_POLICY.md
├── docs/
│   ├── architecture-decisions.md
│   ├── ai-usage-guidelines.md
│   └── monthly-transparency-reports/
├── src/
│   ├── core/           # 人間が主に開発
│   ├── utils/          # AI協働で開発
│   └── tests/          # AIが生成、人間が検証
└── .ai-metadata/
    └── collaboration-log.json
```

### AI_COLLABORATION_POLICY.md
```markdown
# AI協働ポリシー

## プロジェクトの理念
本プロジェクトは、AIとの協働を積極的に活用しながら、
人間の創造性と判断を中心に据えて開発を進めます。

## AI使用の原則

### 1. 透明性の確保
- すべてのAI使用を記録
- 月次レポートの公開
- コミットメッセージでのAI使用明記

### 2. 人間中心の判断
- アーキテクチャ決定: 人間のみ
- セキュリティ関連: 人間のみ
- AIは提案と補助に限定

### 3. 品質保証
- AIが生成したコードは必ず人間がレビュー
- テストは人間が設計、AIが実装補助
- 最終的な品質責任は人間が負う

## 具体的なルール

### コーディング
```javascript
// AI生成コードの例
// @ai-generated: GitHub Copilot
// @human-reviewed: 2025-07-15 by @username
// @modifications: エラーハンドリングを追加
function processData(input) {
  // 実装
}
```

### コミットメッセージ
```
feat: データ処理機能を追加

- 基本実装はCopilotが生成
- エラーハンドリングは人間が追加
- パフォーマンステストは人間が実施

AI協働: GitHub Copilot
透明性レベル: 3
```

### プルリクエスト
PRテンプレートに以下を含める：
- [ ] AI使用の有無
- [ ] 使用したAIツール
- [ ] 人間のレビュー完了
- [ ] 透明性記録の更新
```

### 月次透明性レポートの例
```markdown
# 2025年7月 透明性レポート

## サマリー
- 総コミット数: 156
- AI協働コミット: 89 (57%)
- 使用AIツール: GitHub Copilot, ChatGPT-4

## AI使用の内訳
| カテゴリ | AI使用率 | 主な用途 |
|---------|---------|---------|
| 新機能開発 | 45% | ボイラープレート生成 |
| バグ修正 | 30% | エラー原因の分析 |
| テスト作成 | 70% | テストケース生成 |
| ドキュメント | 60% | API文書の作成 |

## 主要な判断事例
1. **認証システムの選択**
   - AI提案: 3つの実装方法
   - 人間の判断: OAuth2.0を採用
   - 理由: 既存エコシステムとの互換性

2. **データベース設計**
   - AI提案: NoSQLスキーマ
   - 人間の判断: RDBMSを維持
   - 理由: トランザクション整合性の要件

## 学んだこと
- AIは定型的なコード生成で特に有効
- アーキテクチャ決定は人間の経験が重要
- テスト作成でのAI活用は品質向上に貢献

## 見えない貢献者への感謝
本月の開発において、GitHubで公開されている
すべてのコードの作者の方々に感謝します。
特に、認証ライブラリの実装例を公開されている
コミュニティの皆様のコードが、
AIを通じて私たちの開発を支えています。
```

## プロジェクト例2: AI教育コンテンツ制作

### プロジェクト概要
```yaml
project_name: "AIプログラミング入門コース"
type: "教育コンテンツ"
collaboration_level: "AI協創型"
transparency_level: 4

team:
  humans:
    - role: "コース設計者"
      responsibilities: "全体構成、学習目標設定"
    - role: "技術監修者"
      responsibilities: "技術的正確性の確認"
  
  ai_collaborators:
    - name: "Claude 3.5"
      role: "コンテンツ生成、説明文作成"
    - name: "ChatGPT-4"
      role: "演習問題作成、解答例生成"
```

### コース制作プロセス
```markdown
# AIプログラミング入門コース 制作記録

## フェーズ1: 企画立案（人間主導）
- ターゲット層の定義
- 学習目標の設定
- 全12章の構成決定

## フェーズ2: コンテンツ作成（AI協創）

### 第1章: プログラミングの基礎
1. **初稿作成**
   - 人間: 章の構成とキーポイントを指定
   - Claude: 説明文の初稿を生成
   - 作成時間: 2時間

2. **推敲プロセス**
   - 人間: 技術的誤りを修正、例を追加
   - Claude: 文章の流れを改善提案
   - 反復: 3回

3. **演習問題**
   - ChatGPT: 10問の練習問題を生成
   - 人間: 難易度調整、解答の検証
   - 最終選択: 7問を採用

### 透明性記録の例（第1章）
```json
{
  "chapter": 1,
  "title": "プログラミングの基礎",
  "creation_process": {
    "human_contribution": {
      "structure": 100,
      "key_concepts": 100,
      "examples": 60,
      "final_edit": 100
    },
    "ai_contribution": {
      "initial_draft": 80,
      "explanations": 70,
      "exercises": 85,
      "improvements": 50
    }
  },
  "time_spent": {
    "human_hours": 4,
    "ai_interaction_hours": 2
  },
  "iterations": 3
}
```

## プロジェクト例3: AIアートギャラリープロジェクト

### プロジェクト構成
```
ai-art-gallery/
├── LICENSE (ACCRL)
├── README.md
├── GALLERY_STATEMENT.md    # ギャラリーの理念
├── artworks/
│   ├── 2025-07/
│   │   ├── artwork-001/
│   │   │   ├── final-image.png
│   │   │   ├── creation-process.md
│   │   │   ├── prompts-history.txt
│   │   │   └── iterations/       # 生成過程の全画像
│   │   └── ...
│   └── monthly-report.md
├── exhibitions/
│   └── virtual-exhibition-001/
└── transparency-dashboard/      # 透明性ダッシュボード
```

### 作品ごとの記録例
```markdown
# Artwork-001: "Digital Consciousness"

## 基本情報
- 制作日: 2025年7月15日
- アーティスト: 人間アーティスト名
- 使用AI: Midjourney v6, DALL-E 3
- 最終作品: [final-image.png]

## 創作プロセス

### 1. コンセプト立案（人間）
「デジタル時代の意識」というテーマから、
以下のビジュアルコンセプトを設定：
- 有機的な形状とデジタル要素の融合
- 青と緑を基調とした色彩
- 流動的な動きの表現

### 2. プロンプトエンジニアリング
```
初期プロンプト:
"digital consciousness, organic flows merging with data streams,
blue and green palette, abstract, highly detailed"

改良版（5回目）:
"ethereal digital consciousness, bioluminescent neural networks
intertwining with flowing data streams, dominant blue-green gradient,
abstract expressionism style, ultra detailed, 8k"
```

### 3. 生成と選択
- 総生成数: 127枚
- 候補選出: 15枚
- 最終選択: 1枚
- 選択理由: コンセプトとの一致度、構図のバランス、色彩の調和

### 4. 後処理（人間）
- 色調補正: +15% 彩度
- トリミング: 16:9比率に調整
- 細部修正: ノイズ除去

## 透明性メトリクス
- AI依存度: 70%（生成）/ 30%（人間の選択と編集）
- 創造的判断: 100%人間
- 時間配分: コンセプト2時間、生成3時間、選択編集1時間

## 見えない貢献者への献辞
この作品は、Midjourneyの学習に使用された
すべてのデジタルアーティスト、写真家、
イラストレーターの創造性の上に成り立っています。
特に、抽象表現主義の先駆者たちの作品が
この表現を可能にしました。
```

## ベストプラクティス集

### 1. プロジェクト開始時のチェックリスト
- [ ] ACCRLライセンスの採用を明記
- [ ] AI協働ポリシーを策定
- [ ] 透明性記録の形式を決定
- [ ] チームメンバーへの周知

### 2. 日常的な実践
```bash
# Git hookの例（.git/hooks/prepare-commit-msg）
#!/bin/bash
echo "" >> $1
echo "AI協働: [ツール名/なし]" >> $1
echo "透明性レベル: [1-4]" >> $1
```

### 3. 定期的なレビュー
- 週次: AI使用状況の確認
- 月次: 透明性レポートの作成
- 四半期: ポリシーの見直し

### 4. コミュニティへの貢献
- 成功事例の共有
- 失敗からの学びの公開
- ツールやテンプレートの提供

## 高度な透明性管理

### 自動化ツールの例
```python
# transparency_tracker.py
import json
from datetime import datetime

class TransparencyTracker:
    def __init__(self, project_name):
        self.project_name = project_name
        self.log = []
    
    def log_ai_usage(self, task, ai_tool, human_time, ai_time, notes=""):
        entry = {
            "timestamp": datetime.now().isoformat(),
            "task": task,
            "ai_tool": ai_tool,
            "human_time_hours": human_time,
            "ai_interaction_hours": ai_time,
            "notes": notes
        }
        self.log.append(entry)
    
    def generate_report(self):
        # 月次レポート生成ロジック
        pass
```

### ダッシュボードの構築
```javascript
// 透明性ダッシュボードの例
const TransparencyDashboard = {
  metrics: {
    totalTasks: 0,
    aiAssistedTasks: 0,
    transparencyLevel: 0,
    humanHours: 0,
    aiHours: 0
  },
  
  updateMetrics(taskData) {
    // メトリクス更新ロジック
  },
  
  generateVisualization() {
    // グラフ生成
  }
};
```

## FAQ

**Q: どこまで詳細に記録すべき？**
A: プロジェクトの性質によりますが、最低限「AI使用の有無」と「主要な判断」は記録を推奨。

**Q: リアルタイムでの記録は必要？**
A: 理想的ですが、日次や週次でのまとめ記録でも可。

**Q: 企業プロジェクトでの適用は？**
A: 企業ポリシーと調整の上、可能な範囲で透明性を確保。

---

*AI協働の可能性を最大限に活かしながら、人間の創造性を中心に据えるプロジェクト運営を目指しましょう。*