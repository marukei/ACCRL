# 既知の課題と議論の呼びかけ / Known Issues and Call for Discussion

> **2026-08 追記**: 本文書は2025年7月時点の課題一覧である。13ヶ月後の再検討で「本丸」と判断した設計課題は [docs/open-questions.md](./docs/open-questions.md) に絞り込んで整理した。あわせて参照のこと。
>
> **Note (2026-08)**: This document reflects the issues as of July 2025. The core design questions identified in the 13-month review are consolidated in [docs/open-questions.md](./docs/open-questions.md).

## 💡 本文書の目的 / Purpose of This Document

このプロジェクトは**理念先行型プロトタイプ**です。完璧なソリューションではなく、AI時代の創作倫理について具体的な議論を促すための叩き台として公開しています。

This project is an **idealism-first prototype**. Rather than a perfect solution, it serves as a concrete starting point for discussion about creative ethics in the AI era.

## 🚨 認識している脆弱性 / Acknowledged Vulnerabilities

### 1. 法的精度の問題 / Legal Precision Issues

**日本語：**
- 「人格権」概念の国際的解釈に曖昧さが残る
- Common Law圏での実効性が不明確
- 実際の法廷での有効性について十分な検証がない

**English:**
- International interpretation of "moral rights" remains ambiguous
- Effectiveness in Common Law jurisdictions is unclear
- Insufficient verification of validity in actual legal proceedings

**💬 求める議論：**
- 各国の法制度における人格権の実装可能性
- 既存のライセンス体系との整合性
- 法的リスクの具体的な評価

### 2. 実装の複雑さ / Implementation Complexity

**日本語：**
- 透明性レベル1-4の判定基準が主観的
- 「見えない貢献者」への具体的な配慮方法が不明確
- 既存プロジェクトへの適用コストが高い

**English:**
- Transparency levels 1-4 have subjective criteria
- Specific methods for acknowledging "invisible contributors" are unclear
- High adoption costs for existing projects

**💬 求める議論：**
- より客観的な評価基準の提案
- 実践的な実装ガイドラインの共同開発
- 段階的導入方法の検討

### 3. 文化的・思想的な課題 / Cultural and Philosophical Challenges

**日本語：**
- 日本的価値観の国際的な受容性への疑問
- 理想主義vs現実主義の対立
- 既存OSS文化との摩擦の可能性

**English:**
- Questions about international acceptance of Japanese values
- Conflict between idealism and realism
- Potential friction with existing OSS culture

**💬 求める議論：**
- 文化的多様性を尊重した普遍的な表現方法
- 理念と実用性のバランスの取り方
- 既存コミュニティとの建設的な対話

### 4. 技術的実装の課題 / Technical Implementation Challenges

**日本語：**
- AI協働プロセスの標準化が困難
- 大規模プロジェクトでの透明性確保の現実性
- 既存ツールチェーンとの統合性

**English:**
- Difficulty in standardizing AI collaboration processes
- Feasibility of ensuring transparency in large-scale projects
- Integration with existing tool chains

**💬 求める議論：**
- 技術的な実装パターンの提案
- 既存ツールとの統合アプローチ
- 自動化可能な部分の特定

## 🎯 現在の位置づけ / Current Status

### これはv1.0.0ではありません / This is NOT v1.0.0

**正しい位置づけ：**
- **概念実証（Proof of Concept）**
- **議論の叩き台（Discussion Starter）**
- **実験的プロトタイプ（Experimental Prototype）**

**Correct positioning:**
- **Proof of Concept**
- **Discussion Starter**
- **Experimental Prototype**

### 何を求めているか / What We're Looking For

**建設的な批判を歓迎します：**
- 法的な問題点の具体的な指摘
- 実装上の課題の詳細な分析
- 代替案や改善提案
- 文化的な観点からの意見

**We welcome constructive criticism:**
- Specific legal concerns
- Detailed analysis of implementation challenges
- Alternative proposals and improvements
- Cultural perspectives

## 🤝 議論への参加方法 / How to Participate in Discussion

### 1. Issues - 具体的な問題提起 / Specific Problem Reports
- バグや誤記の報告
- 明確な改善提案
- 実装上の技術的課題

### 2. Discussions - 深い議論 / Deep Discussions
- 哲学的・倫理的な議論
- 長期的な方向性の検討
- 文化的な違いについての対話

### 3. Pull Requests - 具体的な改善 / Concrete Improvements
- 条文の修正提案
- 文書の改善
- 実装例の追加

## 📊 なぜこのプロジェクトが必要か / Why This Project Matters

### 問題の現実性 / Real Problems We Face

**日本語：**
1. AI学習データの著作者への配慮が不十分
2. AI協働作品の権利関係が不明確
3. 従来のライセンスでは対応できない新しい創作形態

**English:**
1. Insufficient consideration for authors of AI training data
2. Unclear rights relationships in AI collaborative works
3. New forms of creation that traditional licenses cannot address

### 期待される効果 / Expected Impact

**完璧な解決策ではなく、以下を目指します：**
- 問題の可視化と議論の活性化
- より良い解決策への道筋
- 創作倫理の進化への貢献

**We aim for the following, not perfect solutions:**
- Visualization of problems and activation of discussion
- Pathways to better solutions
- Contribution to the evolution of creative ethics

## 🔬 実験的な取り組み / Experimental Approaches

### 現在試行中 / Currently Testing

1. **透明性記録の実践** - すべての意思決定プロセスを公開
2. **多様な協働規律** - 人間とAI、異なるAI間の協働方法
3. **段階的実装** - 理念から実装への段階的アプローチ

### 求める協力 / Seeking Collaboration

- **法律専門家** - 各国の法制度における実現可能性の検証
- **開発者** - 実装上の課題と解決策の提案
- **哲学者・倫理学者** - 概念的な枠組みの洗練
- **国際的な視点** - 文化的多様性を考慮した改善案

## 📋 今後の方向性 / Future Directions

### 短期目標（3-6ヶ月）/ Short-term Goals (3-6 months)
- [ ] 法的精度の向上
- [ ] 実装ガイドラインの詳細化
- [ ] 小規模な実証実験

### 中期目標（6-12ヶ月）/ Medium-term Goals (6-12 months)
- [ ] 国際的な専門家レビュー
- [ ] 実際の採用事例の蓄積
- [ ] より実用的なバージョンの開発

### 長期目標（1-2年）/ Long-term Goals (1-2 years)
- [ ] 標準化団体への提案
- [ ] 業界での議論の促進
- [ ] より包括的な解決策への発展

## 🎉 あなたの参加を歓迎します / Your Participation is Welcome

このプロジェクトの成功は、多様な視点からの建設的な議論にかかっています。完璧でないからこそ、あなたの知見と経験が必要です。

The success of this project depends on constructive discussion from diverse perspectives. Precisely because it's imperfect, we need your insights and experience.

**一緒に、AI時代にふさわしい創作倫理を築いていきましょう。**

**Let's build creative ethics suitable for the AI era together.**

---

## 関連する透明性記録 / Related Transparency Records

この文書の背景となる議論プロセス：
- [防御的構造構築議論](./docs/transparency-records/2025-07-15-defensive-structure.md)
- [謙虚なリポジショニング](./docs/transparency-records/2025-07-16-humility-repositioning.md)
- [最終準備作業](./docs/transparency-records/2025-07-16-final-preparations.md)

---

*この文書は、人間とAI（Claude）の協働により作成されました。脆弱性を認めることも、透明性の実践の一部です。*

*This document was created through human-AI collaboration. Acknowledging vulnerabilities is part of practicing transparency.*