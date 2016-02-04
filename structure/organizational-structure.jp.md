---
layout: mechanics
title:  組織構造
order: 10
---

<!---
How does this all fit together in an organizational structure? Of course, each organization is different, yet LeSS organizations tend to follow a surprisingly simple structure. The first difference between LeSS organizations and most traditional ones is that the structure is stable as (1) work is organized around teams, and (2) mismatch of skills triggers learning and coordination within existing teams.
--->
どのように全ての組織構造は組み合わさるのでしょうか？
もちろん、それぞれの組織は異なっている。なお、LeSSの組織は、驚くほどシンプルな構造に従う傾向があります。
LeSSの組織と最も伝統的な組織との第一の差は、(1)作業はチームを中心に構成されている構造が安定している(2)スキルのミスマッチが学習と協調のトリガーとなることです。

<!---
## LeSS Organizational Structure
--->
## LeSSの組織構造

<!---
A typical LeSS organizational chart looks like this:
--->
典型的なLeSSの組織図は以下のようになります:

<figure>
  <img src="/img/organizational-structure/xorganization-LeSS.png.pagespeed.ic.R51VOdvboZ.png" alt="organization-LeSS.png">
</figure>

<!---
Notice what isn’t here:
--->
ここでは無いことに注意をしてください:

<!---
* No project/program organization or project/program management office (PMO).
These traditional control organizations cease to exist in a LeSS organization as their responsibilities are distributed between the feature teams and the Product Owner. Insisting on keeping such organizations will cause confusion and conflicts of responsibilities.
--->
* プロジェクト/プログラム組織または、プロジェクト/プログラムマネジメントオフィス(PMO)ではない
これらの従来の制御組織は、その責任はフィーチャーチームとプロダクトオーナーに分散しているようにLeSSの組織には存在しなくなります。
このような組織維持しようとすると、混乱と責任の競合状態になるでしょう。

<!---
* No support groups such as configuration management, continuous integration support, or “quality and process”.
LeSS organizations prefer to expand the existing teams responsibility to include this work over creating more complex organization with specialized groups. Specialized support groups tend to ‘own’ their area which leads to them becoming a bottleneck.
--->
* 構成管理、継続的インテグレーションのサポートや、品質とプロセスのサポートグループは存在しない
LeSSの組織は、専門家グループとともに、さらに複合組織を作り直すことを含め、既存のチームの責任の拡大を好みます。
専門家のグループは、彼ら自身がボトルネックなってくると、自分のエリアを守ろうとする傾向がある。

<!---
Let’s examine a LeSS organization…
--->
それでは、LeSSの組織を調べてみましょう...

<!---
**Head of the Product Group**—Most LeSS organizations still have managers including a “head of product group.” They support the teams by Go See and help them remove obstacles and improve. LeSS organizations don’t have matrix structures and there are no “dotted-line” managers.
“Head of Product Group” is called differently in different organization, here we mean the hierarchical manager of all the teams.
--->
**プロダクトグループ長**—ほとんどのLeSSの組織では、"プロダクトグループ長"などのマネージャーが存在する。
彼らは現地現物によってチームをサポートし、それらが障害の除去し、チームが成長するのを助けます。
”プロダクトグループ長”は、ここでは、全てのチームの階層的なマネージャーを指しているが、異なる組織では別の名前で呼ばれています。

<!---
**Feature teams**—This is where the development work is done. Each team is cross-functional, self-managing feature team with a ScrumMaster. They are permanent units that stay together for the duration of a product (and sometimes longer). Avoid lots of hierarchical layers as much as possible.
--->
**フィーチャーチーム**-開発作業が行われる。
各フィーチャーチームは、スクラムマスターと機能横断的、自己組織化なチームです。
彼らはプロダクトの開発期間中(そして時には長い間)、一緒にいる恒久的なユニットです。
可能な限り、多くの階層は作らないでください。

<!---
**Product Owner (Team)**—This is also commonly called “Product Management.” It can be one person but in a larger LeSS organization the Product Owner might be supported by other product managers.
An important point in this organizational structure is that the Teams and the Product Owner are peers. This important to keep the power balanced between the roles. The Teams and Product Owner should have a cooperative peer relationship.
A common alternative structure is when the Product Owner belongs to a different organization. This is OK though it does often require additional effort to ensure the Product Owner has a close relationship with the Teams.
--->
**プロダクトオーナー(チーム)**-一般的には”プロダクトマネージメント”と呼ばれています。
一人で出来ますが、大きなLeSSの組織のプロダクトオーナーは、他のプロダクトマネージャーにサポートしてもらうかもしれません。この組織構造における重要な点は、チームとプロダクトオーナーの関係が対等であるということです。このロール間のパワーバランスを維持することが重要です。
チームとプロダクトオーナーは、協力的な対等の関係性とすべきです。
プロダクトオーナーが別の組織に属している場合は、一般的な代替構造があります。
それは多くの場合、プロダクトオーナーとチームと密接な関係を確保するためには、追加の取り組みが必要となるが、これは問題ありません。

<!---
**Undone department**—This department, ideally, does not exists.
But unfortunately sometimes the teams are not yet able to create a true shippable increment every Sprint. This is reflected by their “Definition of Done” not being equal to “Potentially Shippable.” Undone departments such as test, QA, architecture, or business analysis groups should never exist in the smaller LeSS framework groups as they should be integrated into the teams from the start. On the other hand, we unfortunately frequently still see an operations or production undone department in LeSS adoptions, as they often cross organizational boundaries.
--->
**未完了に対応する部門**-この部門は、理想的には存在しません。
しかし残念ながら、往々にしてチームは、スプリント毎に真の出荷可能なインクリメントを作ることが出来ません。これは”完成の定義”が”出荷可能”では無いことが反映されています。
小さいLeSSフレームワークのグループには、テスト、QA、アーキテクチャ、ビジネスアナリストのような未完了に対応する部門は存在してはならない。彼らは最初からチームに統合されるべきです。
一方で、LeSSを採用している組織をまたがるような組織では、残念ながらしばしば未完了に対応する部門を見かける。
