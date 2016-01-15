---
layout: mechanics
title: 完成の定義(Definition of Done)
order: 87
---

<!---
Scrum’s inspect-adapt cycles require transparency in order to be effective. Formally defining the meaning of ‘done’ reduces variability and the likelihood of undone work and measuring progress unambiguously (‘done’ or ‘not done’) increases transparency.
--->
スクラムの検査と適応のサイクルが有効であるために、透明性を必要とします。
正式に”完成”の意味を定義することは、未完了作業の見込みと、曖昧さの無い進捗状況(”完成”または”完成しない”)を測定することで、ばらつきを低減させ、透明性を向上させる。
<!---
A perfect Definition of Done includes everything that the organization has to do to deliver the product to customers. Achieving this should be relatively easy for a one-team product group. When the team isn’t able to achieve the perfect Definition of Done then they define ‘done’ as a subset of the perfect set. The team’s goal is to improve so that, one day, their Definition of Done is perfect and they can ship each Sprint or more.
--->
完璧な完成の定義は、組織が顧客にプロダクトを提供するために行う必要がある全ての作業が含まれています。これを達成するには、1チームのプロダクトグループのために比較的簡単にする必要があります。
チームは、完璧な完成の定義を達成することが出来ない場合は、完璧な完成の定義のサブセットとして’完成’を明確にする。チームの目標は、完成の定義を完璧なものとする。そしてスプリント毎またはそれ以上に出荷できるようにするように、完成の定義を改善することです。

<!---
The Definition of Done is an agreed list of criteria that the software will meet for each Product Backlog Item. Achieving this level of completeness requires the Team to perform a list of tasks. When all tasks are completed, the item is done. Don’t confuse the Definition of Done with acceptance criteria, which are specific conditions an individual item has to fulfill to be accepted. The Definition of Done applies uniformly to all Product Backlog items.
--->
完成の定義は、ソフトウェアのプロダクトバックログアイテムについて満たす基準を合意した一覧です。完全なこのレベルを達成するタスクリストを実行するチームを必要とする。全てのタスクが完了すると、プロダクトバックログアイテムは、完成になります。個々のプロダクトバックログアイテムが受け入れられるために満たさなければならない特定の条件である受入基準と完成の定義を混同しないでください。完成の定義は、全てのプロダクトバックログアイテムに均一に適用されます。
<!---
## Creating the Definition of Done
--->
## 完成の定義を作成する
<!---
The initial Definition of Done must be agreed before the first Sprint. This usually happens in the [Initial Product Backlog Refinement workshop](initial-product-backlog-refinement.html).
--->
完成の最初の定義は、最初のスプリントの前に合意する必要があります。
これは通常、[初期プロダクトバックログリファインメントのワークショップ](initial-product-backlog-refinement.html)で行われます。
<!---
The following steps are taken in order to create the Definition of Done:
* Define the activities needed to ship to end customers.
* Decide which activities can be done each Sprint.
--->
完成の定義を作成するためには次の手順を行います。
* 顧客に出荷するために必要なアクティビティを定義します。
* 各スプリントで完成出来るアクティビティを決定します。
<!---
Let’s explore these steps in more detail.
--->
それでは、より詳細にこれらのステップを探索してみましょう。
<!---
### Define the activities needed to ship to end customers
--->
顧客に出荷するのに必要なアクティビティを定義します。
<!---
They key question is, “What activities are currently required to ship our product?”
--->
キーとなる質問は、「実際、私達のプロダクトを出荷するのに必要なアクティビティは何ですか？」です。
<!---
* Shipping means “delivering to end customers” and not “send out of the development department.”
* Challenge the need for intermediate artifacts. Do we really need that specification document?
--->
* 出荷するとは、”顧客にデリバリーする”を意味し、”開発部門の手を離れる”ということではありません。
* 中間成果物の必要性に挑む。本当にその仕様書は必要ですか？
<!---
The teams write post-it notes with required activities. These include activities such as coding and testing but may also include setting up customer support, creating hardware, or even marketing activities. We refer to this list as the required activities for having a Potentially Shippable Product.
--->
チームは必要なアクティビティをポスト・イットに書きます。これらは、コーディングやテストなどのアクティビティが含まれるだけではなく、顧客サポート、ハードウェアの構築、マーケティングなどを含んでも良いです。
<!---
With this step, you have created a [perfection goal](../principles/continuous-improvement-towards-perfection.html) for the organization—do all these activities for each item every Sprint. Product groups now often realize this will take a lot of improvements.
--->
この手順を行うと、全てのスプリントでのプロダクトバックログアイテムごとのアクティビティを行うことで、組織にとって完璧な目標を作成することが出来ます。プロダクトグループでは、多くの場合は、沢山の改善を行わなければならない。
<!---
### Decide which activities can be done each Sprint
--->
### スプリント毎に完成出来るアクティビティを決定します。
<!---
The key question is, “Considering our current context and capability, what activities can be completed each Sprint?” This subset is the initial Definition of Done. A Definition of Done is weak when it is a small subset and strong when it is almost equals Potentially Shippable.
--->
キーとなる質問は、「現在のコンテキストと能力を考え、アクティビティを各スプリントで終わらせることが出来るか？」です。このサブセットは、初期の完成の定義です。ほとんど出荷可能と等しい場合は、強くそして、小さいサブセットの場合は弱い完成の定義です。
<!---
The teams discuss their context and select the subset of the activities that all teams think they realistically can do during the Sprint. This is their initial Definition of Done (see example in Figure 1). The teams that can do more will expand this product Definition of Done within their teams.
--->
チームは、コンテキストと、全てのチームがスプリントの間中、現実的に出来るアクティビティのサブセットの選択を議論する。これは、(図1の例を参照)彼らの最初の完成の定義です。より多くを行うことが出来るチームは、完成の定義を拡張していきます。

<!---
The difference between the Definition of Done and Potentially Shippable is referred to as Undone Work. The Sprint is planned according to the Definition of Done and thus the Undone Work is excluded—it is planned to be left undone
--->
完成の定義と出荷可能の差は、未完了作業と呼ばれます。スプリントは、完成の定義に従って計画される。したがって、未完了作業は除外される。それは完成しないものは残る計画となる。

<figure>
  <img src="/img/framework/dod.jpg" alt="dod.jpg">
  <figcaption>図1. 出荷可能と完成の定義</figcaption>
</figure>

<!---
## Definition of Done terms
--->
## 完成の定義の条件
<!---
The terms Potentially Shippable and Definition of Done are often not used consistently, but in LeSS they have very precise meaning. To clarify the terms:
--->
出荷可能と完成の定義の条件は、相変わらず利用されていないが、LeSSではとても明確な意味を持つ。条件を明確にするには:

<!---
**Potentially Shippable**—All activities that must be performed before the product can be shipped.
--->
**出荷可能** - 実行されなければならない全てのアクティビティを完了して初めて出荷することが出来る

<!---
**Definition of Done**—An agreement between the teams and the Product Owner on which activities are performed inside the Sprint. A Definition of Done is perfect when it equals to Potentially Shippable. The teams strive to improve towards a perfect Definition of Done.
--->
**完成の定義** - スプリントで行うアクティビティをプロダクトオーナーとチームで合意する。
合意した内容が、出荷可能出来る状態であるならば完成の定義は完璧です。
チームは、完成の定義を完璧にするために改善に努めます。

<!---
**Undone Work**—The difference between the Definition of Done and Potentially Shippable. When the Definition of Done is perfect then there is no Undone Work. If this isn’t the case then the organization has to decide, (1) How do we deal with the Undone Work, and (2) How do we improve so that there is less Undone Work in the future.
--->
**未完了作業(Undone Work)** - 完成の定義と出荷可能との違い。完成の定義が完全である場合は、未完了作業はありません。そうで無い場合は、組織は決定をしなければならない。(1)どのように未完了作業を対処するのか。(2)どのように将来的に未完了作業を少なくするための改善を行うのか。

<!---
**Unfinished, not finished, or not done**—Work that was planned in a Sprint but wasn’t completed. This is often confused with Undone Work. ‘Unfinished’ is work that the team planned for but didn’t finish whereas Undone Work was never even planned for. When a team has work that was not finished then they ought to feel anxious and discuss improvement actions during their Retrospective.
--->
**未完成、着手中、完成しない** - スプリントで計画されたが、完了しなかった作業。
これは多くの場合、未完了作業と混同されています。
未完成は、チームは計画したが終わらなかった作業なのに対し、未完了作業は、計画さえしていない。
チームは、作業が途中になってしまった場合は、彼らは不安に感じるべきで、レトロスペクティブの間に改善活動を議論するべきです。
<!---
Teams should never leave work-in-progress at the end of the Sprint and “carry over” to the next one. This causes a lack of transparency and reduces scope flexibility. If they forecast too much work, they need to remove complete items which they haven’t started yet.
--->
チームは、スプリントの最後に決してワークインプログレスを残すべきではないし、次に持ち越すべきでは無い。これは透明性の欠如を引き起こし、スコープの柔軟性を低下させる。
もしチームがあまりにも多くの作業を計画した場合は、まだ開始されていない項目一式を削除する必要がある。

<!---
### Mathematics of Done
--->
### 完成の数学
<!---
Potentially Shippable = Definition of Done + Undone Work
Work in Iteration = Product Backlog Item * Definition of Done
--->
出荷可能 = 完成の定義 + 未完了作業
イテレーションの作業 = プロダクトバックログアイテム * 完成の定義
{: .box_top_bottom  .text_centered_bold }

<!---
## Undone Work -> Risk and Delay
--->
未完了作業 -> リスクと遅延
<!---
Let’s first explore the effects of Undone Work by running through a scenario.
--->
それでは、シナリオを通して、未完了作業の効果を最初に調査してみよう。

<!---
The teams completed—according to the Definition of Done—twenty Product Backlog Items in the first Sprint. They have no unfinished work but there is a lot of Undone Work due to their weak Definition of Done. After the teams completed—according to the weak Definition of Done—forty Product Backlog Items in three Sprints. The amount of Undone Work has grown enormously causing a false sense of progress.
--->
チームは - 完成の定義に従って - 最初のスプリントで20プロダクトバックログアイテムを完了した。未完成の作業は残っていないが、多くの未完了作業がある。原因は、彼らの弱い完成の定義にある。その後、チームは - 弱い完成の定義に従って - 3スプリントで40のプロダクトバックログアイテムを完成した。未完了作業の量は、進捗の誤った感覚を引き起こして、非常に成長した。

<!---
But they can’t ship. They have ‘done’ the features but their weak Definition of Done caused a vast amount of Undone Work to accumulate. This Undone Work causes delay and hidden risk.
--->
しかし、彼らは出荷出来ない。彼らはフィーチャーは完成しているが、弱い完成の定義が原因で、膨大な量の未完了作業が溜まっている。この未完了作業は、遅延と隠されたリスクの原因となった。

<!---
**Delay**—Extra effort is needed to perform the Undone Work. This causes a lack of flexibility for the Product Owner—he can’t directly respond to market needs and changes. The pain caused by this delay is aggravated by the fact that the effort to complete the Undone Work is highly variable and thus hard to predict.
--->
**遅延**- 未完了作業を行うのに余分な手間が必要になります。これはプロダクトオーナーは、直接市場のニーズや変化に対応することが出来きないため、柔軟性の欠如を引き起こします。
未完了作業を完了するための取り組みは、非常に変わりやすく、予測することが困難であるという事実によって、この遅延による痛みは、悪化します。

<!---
**Risk**—The Undone Work causes a lack of transparency. Risks are hidden in it. For example, if performance testing is left Undone then it delays the risk of a non-performing system until close to release—when it hurts most.
--->
**リスク** - 未完了作業は透明性の欠如の原因となる。リスクはその中に隠されている。
例えば、パフォーマンステストが残っている場合は、システムのリリースの近く - 最も損害を与える時 - まで、不履行のリスクを遅らせる。

<!---
A good Product Owner wants a perfect Definition of Done as that reduces product risk and avoids delay.
--->
良いプロダクトオーナーは、プロダクトのリスクを削減し、遅延を回避するため、完璧な完成の定義を望んでいる。
