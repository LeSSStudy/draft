---
layout: mechanics
title: なぜ Less なのか？
order: 10
---

<!---
Traditional sequential-lifecycle development doesn't work well. It doesn't work well for either small or large product development efforts. Since 2001, Agile development and Scrum in particular have revolutionized software development, but when asked how to apply Agile development to large groups many people say "don't" or "just use a small team" or "do Scrum at the team level.” None of those answers is particularly useful, and while it is true that it is best to avoid adding people to your development effort, it is also true that large scale product development isn’t going away so we need to discover ways to do it well.
--->

開発プロダクトの大小にかかわらず、従来型のシーケンシャルなライフサイクルに基づく開発はうまくいかないものです。2001年以降、アジャイル開発手法（特にスクラム）はソフトウェア開発に革命をもたらしましたが、大きな開発グループにアジャイルを適用することに対しては「やめておけ」、「あくまで小さなチーム向けだから…」、「スクラムはチームレベルに閉じて行うべき」といったネガティブなコメントをする人間が多いというのが現実です。開発チームに人を追加しすぎる事は避けるべきという見解は確かに正しいものの、大規模プロダクト開発がこの世から消えることはないことを考えると、うまくアジャイル開発手法を大規模プロダクト開発に適用させる方法を発見する必要があるのは明白です。

<!---
We (Craig and Bas) have been involved in software development for a long time in all sorts of roles in traditional sequential-lifecycle development, Unified Process, CMMi and others. None felt *right*. Scrum, on the other hand, felt right for single-team development. So, the question then became "How can we scale Scrum *without* losing its strength?"
--->

我々（Craig と Bas）は、長きに渡り、従来型のシーケンシャルなライフサイクルに基づく開発、Unified Process、CMMi等といったソフトウェア開発手法において色々な役割を経験してきましたがどれも *正しい* と感じることができませんでした。一方でスクラムは単独チームによる開発に限って言えば正しい手法であると感じました。このことから、我々は「いかに *スクラムの長所を殺すこと無く* スケールさせるか」を考えるようになりました。

<!---
## LeSS is Scrum scaled
--->

## LeSS はスケールしたスクラムである

<!---
What is the strength of Scrum? That is not an easy question to answer. Of course, the concepts and principles behind Scrum, such as [Transparency](../principles/transparency.html), [Empirical Process Control](../principles/empirical_process_control), Iterative development, and [Self-managing teams](../management/self_managing_teams.html) are critical. Those principles have been around for quite a while, however, so their inclusion does not explain Scrum’s success. After much discussion, we have concluded:
--->

そもそもスクラムの強みとは何でしょう？これは簡単に答えられる質問ではありません。当然ながら、[透明性](../principles/transparency.html)や[経験則に基づくプロセスコントロール](../principles/empirical_process_control)、イテレーションによる開発、[自己管理化されたチーム](../management/self_managing_teams.html)等といった、スクラムの背景にある概念や原則はとても重要です。しかし、これらの原則はかなり昔から提唱されていたものであり、これらがスクラムが成功した原因であるとは言い切れない面があります。

議論を重ねた結果、我々は次のように結論に至りました。

<!---
Scrum hits the sweet spot between abstract principles and concrete practices.
{: .box_top_bottom  .text_centered_bold }
--->

スクラムは、抽象的な原則と具体的な慣行との間のスイート・スポットをうまく捉えている。
{: .box_top_bottom  .text_centered_bold }

<!---
Thus, in order to keep [Large-scale Scrum as Scrum](../principles/large_scale_scrum_is_scrum.html), we'll need to find a similar balance, so that we will be able to say:

For large groups, LeSS hits the sweet spot between defined concrete elements and empirical process control.
{: .box_top_bottom  .text_centered_bold }
--->

そこで、我々は[スクラムを大規模スクラム](../principles/large_scale_scrum_is_scrum.html)として維持するためには、同じようなバランスを保つ必要があると考えました。すなわち、次のように考えたのです。

大規模チーム開発向けに、LeSS は具体的に定義された要素と経験則に基づくプロセスコントロールとの間のスイートスポットをうまく捉える必要がある。

<!---
This leads to some decisions:

* LeSS needs to be simple
When scaling, there is a tendency to add roles, artifacts, processes, etc. This should be avoided so that a process can empirically be created by the product group. Most other scaling frameworks fall into the trap of providing a defined process. In LeSS we want to avoid that trap.
* LeSS is Scrum Scaled
  Rather than having Scrum as a building block for a scaled framework, we need to look at Scrum and for each element ask "Why is it there?" followed by “If we have more than one team, how can we achieve the same purpose on a larger scale?”
* Scaled up instead of tailored down
A common concept for process development is to define a universal, overarching framework and then contextually tailor it down. This does not work well because people often assume everything is needed in their particular context. This assumption often leads to the creation of bloated processes. LeSS should be kept to the minimum. We acknowledge that scaling will require “more” but instead of “polluting” LeSS with optional elements, we have separated out a different framework [LeSS Huge](../less-huge/index.html).
--->

このことを踏まえ、我々は次のように方向性を定めました。

* LeSS はシンプルでなければならない
開発プロセスのスケールアップを検討する際、役割や成果物、プロセスなどを増やしてしまう傾向があります。開発グループによる経験則に基づいたプロセスを促進するために、これは避けなければなりません。プロセスをかっちりと定義してしまうという罠に数多くの「スケール性」を謳うフレームワークが陥っています。LeSS はこの罠を回避するもにしたいと我々は考えました。

* LeSS はスケールしたスクラムである
スクラムをスケールしたフレームワークの構成要素として捉えるのではなく、スクラムの各要素に対して「この要素が存在する目的は何か？」、「複数チームを前提にした場合、同じ目的をより大きなスケールで実現するためにはどうすればよいか？」を検討する必要があると考えました。

* そぎ落としではなくスケールアップ
プロセス開発の一般的な考え方は、まず汎用的・包括的なフレームワークを定義し、これをコンテキストに応じてそぎ落としていくというものです。しかし我々はこの考え方はうまくいかないと考えました。あるコンテキスト実現のためにすべての要素が必要であると考えてしまうことが多いため、結果としてプロセスが肥大化してしまうことが多いのです。もちろんスケールアップのための「要素追加」は必要ですが、要素追加で LeSS を「汚染」する代わりに、我々は [LeSS Huge](../less-huge/index.html) という別のフレームワークを用意することを選択しました。

<!---
## LeSS uses experiments
-->

## 経験則に基づく LeSS

<!--
In our first two books, [Scaling Agile and Lean Development](http://www.amazon.com/Scaling-Lean-Agile-Development-Organizational/dp/0321480961) and [Practices for Scaling Agile and Lean Development](http://www.amazon.com/Practices-Scaling-Lean-Agile-Development/dp/0321636406), we framed large-scale Scrum as a set of experiments with the principle:

There are no such things as best practices. There are only practices that are good within a certain context.
{: .box_top_bottom  .text_centered_bold }
-->

我々が過去に出版した２冊の本（[Scaling Agile and Lean Development](http://www.amazon.com/Scaling-Lean-Agile-Development-Organizational/dp/0321480961) と [Practices for Scaling Agile and Lean Development](http://www.amazon.com/Practices-Scaling-Lean-Agile-Development/dp/0321636406)）において、我々は大規模スクラムを次のような思想に基いた実験のセットとして定義しました。

ベストプラクティスなどというものは存在しない。あるコンテキストに対してうまくハマるプラクティスが存在するのみである。
{: .box_top_bottom  .text_centered_bold }

<!--
Thus, the books are full of experiments that we have done. Certain things we recommend you try, certain things we recommend you avoid, and others we caution will work in some contexts but are terrible in others. This worked well and we have received a lot of positive feedback about this approach. 
-->

この上で、前出の２冊では我々が行ってきた実験をまとめ、「我々が実践をオススメするもの」、「逆に実践すべきではないもの」、「あるコンテキストにおいてはうまくいくが他のコンテキストにおいてはまったくうまくいかないもの」等について解説を行いました。この試みはうまくいき、読者の方より多くの良い評価を頂くことができました。

<!--
We also got feedback from people who were a bit confused. They needed more to hold on to... something less context-specific ... some rules. Based on this feedback, we reflected and returned to the Shu Ha Ri model of learning:

<figure>
  <img src="/img/framework/shuhari.png" alt="shuhari.png">
</figure>
-->

一方、内容が少し分かりにくいというフィードバックも頂きました。これは、ある特定のコンテキストに基づいた説明ではなく、もっとルールベースの説明がほしいというコメントでした。このフィードバックを踏まえ、我々は学習の「守破離」モデルに立ち返ることにしました。

<figure>
  <img src="/img/framework/shuhari.png" alt="shuhari.png">
</figure>

<!--
This model shows the different stages that learners go through when learning new concepts:

* Shu---Follow rules to learn basics
* Ha---Break rules and discover context
* Ri---Mastery and find your own way
-->

このモデルは、人が新しい概念を会得する過程で通る段階を表しています。

* 守---基本を学ぶためにルールに従う
* 破---ルールを破りコンテキストを発見する
* 離---熟練者として独自の道を発見する

<!--
We realized that our previous scaling work did not provide anything on the shu level, which caused difficulty and confusion for people who had just started agile development in large product groups. This became even more obvious when other, more predictive scaling approaches started offering beginner level advice. Hence...
-->

我々は、今まで「守」段階の読者に対して何も有益な情報を提供していないことに気がつきました。結果、大規模製品開発グループにおいてアジャイル開発を始めたばかりの読者にとっては、とっつきにくく理解が難しい内容になっていました。他のスケール性を謳うアプローチが初心者レベルのアドバイスを行うようになったことからもこの問題点は明白でした。

このような反省を踏まえ、LeSSは次のようなものになりました。

<!--
## LeSS as a framework
-->

## フレームワークとしての LeSS

<!--
LeSS is more than a set of principles and experiments. It also provides a framework with rules. The [LeSS Rules](../rules/index.html) define what is LeSS (and what isn't) and they provide a concrete framework for applying LeSS. Within the LeSS Framework, product groups can apply the experiments and discover what works best for them at a certain moment.
-->

LeSS は原則と経験則のセットを提供するだけではなく、ルールに基づくフレームワークを提供するものです。[LeSS ルール](../rules/index.html)は LeSS とは何か（何ではないか）を定義し、LeSS を適用するための具体的なフレームワークを提供します。このLeSSフレームワークの中で、製品開発グループは自分たちの経験則を当てはめ、ある瞬間において何がベストなのかを発見することができるようになっています。

<!--
This is also the basis of the third LeSS book, simply called [Large-Scale Scrum](http://www.amazon.com/Large-Scale-Scrum-More-Craig-Larman/dp/0321985710). In this book, LeSS is defined as:

* LeSS Rules that provide the LeSS framework (and the LeSS Huge framework for larger product groups)
* Guides for adopting LeSS
* Experiments from the first two books.
-->

これは我々の３冊目の本（[Large-Scale Scrum](http://www.amazon.com/Large-Scale-Scrum-More-Craig-Larman/dp/0321985710)）でもカバーされています。この本では LeSS に関する以下の項目がカバーされています。

* Less フレームワーク（および、大規模製品開発チーム向けである LeSS Huge フレームワーク）を提供する LeSS ルール
* LeSS 導入へ向けたガイド
* 最初の２冊の本より抜粋した経験則

<!--
This way ensures that LeSS is simple and stays true to the Scrum nature. Yet, like Scrum, LeSS provides enough concrete practices to start and enough flexibility and power to scale.
-->

このようにLeSSはスクラムの本質を守ったシンプルな構成になっています。さらにスクラム同様、スタートのための明確な慣例とスケールのための柔軟性やパワーを持つものになっています。
