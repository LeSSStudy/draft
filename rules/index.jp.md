---
layout: mechanics
title: LeSSルール(April 2018)
order: 45
---

<!---
(what changed since previous version)
The LeSS Rules are the definition of the LeSS Framework. They are things we consider a must. Why? This is explained in the Why LeSS? section.
--->
([前回からの変更点](rules-changes.jp.html))
LeSSのルールはLeSSフレームワークを定義するもので、必須と定めているものです。
[なぜLeSSなのか?](../framework/why-less.jp.html)を参照してください。

<!---
## LeSS Framework Rules

The LeSS framework applies to products with 2-“8” teams.
--->

## LeSSフレームワークのルール

LeSSフレームワークは2〜”8”チームで開発するプロダクトに適用します。

<!---
### LeSS Structure
- Structure the organization using real teams as the basic organizational building block.
- Each team is (1) self-managing, (2) cross-functional, (3) co-located, and (4) long-lived.
- The majority of the teams are customer-focused feature teams.
- Scrum Masters are responsible for a well-working LeSS adoption. Their focus is towards the Teams, Product Owner, organization, and development practices. A Scrum Master does not focus on just one team but on the overall organizational system.
- A Scrum Master is a dedicated full-time role.
- One Scrum Master can serve 1-3 teams.
- In LeSS, managers are optional, but if managers do exist their role is likely to change. Their focus shifts from managing the day-to-day product work to improving the value-delivering capability of the product development system.
- Managers’ role is to improve the product development system by practicing Go See, encouraging Stop & Fix, and “experiments over conformance”.
- For the product group, establish the complete LeSS structure “at the start”; this is vital for a LeSS adoption.
- For the larger organization beyond the product group, adopt LeSS evolutionarily using Go and See to create an organization where experimentation and improvement is the norm.
--->

### LeSSの構造

- 実際のチームを組織の基本構成要素として組織を構成します。
- それぞれのチームは、(1)自己管理、(2)クロスファンクショナル、(3)同一ロケーション、(4)長期間存続です。
- チームの大半は顧客中心のフィーチャーチームです。
- スクラムマスターはLeSSの導入が問題なく行われることに責任を持ちます。注力する対象は、チーム、プロダクトオーナー、組織、技術的手法であり、１チームだけの改善に留まることなく、組織全体の改善を行う必要があります。
- スクラムマスターは専任でフルタイムのロール役割です。
- １人のスクラムマスターが１〜３チームを担当することができます。
- LeSSではマネージャーは必須ではありません。もしマネージャーがいた場合は、が、いる場合でも多くの場合役割が変わります。マネージャーがフォーカスすべきことは、日々の作業の管理からプロダクトを開発するシステム全体の価値提供能力の向上に移ります。
- マネージャーの役割はプロダクト開発の仕組みの改善を促進することです。「現地現物」の実践、「止めて直す」の推奨、「”適合するよりも実験をする」”ことを通じて改善を促進します。
- プロダクトグループは、「”最初から」”完全なLeSSの構造を適用します。これはLeSSを導入する際の肝となることです。
- プロダクトグループを越える、より大きな組織には、「現地現物」の考え方を使い、実験や改善があたりまえとなる環境を作っていくことで段階的にLeSS導入を進めます。

<!---
### LeSS Product
- There is one Product Owner and one Product Backlog for the complete shippable product.
- The Product Owner shouldn’t work alone on Product Backlog refinement; he is supported by the multiple Teams working directly with customers/users and other stakeholders.
- All prioritization goes through the Product Owner, but clarification is as much as possible directly between the Teams and customer/users and other stakeholders.
- The definition of product should be as broad and end-user/customer centric as is practical. Over time, the definition of product might expand. Broader definitions are preferred.
- One Definition of Done for the whole product common for all teams.
- Each team can have their own stronger Definition of Done by expanding the common one.
- The perfection goal is to improve the Definition of Done so that it results in a shippable product each Sprint (or even more frequently).
--->

### LeSSのプロダクト

- 1人のプロダクトオーナーと1つのプロダクトバックログがあり、出荷可能なプロダクト全体を運用します。
- プロダクトオーナーだけでプロダクトバックログリファインメントをするべきではありません。複数のチームが顧客やユーザー、ステークホルダーと直接コミュニケーションをとり、プロダクトオーナーをサポートします。
- 全ての優先順位付けはプロダクトオーナーが行います。が、要求や仕様を明確にするのは出来る限りチームと、顧客やユーザーそしてステークホルダーとの間で直接行います。
- プロダクトの定義は現実的な範囲で、エンドユーザーまたは顧客中心でなければなりません。プロダクトの定義は広い方が好ましく、時間の経過とともに拡張する可能性があります。
- プロダクト全体で全チーム共通の1つのDoneの定義を持ちます。
- 各チームは共通のDoneの定義を拡張してより厳しい独自のものを定めても構いません。
- 究極のゴールはDoneの定義を拡張し、毎スプリント（あるいはより高い頻度で）出荷可能なプロダクトを作れるようになることです。

<!---
### LeSS Sprint
- There is one product-level Sprint, not a different Sprint for each Team. Each Team starts and ends the Sprint at the same time. Each Sprint results in an integrated whole product.
- Sprint Planning consists of two parts: Sprint Planning One is common for all teams while Sprint Planning Two is usually done separately for each team. Do multi-team Sprint Planning Two in a shared space for closely related items.
- Sprint Planning One is attended by the Product Owner and Teams or Team representatives. They together tentatively select the items that each team will work on that Sprint. The Teams identify opportunities to work together and final questions are clarified.
- Each Team has their own Sprint Backlog.
- Sprint Planning Two is for Teams to decide how they will do the selected items. This usually involves design and the creation of their Sprint Backlogs.
- Each Team has their own Daily Scrum.
- Cross-team coordination is decided by the teams. Prefer decentralized and informal coordination over centralized coordination. Emphasize Just Talk and informal networks via communicate in code, cross-team meetings, component mentors, travelers, scouts, and open spaces.
- Product Backlog Refinement (PBR) is preferably done with multiple teams to increase shared learning and to exploit coordination opportunities.
- There is one product Sprint Review; it is common for all teams. Ensure that suitable stakeholders join to contribute the information needed for effective inspection and adaptation.
- Each Team has their own Sprint Retrospective.
- An Overall Retrospective is held after the Team Retrospectives to discuss cross-team and system-wide issues, and create improvement experiments. This is attended by Product Owner, Scrum Masters, Team representatives, and managers (if any).
--->

### LeSSのスプリント

- １つのプロダクトに関わる全てのチームは同じスプリントで作業します。スプリントの開始も終了も全チーム共通です。スプリントの終わりにはプロダクト全体が１つに統合されている状態にします。
- スプリントプランニングは２つのパートで構成されています。スプリントプランニング１は全てのチームが合同で実施します。それに対してスプリントプランニング２は通常、各チームごとに個別で行われます。ただし、関連性が強いアイテムがある場合は共有スペースで、マルチチーム・スプリントプランニング２を行います。
- スプリントプランニング１にはプロダクトオーナーとチーム全員またはチームの代表者が参加します。参加者は一緒に、各チームがこのスプリントで作業するアイテムを暫定的に選択します。チームは協働する部分を特定し、質問を明確にします。
- 各チームにはチームごとのスプリントバックログがあります。
- スプリントプランニング２は各チームがどのようにアイテムを実現させるかを考える場であり、設計やスプリントバックログの作成を行います。
- デイリースクラムはチームごとに行います。
- チームどうしの調整はチームに委ねられています。中央集権的な調整ではなく、個別の判断で自由かつ非公式に調整する方が好ましいです。重要なのは、「ただ話す」ことや、非公式のコミュニケーションである「コードでのコミュニケーション」、チームをまたいだミーティング、「コンポーネントメンター」、「トラベラー」、「偵察」、そして「オープンスペース」を活用することです。
- プロダクトバックログリファインメント（PBR）は、シェアード・ラーニング(訳注:学習しらものをシェアする)を増やし、調整の機会として活用できるため、複数チームで行うのが望ましいです。
- スプリントレビューは全てのチームが共同で行います。検査と適応を行うのに適切な情報を得られるよう、必要なステークホルダーが参加するようにします。
- スプリントレトロスペクティブは各チームで行います。
- オーバーオール・レトロスペクティブは各チームのレトロスペクティブの後に行われます。ここでは複数チームやシステム全体にまたがる課題を扱い、改善に向けての実験を議論します。この場にはプロダクトオーナー、全スクラムマスター、チーム代表者と、（いるなら）マネージャーが参加します。

<!---
## LeSS Huge Framework Rules
LeSS Huge applies to products with “8+” teams. Avoid applying LeSS Huge for smaller product groups as it will result in more overhead and local optimizations.

All LeSS rules apply to LeSS Huge, unless otherwise stated. Each Requirement Area acts like the basic LeSS framework.
--->

## LeSS Hugeフレームワークのルール

LeSS Hugeはプロダクトを「”８チーム以上」”で作る場合に適用します。これよりも小さな規模でLeSS Hugeを適用することは推奨しません。不必要なオーバーヘッドや部分最適の原因となります。

特に明記しない限り、すべてのLeSSのルールはLeSS Hugeにも適用されます。各要求エリアは、基本的なLeSSのフレームワークのようにふるまいます。

<!---
### LeSS Huge Structure
- Customer requirements that are strongly related from a customer perspective are grouped in Requirement Areas.
- Each Team specializes in one Requirement Area. Teams stay in one area for a long time. When there is more value in other areas, teams might change Requirement Area
- Each Requirement Area has one Area Product Owner.
- Each Requirement Area has between “4-8” teams. Avoid violating this range.
- LeSS Huge adoptions, including the structural changes, are done with an evolutionary incremental approach.
- Remember each day: LeSS Huge adoptions take months or years, infinite patience, and sense of humor.
--->

## LeSS Hugeの構造

- 顧客視点で関連の強い顧客の要求は、要求エリアにまとめられます。
- 各チームは１つの要求エリアを専門的に対応します。チームはエリアに長期間固定するものです。ただし、他のエリアの価値がより高くなった場合、そちらに移動することがあります。
- 各要求エリアにはエリア・プロダクトオーナーが1人ずついます。
- 各エリアは「４〜８」チームで構成されます。このチーム数の範囲を守るようにします。
- LeSS Hugeの導入は、構造上の変更も含め、進化させながらインクリメンタルなアプローチで進めます。
- 毎日思い出して下さい。LeSS Hugeの導入は数ヶ月〜数年を要します。無限の忍耐とユーモアのセンスを持って進めてください。

<!---
### LeSS Huge Product
- One (overall) Product Owner is responsible for product-wide prioritization and deciding which teams work in which Area. He works closely with Area Product Owners.
- Area Product Owners act as Product Owners towards their teams.
- There is one Product Backlog; every item in it belongs to exactly one Requirement Area.
- There is one Area Product Backlog per Requirement Area. This backlog is conceptually a more granular view onto the one Product Backlog.
--->

### LeSS Hugeのプロダクト

- 全体の（オーバーオール）プロダクトオーナーの役割はプロダクト全体の優先順位決めと、どのチームがどのエリアを対応するかを決めることです。エリア・プロダクトオーナーとは密にコミュニケーションを取る必要があります。
- エリア・プロダクトオーナーは当該エリアのチームに対してプロダクトオーナーとしてふるまいます。
- プロダクトバックログは１つです。そして全てのアイテムはどこか必ず１つの要求エリアに属します。
- 要求エリアごとに１つのエリア・プロダクトバックログが存在します。このバックログは概念的には、プロダクトバックログをより詳細な視点で記述しているものです。

<!---
### LeSS Huge Sprint
- There is one product-level Sprint, not a different Sprint for each Requirement Area. It ends in one integrated whole product.
- The Product Owner and Area Product Owners synchronize frequently. Before Sprint Planning they ensure the Teams work on the most valuable items. After the Sprint Review, they further enable product-level adaptations.
--->

### LeSS Hugeのスプリント

- プロダクト単位でスプリント期間は共通です。各要求エリアで別々のスプリント期間にとすることはありません。スプリントの終わりには統合された１つのプロダクトになっている必要があります。
- プロダクトオーナーとエリア・プロダクトオーナーは頻繁に会話し、スプリントプランニング時にチームが最も価値の高いアイテムに着手できるように準備する必要があります。また、スプリントレビュー後にはプロダクト規模の適応がより一層可能となります。