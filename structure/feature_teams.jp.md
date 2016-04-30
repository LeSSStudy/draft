---
layout: mechanics
title:  フィーチャーチーム
order: 10
---

<!---
A feature team, shown in Figure 1, is a long-lived, cross-functional, cross-component team that completes many end-to-end customer features—one by one.
--->
図1に示すフィーチャーチームは、ひとつづつ、たくさんの顧客のフィーチャーをエンドツーエンドで作り上げる、寿命が長く、機能横断的で、コンポーネント横断チームです。

<figure>
  <img src="/img/feature_teams/xfeature_team.jp.png" alt="feature_team.jp.png">
  <figcaption>図1. フィーチャーチーム</figcaption>
</figure>

<!---
The characteristics of a feature team are listed below:
--->
フィーチャーチームの特徴は以下のとおり:

<!---
* long-lived—the team stays together so that they can ‘jell’ for higher performance; they take on new features over time
* cross-functional and cross-component
* ideally, co-located
* work on a complete customer-centric feature, across all components and disciplines (analysis, programming, testing, …)
* composed of generalizing specialists
* in Scrum, typically 7 ± 2 people
--->
* 長寿命 - チームは、より高いパフォーマンスを発揮するために、一緒に居続ける。そして時間を掛けて新しいフィーチャーを引き受ける
* 機能横断的でコンポーネント横断的
* 理想的には同じ場所にいる
* 全てのコンポーネントや領域(分析、プログラミング、テスト)を超え、完全なる顧客中心のフィーチャーで作業する
* 一般的に専門家で構成される
* スクラムでは、通常は7±2人

<!---
Applying modern engineering practices—especially continuous integration—is essential when adopting feature teams. Continuous integration facilitates shared code ownership, which is a necessity when multiple teams work at the same time on the same components.
--->
モダンなエンジニアプラクティスを適用する - フィーチャーチームを採用する場合は、特に継続的インテグレーションが不可欠です。
継続的インテグレーションは、複数のチームが同じコンポーネントを同時に作業する場合に必須であるコードの共同所有を容易にします。

<!---
A common misunderstanding: every member of a feature team needs to know the whole system. Not so, because
--->
共通の誤解:フィーチャーチームのすべてのメンバーは、システム全体を知る必要があります。
あながち間違いではないが、理由は

<!---
* The team as a whole—not each individual member—requires the skills to implement the entire customer-centric feature. These include component knowledge and functional skills such as test, interaction design, or programming. But within the team, people still specialize… preferably in multiple areas.
* Features are not randomly distributed over the feature teams. The current knowledge and skills of a team are factored into the decision of which team works on which features.
--->
* チーム(各チームメンバーではない)として、顧客中心のフィーチャー全体を実装するためのスキルを必要とします。
これらスキルは、コンポーネントの知識、テストなどの機能スキル、インタラクションデザイン、プログラミングを含みます。
しかしながら、チーム内でまだ特化してしまう...できれば複数の領域にしてください。
* フィーチャーはフィーチャーチームを超えて、無作為に分配されるわけではない。どのフィーチャーをどのチームが作業するかは、現在の知識とチームのスキルを織り込んで決定する。

<!---
Within a feature team organization, when specialization becomes a constraint…learning happens.
--->
フィーチャーチームの組織では、分業が制約になると...学習が発生する。

<!---
A feature team organization exploits speed benefits from specialization, as long as requirements map to the skills of the teams.
But when requirements do not map to the skills of the teams, learning is ‘forced,’ breaking the overspecialization constraint.
Feature teams balance specialization and flexibility.
--->
フィーチャーチームの組織では、要求とチームのスキルが一致するのであれば、分業によるスピードの利点を有効に活用する。
しかし、要求とチームのスキルが一致しない場合は、学習が'強制的に'過度の専門化の制約を壊します。
フィーチャーチームは、専門性と柔軟性のバランスをとる。

<!---
## component vs. feature teams

The table below and Figure 2 show the differences between feature teams and more traditional component teams.
--->
## コンポーネントチーム vs フィーチャーチーム

以下の表および図2は、フィーチャーチームと伝統的なコンポーネントチームとの違いを示しています。

<!---
|component team	|feature team|
|optimized for delivering the maximum number of lines of code|	optimized for delivering the maximum customer value|
|focus on increased individual productivity by implementing ‘easy’ lower-value features|	focus on high-value features and system productivity (value throughput)|
|responsible for only part of a customer-centric feature|	responsible for complete customer-centric feature|
|traditional way of organizing teams — follows Conway’s law|	‘modern’ way of organizing teams — avoids Conway’s law|
|leads to ‘invented’ work and a forever-growing organization|	leads to customer focus, visibility, and smaller organizations|
|dependencies between teams leads to additional planning|	minimizes dependencies between teams to increase flexibility|
|focus on single specialization|	focus on multiple specializations|
|individual/team code ownership	|shared product code ownership|
|clear individual responsibilities|	shared team responsibilities|
|results in ‘waterfall’ development|	supports iterative development|
|exploits existing expertise; lower level of learning new skills|	exploits flexibility; continuous and broad learning|
|works with sloppy engineering practices—effects are localized|	requires skilled engineering practices—effects are broadly visible|
|contrary to belief, often leads to low-quality code in component|	provides a motivation to make code easy to maintain and test|
|seemingly easy to implement|	seemingly difficult to implement|
--->

| コンポーネントチーム | フィーチャーチーム |
|コードの行数を最大化するために最適化|顧客価値を最大化するために最適化|
|'簡単に'低い価値のフィーチャーを実装することにより増えた、個人の生産性にフォーカスする|価値の高いフィーチャーや、システムの生産性(価値のスループット)にフォーカスする|
|顧客中心のフィーチャーの一部分だけに責任を持つ|顧客中心のフィーチャー全てに責任を持つ|
|コンウェイの法則に従う伝統的なチーム編成方法|チーム編成の'近代的な'方法はコンウェイの法則を回避する|
|'生み出す'作業と永遠に成長する組織につながる|顧客重視、可視性、中小規模の組織につながる|
|チームの依存関係は計画の追加につながる|柔軟性を高めるためにチーム間の依存関係を最小化する|
|単一の専門分野にフォーカス|複数の専門分野にフォーカス|
|個人/チームでのコードの所有|プロダクトコードの共同所有|
|個人の責任|チームの責任|
|ウォーターフォール開発の結果|反復開発をサポート|
|既存の専門知識を活用;新しいスキルの低レベルの学習|柔軟性を活用;継続した幅広い学習|
|ずさんなエンジニアリングの実践と連携 - 効果が局所的|熟練したエンジニアリングの実践が求められる - 効果は広く明らか|
|信念に反して、コンポーネントの低品質なコードにつながる|メンテナンスとテストを容易にするためのコードを書く動機をもたらす|
|実装が一見簡単|実装が一見難しい|

<figure>
  <img src="/img/feature_teams/xcomponent_vs_feature_teams.jp.png" alt="component_vs_feature_teams.jp.png">
  <figcaption>図2. コンポーネントチーム vs フィーチャーチーム</figcaption>
</figure>

<!---
The table below summarizes the differences between feature teams and conventional project or feature groups.
--->
以下の表は、フィーチャーチームと従来のプロジェクトやフィーチャーグループとの違いをまとめたものです。

<!---
|feature team|	feature group or feature project|
|stable team that stays together for years and works on many features|	temporary group of people created for one feature or project|
|shared team responsibility for all the work|	individual responsibility for ‘their’ part based on specialization|
|self-managing team	|controlled by a project manager|
|results in a simple single-line organization (no matrix!)|	results in a matrix organization with resource pools|
|team members are dedicated—100% allocated—to the team|	members are part-time on many projects because of specialization|
--->

|フィーチャーチーム|フィーチャーグループ or フィーチャープロジェクト|
|年間を通じて一緒にたくさんのフィーチャーで作業を維持する安定したチーム|1つのフィーチャーまたはプロジェクトのために集められた一時的なグループ|
|全ての作業において責任を共有するチーム|専門に基づく個人の責任|
|自己組織化されたチーム|プロジェクトマネージャーに管理される|
|シンプルな単一ライン組織における結果(マトリックスではない)|リソースプールを持つマトリックス組織の結果|
|チームメンバーは専任(100%割り当てられる)チーム|メンバーは専門であるがゆえに多くのプロジェクトで作業するパートタイム|

<!---
Most drawbacks of component teams are explored in the “Feature Teams” chapter of Scaling Lean & Agile Development, Figure 3 summarizes some of these.
--->

コンポーネントチームの欠点の多くは、Scaling Lean & Agile Developmentの"フィーチャーチーム"の章で検討されている。図3は、これらのいくつかをまとめたものです。

<!---
What is sometimes not seen is that a component team structure reinforces sequential development (a ‘waterfall’ or V-model), with many queues with varying-sized work packages, high levels of WIP, many handoffs, and increased multitasking and partial allocation.
--->
見えないこともあるが、コンポーネントチームの構造は、シーケンシャル開発(ウォーターフォールやV字モデル)を強化する。それは、多くの待ち行列や可変サイズの作業の塊、たくさんのWIP、多くの情報伝達、増大するマルチタスク、部分的な割り当てをもたらす。

<!---
## Choose Component Teams or Feature Teams?
--->
## コンポーネントチームとフィーチャーチームとどちらを選ぶ？

<!---
A pure feature team organization is ideal from the value-delivery and organizational-flexibility perspective. Value and flexibility, however, are not the only criterion for organizational design, and many organizations therefore end up with a hybrid—especially during a transition from component to feature teams. Caution: hybrid models have the drawbacks from both worlds and can be…painful.
--->

純粋なフィーチャーチームの組織は、価値を届けるのと組織の柔軟性の観点から理想的です。
しかしながら、価値と柔軟性は、組織設計のための唯一の基準ではなく、多くの組織は、特にコンポーネントチームからフィーチャーチームへの移行中にハイブリッドで終わる。
注意:ハイブリッドモデルでは、両者の欠点と痛みを伴う...

<!---
A frequently expressed reason in favor of a hybrid organization is the need to build infrastructure, construct reusable components, or clean up code—work traditionally done within component teams. But these activities can also be done in a pure feature team organization—without establishing permanent component teams. How? By adding infrastructure, reusable components, or cleanup work to the Product Backlog and giving it to an existing feature team—as if it were a customer-centric feature. The feature team temporarily—for as long as the Product Owner wishes—does such work and then returns to building customer-centric features.
--->
たびたびハイブリッド組織を支持する理由は、インフラの構築、再利用可能なコンポーネントの構築、コードのクリーンアップなど、伝統的なコンポーネントチームで行われた作業をする必要があることです。
しかし、これらの活動はまた、恒久的なコンポーネントチームを確立し、組織することなく、純粋なフィーチャーチームで行うことができます。
どうやって？
プロダクトバックログに、インフラや、再利用可能なコンポーネント、クリーンアップなどの作業を追加し、
既存のフィーチャーチームに顧客中心のフィーチャーと同様にそれを与える。
フィーチャーチームは、一時的にこのような作業(プロダクトオーナーの要望であるならば)を行い、その後、顧客中心のフィーチャーの構築に戻します。

<!---
## Transitioning to Feature Teams
--->
## フィーチャーチームへの移行

<!---
Different organizations require different transition strategies when changing from component to feature teams. We have experience with many strategies that worked…and failed in a different context. A safe—but slow—transitioning strategy is to establish one feature team within the existing component team organization. After this team performs well, a second feature team is formed. This continues gradually at the speed the organization is comfortable with. This is shown in Figure 4.
--->
コンポーネントチームからフィーチャーチームへの移行する場合は、異なる組織は異なる移行戦略が必要になる。
私たちは、多くの戦略と経験を持っている...そして異なるコンテキストによって失敗もしている。
安全な(しかしゆっくりと)移行戦略は、既存のコンポーネントチームの中から一つのフィーチャーチームを作ることです。
このチームが上手くできたのちに、第2のフィーチャーチームが作られます。
これを、組織がしっくりくるスピードで徐々に続けていきます。
図4に示しています。

<!---
## Recommended Reading
--->

## 推薦図書

<!---
* Feature Team Primer
This article originally appeared as the [Feature Team Primer](http://www.featureteamprimer.com/)
* Feature Teams chapter of [Scaling Agile & Lean Development](http://www.amazon.com/Scaling-Lean-Agile-Development-Organizational/dp/0321480961)
This 60-page analysis of feature and component teams is also [available online](http://www.infoq.com/resource/articles/scaling-lean-agile-feature-teams/en/resources/feature%20teams_%20infoq_%20final.pdf)
* [Dynamics of Software Development by Jim McCarthy](http://www.amazon.com/Dynamics-Software-Development-Jim-McCarthy/dp/1556158238)
Originally published in 1995 but republished in 2008. Jim’s book is a true classic on software development. Already in 1995 it emphasized feature teams. The rest of the book is stuffed with insightful tips related to software development.
* [“XP and Large Distributed Software Projects” by Karlsson and Andersson.](http://dl.acm.org/citation.cfm?id=377525)
This early large-scale agile development article is published in Extreme Programming Perspectives. It is a insightful and much under-appreciated article describing the strong relationship between feature teams and continuous integration.
* [“How Do Committees Invent?” by Mel Conway.](http://www.melconway.com/research/committees.html)
This 40-year article is as insightful today as it was 40 years ago. It is available via the authors website at www.melconway.com.
--->
* フィーチャーチーム入門
この記事はもともと[フィーチャーチーム入門](http://www.featureteamprimer.com/)として掲載されました。
* [Scaling Agile & Lean Development](http://www.amazon.com/Scaling-Lean-Agile-Development-Organizational/dp/0321480961)のフィーチャーチームの章
60ページのフィーチャーチームとコンポーネントチームの分析[オンラインも利用可能です](http://www.infoq.com/resource/articles/scaling-lean-agile-feature-teams/en/resources/feature%20teams_%20infoq_%20final.pdf)
* [Dynamics of Software Development by Jim McCarthy](http://www.amazon.com/Dynamics-Software-Development-Jim-McCarthy/dp/1556158238) 邦訳[ソフトウェア開発のダイナミズム](http://www.amazon.co.jp/dp/4756110525/sr=8-1/qid=1201160706/ref=olp_product_details?_encoding=UTF8&me=&qid=1201160706&sr=8-1) オリジナルは1995年に発表されたが、2008年に再販された。 Jimの本は、ソフトウェア開発における真の古典です。1995年にすでにフィーチャーチームを取り上げていました。その他、ソフトウェア開発に関連する洞察力のヒントが詰まっています。
* [“XP and Large Distributed Software Projects” by Karlsson and Andersson.](http://dl.acm.org/citation.cfm?id=377525) この初期の大規模アジャイル開発の記事は、エクストリーム・プログラミングの視点で公開されています。過小評価されている記事ではあるが、フィーチャーチームと継続的インテグレーションの間に強い相関関係があることを記述した洞察力のある記事です。
* [“How Do Committees Invent?”(委員会をどのように作り出すのか) by Mel Conway.](http://www.melconway.com/research/committees.html) 今日にも通用する40年前の洞察力のある記事です。この記事は、著者の[webサイト](www.melconway.com)を通じて入手できます。
