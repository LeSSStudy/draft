---
layout: mechanics
title: プロダクトバックログリファインメント
order: 110
---

<!---
Ongoing Product Backlog Refinement (PBR) is needed within each Sprint to refine items to be ready for future Sprints. Key activities of PBR are (1) splitting big items, (2) detailing items until ready, and (3) estimating. In the spirit of [empirical process control](../principles/empirical_process_control.html), Scrum does not say how to do PBR, though suggests that the Team spend no more than 10% of their Sprint capacity on it. It usually happens “mid-Sprint.”
--->
継続的なプロダクトバックログリファインメント(PBR)は、将来のスプリントのプロダクトバックログアイテムを洗練するために、各スプリント内で必要とされている。
PBRの主なアクティビティは、(1)大きなプロダクトバックログアイテムを分割する。(2)準備ができるまでプロダクトバックログアイテムを詳細化する。(3)見積もりを行う。
[経験的プロセス制御](../principles/empirical_process_control.jp.html)の精神で、スクラムはPBRをどのように行うかは伝えてはいないにもかかわらず、チームは、スプリントの10%以下を費やすことを示唆している。それは通常"スプリントの中間"で発生します。 <!-- TODO mid-Sprint ってなんだ？ -->

<!---
Note! Refinement of items is not done separately by the [Product Owner](product-owner.html) or a business analysis group—doing that would increase the [lean wastes](../principles/lean_thinking.html) of hand-off and information scatter. Rather, the Team does this work—and not a subset of the Team, but the whole Team, as Scrum rules prohibit sub-groups dedicated to particular domains such as analysis or testing.
--->
注意！
プロダクトバックログアイテムの洗練は、[プロダクトオーナー](product-owner.jp.html)またはビジネスアナリストのグループとは別に行われていませんか - それを行なっていると、[手持ちのムダ](../principles/lean_thinking.jp.html)や情報の散乱を増加させるでしょう。
正しくは、スクラムのルールでは、分析やテストのような特定のドメインに専念するサブグループを禁止しています。チームのサブセットではなくチーム全体で行います。

<!---
## Product Backlog Refinement Overview
--->
## プロダクトバックログリファインメント概要

<!---
Product Backlog Refinement is often done in:

* Overall Product Backlog Refinement (shared amount all teams)
* Team-level Product Backlog Refinement
* Multi-team Product Backlog Refinement
--->
プロダクトバックログリファインメントはしばしば行われます。
* 全体的なプロダクトバックログリファインメント (全てのチームに共有する)
* チームレベルのプロダクトバックログリファインメント
* マルチチームのプロダクトバックログリファインメント

<figure>
  <img src="/img/framework/product-backlog-refinement.png" alt="product-backlog-refinement.png">
</figure>

<!---
## Overall Product Backlog Refinement
--->
## 全体的なプロダクトバックログリファインメント

<!---
The LeSS rule raises the questions: How to decide which teams are likely to implement which items? And there are the scaling issues just examined: shared understanding, coordination, common work, aligned estimates, and balancing specialization and agility.
--->
LeSSのルールは質問を引き出します:どのチームがどのプロダクトバックログアイテムを実装するのかをどのように決めますか？
そして、ちょうど調べたスケーリングの課題もあります:共通の理解、協調、共通の仕事、見積もりを合わせる、バランスをとる専門性とアジリティ

<!---
An overall PBR session addresses all of these. In brief, hold an overall PBR workshop with representatives before the individual team PBR sessions, to explore which teams might work on which items, and to increase learning and alignment. Attendees include the Product Owner, subject-matter experts, and either all members of all teams or a couple of representatives from each team. Representatives are usually preferred, to keep the meeting smaller and to not have everyone in yet another meeting, though the cost is information handoff and scatter.
--->
全体的なプロダクトバックログリファインメントではこれらすべてに対応しています。
簡単に言えば、学習と協力を高め、どのチームがどのプロダクトバックログアイテムの作業をするのが良いのかを探求するために、個々のチームのプロダクトバックログリファインメントの前に代表者で、全体的なプロダクトバックログリファインメントを開催する。
参加者は、プロダクトオーナー、主題の専門家、およびすべてのチームメンバーまたは、個々のチームの2名の代表者で行う。
代表者で実施することは、情報伝達や情報の散乱してしまうコストが発生するが、ミーティングを小さく維持すること、そしてさらにもうひとつミーティングを全員に増やさないために、推奨している。

<!---
Do the following:

* split big items
* do very lightweight item analysis for basic understanding
* estimate items
* identify strongly-related items that suggest shared work, common work, or coordination
--->
以下を行います。
* 大きなプロダクトバックログアイテムの分割
* 基本的な理解のために、非常に軽量なプロダクトバックログアイテムの分析を行う
* プロダクトバックログアイテムの見積もり
* 共同での作業、共通的な作業の提案または調整のため、強い関連があるプロダクトバックログアイテムの特定

<!---
## Team-level Product Backlog Refinement
--->
## チームレベルのプロダクトバックログリファインメント

<!---
When an item will clearly be done by one team and it won't be too strongly related to other items, then the Product Backlog Refinement is the same as in a one-team Scrum. The team does the refinement themselves, ideally together with users/customer/stakeholders and they inform the Product Owner related to changes (splitting, new estimates) in the Product Backlog.
--->
プロダクトバックログアイテムが明らかに1つのチームで完了でき、他のプロダクトバックログアイテムと強い関連性が無い場合は、プロダクトバックログリファインメントは1チームのスクラムの場合と同じです。
チームは、理想的にはユーザー・顧客・ステークホルダーと一緒にリファインメントを行い、プロダクトバックログの変更(分割、新たな見積もり)に関係のある情報をプロダクトオーナーに提供します。

<!---
## Multi-team Product Backlog Refinement
--->
## マルチチームのプロダクトバックログリファインメント

<!---
Multiteam PBR is when more than one team are (literally) in the same room at the same time doing PBR. Attendees include subject-matter experts, and either all members of the participating teams or a couple of representatives from each.
--->
マルチチームのプロダクトバックログリファインメントは、1チーム以上で同じ時間、同じ場所で行う(文字通りの)プロダクトバックログリファインメントです。
参加者は、主題の専門家および関わる全てのチームのメンバーまたはそれぞれのチームの2人の代表者です。

<!---
How is it different from overall PBR? Overall PBR includes participation from all teams, but multiteam PBR may involve as few as two teams. It is also more likely to include all members rather than representatives.
--->
全体的なプロダクトバックログリファインメントとどのように異なるのか？
全体的なプロダクトバックログリファインメントは、全チームからの参加者で行うが、マルチチームのプロダクトバックログリファインメントは、出来る限り少ないチームで行います。
また、全てのチームメンバーではなく、代表者で行うことを推奨します。

<!---
Do multiteam PBR to increase shared understanding and exploit coordination opportunities when a group of teams are working on a common family of items or strong-related items.
--->
チームのグループが共通のプロダクトバックログアイテムまたは強い関連のあるプロダクトバックログアイテムに取り組むことで、共通理解を増やし、連携の機会を生かすために、マルチチームのプロダクトバックログリファインメントを行う。

<!---
Multiteam PBR may be a complement or replacement to team PBR.
--->
マルチチームのプロダクトバックログリファインメントは、チームのプロダクトバックログリファインメントを補完するもの、または置きかわることができます。
