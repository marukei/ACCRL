# ソフトウェアプロジェクトでのACCRL適用例

このディレクトリには、ソフトウェア開発プロジェクトでACCRLを適用する実例を収録しています。

## 基本的な適用方法

### 1. ライセンスファイルの配置

プロジェクトルートに`LICENSE`ファイルを配置：
```
PROJECT_ROOT/
├── LICENSE          # ACCRLライセンス文
├── TRANSPARENCY.md  # 透明性記録
├── README.md
└── src/
```

### 2. READMEでの表記

```markdown
## ライセンス

本プロジェクトは [AI Collective Creativity Respect License (ACCRL)](https://github.com/yourusername/ACCRL) の下で公開されています。

### AI協働の開示
- 使用AI: GitHub Copilot, ChatGPT-4
- 協働レベル: AIアシスト型（人間主導）
- 透明性レベル: 3（詳細は[TRANSPARENCY.md](./TRANSPARENCY.md)参照）

### 謝辞
本プロジェクトの開発にあたり、AIの学習に貢献されたすべてのオープンソース開発者の方々に深く感謝いたします。
```

### 3. 透明性記録の例

`TRANSPARENCY.md`:
```markdown
# 透明性記録

## プロジェクト情報
- プロジェクト名: ExampleApp
- 開発期間: 2025年1月〜現在
- 主要開発者: 山田太郎

## AI協働の詳細

### 使用AIツール
1. **GitHub Copilot**
   - バージョン: 1.x
   - 使用範囲: コード補完、ボイラープレート生成
   - 使用頻度: 開発時間の約30%

2. **ChatGPT-4**
   - 使用目的: アーキテクチャ設計の相談、エラー解決
   - 使用頻度: 週2-3回程度

### 人間の創作的判断

#### アーキテクチャ決定
- **選択**: マイクロサービスアーキテクチャ
- **理由**: スケーラビリティと保守性を重視
- **AIの役割**: 各アーキテクチャパターンの長所短所を整理
- **最終判断**: 人間がプロジェクト要件に基づいて決定

#### 主要アルゴリズム
- **課題**: 効率的なデータ処理アルゴリズムの実装
- **AIの提案**: 3つのアルゴリズムを提示
- **人間の判断**: ベンチマークテストを実施し、最適なものを選択

### コード生成の内訳（推定）
- 人間が直接記述: 60%
- AIが生成し人間が修正: 30%
- AIが生成しそのまま使用: 10%

## 創作プロセスの記録

### 2025年7月の開発記録
- 新機能の設計において、ChatGPTと5回の対話セッション
- Copilotの提案を採用: 15件
- Copilotの提案を修正して採用: 23件
- Copilotの提案を却下: 8件

### 判断の具体例
1. **認証システムの実装**
   - AI提案: JWT認証
   - 人間の判断: OAuth2.0を選択（既存システムとの統合のため）

2. **データベース設計**
   - AI提案: NoSQL (MongoDB)
   - 人間の判断: PostgreSQLを選択（ACIDトランザクションが必要）

## 今後の方針
- AI使用の割合は現状維持
- 重要な設計判断は必ず人間が行う
- 月次で透明性記録を更新

---
最終更新: 2025年7月15日
```

## 実装パターン集

### パターン1: オープンソースライブラリ

```javascript
/**
 * ACCRL Licensed Library Example
 * 
 * @license ACCRL-1.0
 * @author 人間開発者名
 * @ai-collaborator GitHub Copilot
 * @transparency-level 2
 */

// ライブラリのメタデータ
export const metadata = {
  license: 'ACCRL-1.0',
  aiCollaboration: {
    used: true,
    tools: ['GitHub Copilot'],
    level: 'assistive'
  },
  acknowledgment: '本ライブラリはAIとの協働により開発されました。'
};

// 実際のコード
export function exampleFunction(param) {
  // 実装
}
```

### パターン2: エンタープライズアプリケーション

大規模プロジェクトでは、より詳細な管理が必要：

1. **プロジェクト構造**
```
enterprise-app/
├── LICENSE
├── TRANSPARENCY.md
├── docs/
│   ├── ai-collaboration-policy.md
│   └── decision-log.md
├── src/
└── .ai-transparency/
    ├── 2025-07-usage.json
    └── templates/
```

2. **AI使用ポリシー文書**
```markdown
# AI協働ポリシー

## 許可される使用
- コードレビューの補助
- ドキュメント生成の支援
- 単体テストの生成

## 禁止事項
- セキュリティ関連コードのAI生成
- 個人情報を含むコードでのAI使用
- 重要なビジネスロジックの完全なAI依存
```

### パターン3: 個人プロジェクト

個人開発でも透明性は重要：

```markdown
# 個人プロジェクトでのACCRL適用

## 最小限の実装
READMEに以下を追加：

「本プロジェクトはChatGPTの支援を受けて開発しました。
AIの学習に貢献したすべての開発者に感謝します。」

## 推奨される実装
- 月次でAI使用状況をログ
- 重要な判断は記録を残す
- 可能な限り透明性を保つ
```

## ベストプラクティス

### 1. 継続的な記録
- AI使用は都度記録
- 月次サマリーの作成
- 年次レビューの実施

### 2. チーム開発での運用
- AI使用ガイドラインの策定
- コードレビューでの確認
- 定期的な振り返り

### 3. コミュニティへの還元
- 学んだことの共有
- ツールの開発と公開
- 事例の提供

## ツールとテンプレート

### 透明性記録の自動生成
```bash
# 仮想的なCLIツール例
accrl-transparency generate --project ./my-project --output TRANSPARENCY.md
```

### メタデータの管理
```json
{
  "accrl": {
    "version": "1.0",
    "project": "ExampleApp",
    "ai_tools": [
      {
        "name": "GitHub Copilot",
        "version": "1.x",
        "usage": "code_completion"
      }
    ],
    "transparency_level": 3,
    "last_updated": "2025-07-15"
  }
}
```

## FAQ

**Q: すべてのAI使用を記録する必要がありますか？**
A: 完璧である必要はありません。重要なのは誠実な努力と継続的な改善です。

**Q: 既存プロジェクトへの適用は？**
A: 過去に遡る必要はありません。今から始めることが重要です。

**Q: 商用プロジェクトでも使えますか？**
A: はい。ACCRLは商用利用を制限しません。

---

*これらの例は、実際のプロジェクトでの適用を想定して作成されました。*