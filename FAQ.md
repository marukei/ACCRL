# よくある質問（FAQ）

[日本語](#japanese) | [English](#english)

> 本FAQは v0.3-PROTOTYPE（2026-09-29）に合わせて改訂した。2025-07 版の記述のうち、現在の設計と矛盾していたもの（「契約法上有効」「執行力はコミュニティの採用から生まれる」「普遍的な概念を明確にしているだけ」等）は削除した。旧版は git の履歴に残っている。

---

<a name="japanese"></a>
## 日本語

### このプロジェクトについて

**Q: 何を目指しているのですか？ 普及ですか？**

A: 普及は目指していません。目的は、AI時代の創作倫理について「この時期にこういう問いを立てた文書があった」と後年参照できる記録を残すことです。採用の数や話題性を成功の指標にしません（[design-axis.md](./docs/design-axis.md) §0）。

**Q: 既存のライセンス（MIT、GPL、Creative Commons）ではだめなのですか？**

A: 既存のライセンスは著作権の上に成り立っています。LLM が生成したコードのように、著作権が成立しない部分を含む作品では、ライセンスは許諾するものを持たず、空振りします。ACCRL の第II部（誓約）は規範であって著作権に依存しないため、著作権のない部分にも規範として及びます（[design-axis.md](./docs/design-axis.md) §5）。ACCRL は既存のライセンスを置き換えるものではなく、それらが扱わない領域を扱います。

### 法的な性質

**Q: 法的強制力はありますか？**

A: 利用者に対しては、ありません。これは欠陥ではなく設計です。

- **第I部（許諾と約束）** は法的に作用します。ただし拘束されるのは採用者（自分の作品に ACCRL を適用した人）だけです。採用者は、撤回できない許諾と、誓約を理由に訴えないことを約束します
- **第II部（誓約と呼びかけ）** は契約ではなく、誰にも法的義務を課しません

つまり、ACCRL で法的に拘束されるのは、自ら選んで採用した人だけです。

**Q: 強制力がないのに「ライセンス」と名乗るのはなぜですか？**

A: ライセンスと宣言することで、利用者に「この作品には規範がある」と意識させるためです。強制力の強弱はライセンスの資格要件ではありません。ライセンスフリーも立派なライセンスです。ACCRL は「器はライセンス、実態は誓約」という設計をとっています（[決定の記録](./docs/transparency-records/2026-08-12-vessel-decision.md)）。

**Q: 著作者人格権はどうなりますか？**

A: 放棄も譲渡もされず、創作者のもとに残ります。ACCRL は人格権を「人を守る盾」として残し、第II部の誓約を強制する手段としては使いません。ただし、法律が人格権として保護する範囲（氏名表示、同一性保持、名誉声望）では、誓約の一部が法律上の義務と重なります。重なった部分で働くのは ACCRL ではなく法律です（v0.3 第5条）。改変の許諾を実質的なものにしたい採用者は、任意の不行使宣言（付録B）を付すことができます。

**Q: 誓約に従わない利用があったらどうなりますか？**

A: 許諾は終了しませんし、採用者は誓約を理由に訴えません。ACCRL の応答は、対話と是正の呼びかけだけです。誓約に沿うかどうかを判定する権限は、誰にも与えられていません（v0.3 第11条）。ただし、法律上の権利（人格権など）の侵害に当たる場合、それは法律の問題として残ります。

### AIとの関係

**Q: AIの学習に使ってよいのですか？**

A: 既定では、第I部の許諾にAI学習が含まれます。そのうえで、学習する人に、見えない貢献者への敬意と、学習に用いたことの開示を呼びかけています。採用者は、AI学習を許諾の範囲から除く留保を付すこともできます。留保の法的効果は各国の法律によって決まり、効果を持たない国（日本など、許諾なく学習できる国）もあります。留保は、人が読める形に加えて、機械が読める形でも示すことをおすすめします（v0.3 第2.2条・第9条）。

**Q: AI開発者を拘束できるのですか？**

A: できない場合が多い、と条文自身が書いています。AI開発者は多くの場合、ライセンスの被許諾者の立場に立たないからです。ACCRL はこの限界を隠しません（[open-questions.md](./docs/open-questions.md) Q4）。

**Q: AIは誓約できますか？**

A: できません。誓約できるのは人間だけです。AIと協働して作った作品でも、誓約するのは人間の採用者です（v0.3 第1条4号）。

**Q: `Assisted-by:` トレーラとの関係は？**

A: 両立します。AIを使った事実だけを示す形（`Assisted-by: LLM`）は透明性レベル1、使ったAIシステムやモデルを示す形はレベル2に当たります（v0.3 第10条）。

### 使い方

**Q: 使うにはどうすればよいですか？**

A: 一行で表明できます。

```
SPDX-License-Identifier: LicenseRef-ACCRL-0.3
```

README には次のように書けます。

```
本作品は AI Collective Creativity Respect License (ACCRL) v0.3 の下で公開し、その誓約を行います。
```

採用の表明そのものが、第6条の誓約（協働の透明性、見えない貢献者への敬意、他者の創作的人格の尊重、強制しないこと）の表明になります。詳しくは [v0.3 付録A](./LICENSE-v0.3-PROTOTYPE.md) をご覧ください。

**Q: ACCRL の作品を改変したら、改変物も ACCRL にしなければなりませんか？**

A: いいえ。派生物にどのライセンスを使うかは自由です。ACCRL が呼びかけるのは、原作への帰属と、誓約が存在することを示し続けること（敬意の継承）だけです。ライセンスの継承は求めません（v0.3 第8条）。

**Q: 他のライセンスと併用できますか？**

A: できます。ACCRL は、他のライセンスの下にある著作物との組み合わせを妨げません。

### 理念

**Q: 日本中心的ではありませんか？**

A: ACCRL は日本的な人格権思想を出発点に持ちます。ただし、それが普遍的に正しいとは主張しません。異なる法域や文化圏の創作倫理と共存し、選択肢の一つとして自らを置いています。普遍性の主張は、それ自体が一種の強制だからです（[design-axis.md](./docs/design-axis.md) §2.4）。

**Q: 批判は受け付けていますか？**

A: 「思想が不明瞭だ」「内部で矛盾している」という内在的な批判を歓迎します。v0.3 は、まさにそうした内在的批判から生まれました（[legal-analysis/non-coercive-design-2026.md](./docs/legal-analysis/non-coercive-design-2026.md)）。一方、「使われていない」「法的に不利だ」という外形的な評価は、このプロジェクトの目的に対して的を外しています。

---

<a name="english"></a>
## English

### About the project

**Q: What is the goal? Adoption?**

A: No. The goal is to leave a record — a document that, years from now, can be pointed to as "someone asked these questions at this moment." Adoption and attention are not measures of success ([design-axis.md](./docs/design-axis.md) §0, Japanese).

**Q: Why not just use MIT, GPL, or Creative Commons?**

A: Existing licenses rest on copyright. Where a work contains parts in which no copyright subsists — such as LLM-generated code — a license has nothing to grant there. ACCRL's Part II (the pledge) is a norm that does not depend on copyright, so it reaches those parts as a norm. ACCRL does not replace other licenses; it covers ground they do not.

### Legal nature

**Q: Is it legally enforceable?**

A: Not against users. That is by design.

- **Part I (grant and promises)** is legally operative, but it binds only the adopter — the person who applied ACCRL to their own work. The adopter promises an irrevocable grant and not to sue on the basis of the pledge.
- **Part II (pledge and invitation)** is not a contract and imposes no legal obligation on anyone.

The only person legally bound by ACCRL is the one who chose to adopt it.

**Q: Why call it a "license" if it has no coercive force?**

A: Declaring it a license makes users aware that the work carries norms. Coercive force is not a requirement for being a license. ACCRL is "a license in form, a covenant in substance."

**Q: What happens to moral rights?**

A: They are neither waived nor transferred; they remain with the creator as a shield. ACCRL does not use them to enforce the pledge. Where the law protects moral rights (attribution, integrity, honor), parts of the pledge overlap with legal duties — in that overlap, it is the law that operates, not ACCRL. An adopter may attach an optional non-assertion declaration (Appendix B).

**Q: What if someone does not follow the pledge?**

A: The grant does not terminate, and the adopter does not sue on the basis of the pledge. ACCRL's only response is dialogue. No one is given authority to judge conformity.

### AI

**Q: May the work be used for AI training?**

A: By default, yes — Part I includes AI training. Those who train are invited to respect the invisible contributors and to disclose the use. An adopter may reserve AI training out of the grant; the legal effect of the reservation depends on each jurisdiction's law. Expressing the reservation in machine-readable form as well is recommended.

**Q: Can AI make the pledge?**

A: No. Only humans can pledge.

**Q: How does this relate to the `Assisted-by:` trailer?**

A: They are compatible. `Assisted-by: LLM` corresponds to transparency level 1; naming the AI system or model corresponds to level 2.

### Using it

**Q: How do I adopt it?**

A: In one line:

```
SPDX-License-Identifier: LicenseRef-ACCRL-0.3
```

The act of adopting is itself the pledge. See [v0.3 Appendix A](./LICENSE-v0.3-PROTOTYPE.md) (Japanese; English translation planned).

**Q: Must derivatives also use ACCRL?**

A: No. ACCRL invites you to carry forward respect — attribution and notice of the pledge — not the license.

**Q: Isn't this Japan-centric?**

A: It starts from Japanese thinking on moral rights, but does not claim universality. It offers itself as one option among the creative ethics of other jurisdictions and cultures.

---

## さらに質問がある場合 / More questions

- GitHub Issues / Discussions
