---
layout: mechanics
title: Continuous Integration
order: 10
---

# Continuous Integration

---

<div style="text-align: right;">
The use of COBOL cripples the mind; <br/>
 its teaching should, therefore, be regarded as a criminal offense. <br/>
--Edsger Dijkstra <br/>
<br/>
<b>COBOLを使っていると人は無能になってしまう。 <br/>
COBOLの教育は犯罪とみなすべきである。 <br/>
-- エドガー・ダイクストラ
</b>
</div>

---

継続的インテグレーション（CI）は大規模のリーンとアジャイル開発には欠かせないものだ。

> Our conclusion is that there is no inherent reason why Continuous Integration and Automated Build processes won’t scale to any size team. 
In fact… [they] become more essential than ever.

> 筆者らの結論としては、継続的インテグレーションと自動ビルドのプロセスが、あらゆる規模のチームに合わせて使おうとしない理由などない、ということだ。
実際、これまで以上に欠かせないものとなっている。

With CI, developers gradually grow a stable system by working in small batches and short cycles–a lean theme. 
This enables teams to work on shared code and increases the visibility into the development and quality of the system.

CIで、開発者は小さなサイズで短いサイクル、すなわちリーンによって、徐々にしっかりしたシステムを育てる。
これによってチームが共有されたコードで作業できるようになり、システムの開発状況と品質の見える化が促進される。

There are misconceptions about CI; it seems a simple concept, but in practice it’s not. 
To get one misconception out of the way: Continuous integration is not automating the build and running tests.

CIに対する誤解として、シンプルなコンセプトに見えるというのがあるのだが、実際やってみるとそうではない。
とんでもない誤解を一つあげると、CIでビルドの自動化とテストの実行を行わない、というものだ。

The classic paper on CI states:

CIについて述べられた古い（Martin Fowlerの）記事によると、

> Continuous Integration is a software development practice where members of a team integrate their work frequently, usually each person integrates at least daily - leading to multiple integrations per day. 
Each integration is verified by an automated build (including test) to detect integration errors as quickly as possible.

> 継続的インテグレーションはソフトウェア開発のプラクティスである。チームメンバーは彼らの成果を頻繁に統合し、少なくとも1日に一回以上、それぞれのメンバーが統合する。
各統合は、統合失敗をできるだけ早く検出できるよう、（テストを含んだ）自動テストによって検証される。

---

## Continuous Integration Practices

Continuous Integration is:

継続的インテグレーションというのは、

* a developer practice…
* to keep a working system
* by small changes
* growing the system
* by integrating at least daily
* on the mainline
* supported by a CI system
* with lots of automated tests

* 開発者のプラクティス
* 動くシステムを保つ
* 小さな変更による
* システムを育てる
* 少なくとも1日1回統合する
* 本流に沿う
* CIシステムのサポート
* たくさんの自動テスト

である。

### Developer Practice

Discussions about CI all too often are about tools and automation. 
Though important, CI in essence is a developer practice. 
Owen Rogers, one of the original creators of CruiseControl.NET writes:

CIについての議論は全て、ほとんどがツールと自動化に関するものになりがちだ。
重要ではあるのだが、CIは本質的には開発者のプラクティスだということである。
CruiseControl.NETの初期のクリエイターの1人であるOwen Rogersが言うには、

> Continuous integration is a practice–it is about what people do, not about what tools they use. 
As a project starts to scale, it is easy to be deceived into thinking that the team is practicing continuous integration just because all of the tools are set up and running. 
If developers do not have the discipline to integrate their changes on a regular basis or to maintain the integration environment in a good working order they are not practicing continuous integration. 
Full stop. [[Rogers04]](http://link.springer.com/chapter/10.1007%2F978-3-540-24853-8_8)

> 継続的インテグレーションはプラクティスである。人がなにをするかであり、何のツールを使うかではないのだ。
プロジェクトが大きくなり始めると、全てのツールがセットアップされ動いてるので、チームはCIをやっているのだといとも簡単に誤解してしまう。
もし開発者が、習慣的に自分たちの変更を統合する、あるいは統合環境が順調であるよう維持する、といった訓練を受けていないのであれば、彼らは継続的インテグレーションをやってるとはいえない。
以上。

Splitting changes into small increments, integrating them at least daily, and having the discipline to not break the build are all done by the individual developer. 
He needs the skill to work in small increments and keep his own copy of the system (or part of the system) working all the time.

変更を小さなインクリメントに分割し、少なくとも1日1回それらを統合し、そしてビルドを壊さないよう訓練を受けていることが、個々の開発者全てによってすべてなされているべきだ。
開発者は、小さなインクリメントで作業し、作業中ずっと自分用のシステムのコピー（かあるいはシステムの一部）を維持するスキルを要するのだ。

Adopting CI requires a change in human behavior. 
We worked with several large products with an excellent automated build but where developers did not integrate their code frequently. 
Even worse, the message “thou shall not break the build” was strongly promoted, for example, by shaming the people who broke the build. 
The predictable result? 
Developers would delay their integrations out of fear of breaking the build. 
Despite their excellent always-green (always passing) automated build, they are doing the opposite of CI.

CIの適用は、人としての振る舞いに変化を要する。
筆者らは、よくできた自動ビルドではあるが、開発者が彼らのコードを頻繁に統合していないという、いくつかの大きなプロダクトで仕事をした。
さらに悪いことに、「汝、ビルドを壊すことなかれ」というメッセージがかなり強調され、例えば、ビルドを壊すと恥さらしになる、といったことが行われていた。
結果どうなると思う？
開発者はビルドを壊すことが怖くて、彼らの統合が遅くなってしまうだろう。
彼らのすばらしい常にグリーン（で常にパスしたもの）である自動ビルドであるにもかかわらず、CIとは正反対のことをしているのだ。

Test-driven development (TDD) with constant refactoring helps. 
When a developer is unit-test-driving his code, he ensures that his local copy is always working. 
All the tests pass all the time. 
In theory, he is able to integrate code every TDD cycle (about ten minutes); in practice, he integrates after a couple of cycles.

コンスタントにリファクタリングを行うテスト駆動開発（TDD）が助けとなる。
開発者が単体テスト駆動で自分のコードを書いている時、自分のローカルコピーが常に動いていることを確かなものとする。
全てのテストがいつもパスするのだ。
理論的には、（C++でだいたい10分で、Cではもっと長いしJavaだともっと短いだろう）すべてのTDDサイクルでコードを統合することができる。実際にはいくつかのサイクルの後、統合する。

CI on large products is hard precisely because it is a developer practice. 
If it were only about tools and automation, you could simply start a CI project or hire a company to “install CI.” 
But as a developer practice, CI requires a change to the daily habits of all developers. 
With many people, this is hard, takes time, and requires coaching.

大きなプロダクトのCIは、開発者のプラクティスであるがゆえまさに困難なものである。
もしツールや自動化についてのことだけであれば、CIのプロジェクトをシンプルに開始できるし、「CIをインストールする」仲間を雇える。
しかし、開発者のプラクティスなので、CIはすべての開発者に日々の習慣を変えることを求める。
多くの人にとって、これは大変で、時間がかかり、コーチが必要であったりする。

With the right behavior, the developers will…

正しくふるまうことで、開発者は。。。

### Keep a Working System

Similar to the lean concept of jidoka , CI means always having a stable system. 
When a test fails–run locally or on the CI system–the developer fixes it immediately and therefore always keeps a working and stable system.

リーンにおける「自働化」の概念同様、CIは常に安定したシステムを意味する。
テストが失敗した時、ローカルだろうがCIシステム上だろうが、開発者はそれをすぐに修正することで、役に立って安定したシステムを維持する。

Traditional sequential development has un-integrated work-in-progress (WIP). 
Nobody knows if these parts work together or if they are free of defects. 
WIP makes it hard to predict when, or if, the system is deliverable. 
CI increases visibility by removing this WIP–always having everything integrated–and with this comes more control and predictability.

伝統的でシーケンシャルな開発では、統合されていない仕掛品（WIP）がある。
これらの部品を一緒にしたら動くのか、あるいは欠陥がないのかは誰も知らない。
WIPはシステムの納品をいつできるのか、あるいは納品できるのか否か、の予想を難しくする。
CIは、常にすべてのものを統合し、このWIPを取り除くことで見える化を促進し、そしてこれにより制御しやすくまた予想できるようになる。

> Note : CI and iterative and incremental development in Scrum have the same strategy. 
However, CI is a more fine-grained level than a Scrum iteration. 
Both reduce variability, uncertainty, and risk by working in small batches--iteratively.

> 注釈 : CIとスクラムの反復的で漸進的な開発は同じ戦略を持つ。
しかしながら、CIスクラムのイテレーションよりきめ細かいレベルである。
どちらも反復的に、小さいサイズで作業を行うことで、変わりやすさ、不確かさ、リスクを減らす。

This working system, evolved in small increments, is created by…

この役に立つシステムは、小さなインクリメントが含められ、作られるのだがそれは。。。

<img class="rounded shadowed" src="http://less.works/img/technical-excellence/xcontinuous-integration-chicken.png.pagespeed.ic.nvadKU22pt.png" alt="continuous-integration-chicken.png" pagespeed_url_hash="3833794616" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

> Rubber Chicken<br/>
「アート・オブ・アジャイルデベロップメント」の著者でアジャイルな開発者であるJames Shoreは、開発者のプラクティスとしてのCIを強調している。
彼のとても素晴らしい記事である Continuous Integration on a Dollar a Day では、彼は古い開発用コンピュータ、鶏のゴム人形、デスクのベル、そして自動ビルドを用いたCIの仕方について説明している。
古い開発機は、統合用のマシンとして使われる。
鶏のゴム人形は、それを持つ人だけがコードを統合できるという統合のトークンである。
デスクのベルは統合成功をアナウンスするものである。
しかし彼のCIについての記事においてもっとも重要なステップは、開発者を一つの部屋にまとめ、彼らがお互いに「これから、バージョンコントロールにある僕らのコードはいつでもビルドが通り、テストもパスするようにね。」ということについて合意する、ということだ。
<br/>
鶏のゴム人形は大きなプロダクトには合わない。
とはいうものの、この話はCIが開発者のプラクティスであることを鮮明に思い出させてくれる。


### Small Changes

We once worked with a gateway product group in Finland who needed to make a change to their protocol stack. 
They insisted it could not be split into small changes. 
They made the large change and spent three months trying to get the system to work again. 
After that painful experience, they agreed to never make such large changes in one big batch.

筆者らはフィンランドにある企業のゲートウェイ製品グループで働いたことがある。彼らは自分たちのプロトコルスタックを変更する必要に迫られていた。
彼らは小さな変更には分けられないと主張していた。
彼らは大きな変更を行い、システムが再度動くようになるまでに3ヶ月費やした。
この苦い経験の後、彼らはあんな大きなサイズの変更は決して行わない、ということに合意した。

Large changes to a stable system will destabilize and break it in large ways .
The larger the change, the more time it takes to get the system back to a stable state.

安定したシステムへの大きな変更は、ひどく不安定で壊れたものにしてしまうだろう。
変更が大きければ大きいほど、システムを安定した状態へ戻すのにより沢山の時間が費やされるのだ。

Avoid large changes.
Instead, break each change into small changes–the lean concept small batches.
Each change integrates in the system easily.

大きな変更は避けるべし。
その代わり、各々の変更を、リーンのコンセプトでスモールバッチと呼ばれる、小さなサイズに分割しよう。
それぞれの変更は簡単にシステムに統合できる。

By small changes you will be…

その小さな変更によって。。。

### Growing the System

Growing versus building is an important mindset shift.
Brooks, in his famous article, No Silver Bullet , reflects on his experience:

育てることと構築することの違いは、重要マインドセットの移行である。
Brooksは彼の記事「銀の弾丸などない」で、彼の経験を踏まえている。

> The building metaphor has outlived its usefulness… If, as I believe, the conceptual structures we construct today are too complicated to be accurately specified in advance, and too complex to be built faultlessly, then we must take a radically different approach… The secret is that it is grown, not built… Harlan Mills proposed that any software system should be grown by incremental development… Nothing in the past decade has so radically changed my own practice, or its effectiveness… The morale effects are startling.
Enthusiasm jumps when there is a running system, even a simple one… One always has, at every stage in the process, a running system.
I find that teams can grow much more complex entities in four months than they can build.

> 構築するというメタファはその有用性で長生きしている。。。
もし、私が信じるように、今日我々が構築する概念上の構造は、前もって正確に明示されるにはあまりにも込み入っており、また失敗することなく構築されるにはあまりにも複雑なので、我々は根本的に異なるアプローチを取る必要がある。。。
Harlan Millsはソフトウェアシステムがインクリメンタルに育てられるべきだ、と述べている。。。
ここ10年で、私自身のプラクティスやその有効性を、かなり根本的なところで変更したものはない。。。
モラルの効果には驚かされる。
熱意は、稼働しているシステムがあれば、たとえそれが単純なものであったとしても、急上昇する。。。
プロセスのどのステージであれ、稼働しているシステムがある。
私は、チームが構築できる以上に、4ヶ月で非常に複雑なものに育てられることを知っている。

Building a system implies building separate components and, when they are finished, assembling them together.
Growing a system implies nurturing it and evolving it into a larger system (See grow-ing versus building.).

システムを構築するということは、分離したコンポーネントの構築を含み、それらが完了すれば、一つにまとめられる。
システムを育てるということは、まさしくそれを育てることであり、大きなシステムへと徐々に発展していく。

<img src="http://less.works/img/technical-excellence/xcontinuous-integration-grow-versus-bolt.png.pagespeed.ic.37eTdjZE2e.png" alt="grow-versus-bold" pagespeed_url_hash="406211021" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

Is this possible in big systems with legacy code? We get that question frequently.
In almost every case, the answer is yes .
If your developers or architects cannot do this or claim it is not possible, take that as a sign of lack of skill.

これはレガシーコードの大きなシステムにおいても可能だろうか？
筆者らはよくその質問を受ける。
殆どのケースにおいて、答はイエスだ。
もし開発者やアーキテクトがやれずにいるか、不可能だと主張するのであれば、スキル不足の兆候だと受け取るべし。

A developer continuously integrates his work while working on a task.
He does not wait for the task or the whole feature to be complete and then “bolt it” on the system.
Rather, whenever a small amount of work can be integrated without breaking the system, then he integrates it…

開発者は、タスクをこなしている間は彼の作業を継続的に統合する。
開発者はタスクかあるいは完全なフィーチャーが完成するのを待つことなく、システムに「仕込む」。
むしろ、小さな作業の集まりが、システムを壊すことなく統合できるのであればいつでも、開発者はそれを統合する。。。

### At Least Daily

How frequent is ‘continuous’? As frequently as possible! This is limited by

「継続的」とはどのくらいだろうか？可能なかぎり頻繁にということだ！これには次の制限を受ける。

- the ability to split large changes
- speed of integration
- speed of feedback cycle

- 大きな変更を分割する能力
- 統合するスピード
- フィードバックサイクルのスピード

Ability to split large changes –splitting large changes into smaller ones, while keeping the old functionality working, is a skill that must be learned.
The better developers are at this splitting, the more frequently they can integrate.
TDD, in short ten-minute cycles, is an excellent technique for this.

**大きな変更を分割する能力** - 機能を維持しつつ大きな変更を小さく分割するということは、学ぶべきスキルだ。
開発者がより優れているほど、この分割で彼らはより頻繁に統合できている。
10分程度のサイクルでのTDDは、これの非常に良いテクニックとなる。

Speed of integration –the more time it takes to integrate changes into the code repository, the less frequently developers will do so.
Changes are batched for the sake of efficiency.
Integration effort is impacted by the process overhead (the transaction cost), such as approvals and reviews needed before developers are allowed to integrate.
Reduce this overhead or find creative ways to do things differently.
For example, we worked with a 40-person product group where the check-in message had to mention the person who had reviewed the code.
The result? Developers batched many changes to make the code reviews more ‘effective’ and thus delayed integration–a local optimization.
Solution? Code reviews can instead be done on already integrated code–not delaying the integration.

**統合のスピード** - コードリポジトリに変更を加えて噛合するのに時間がかかるほど、開発者がそうする頻度が減っていく。
変更は効率化のために大きな塊になってしまう。
統合の努力は、開発者が統合する前に承認やレビューを要するような、プロセスのオーバーヘッド（やりとりのコスト）に影響を受ける。
オーバーヘッドを減らすか、違ったやり方を見つけよう。
例えば、筆者らは誰がコードをレビューしたのかというメッセージをチェックイン時のメッセージに残すという、40人のプロダクトグループで仕事をしたことがある。
どうなったかって？
開発者はコードのレビューをより「効率的」に行うよう沢山の変更を一つにまとめ、それによって統合が遅れるという、局所最適に陥った。
解決策は？
コードレビューは、すでに統合されたコードで終わらせられたことにできる。これで統合は遅れない。

Speed of feedback cycle –a developer should only integrate changes that do not break existing tests.
Ideally, he runs all the tests before integrating.
For this to be possible, the tests must run very fast.
If they are slow, the developer will delay the integration to “work more efficiently.” However, running all the tests quickly is hard for large systems.
Therefore, developers only run a subset of tests before checking in, and a CI system runs the remaining tests.
The CI system acts as a safety net by giving the developer feedback about the tests he did not run.
What happens when the CI system is slow? First, there will be many changes during one cycle, increasing the chance the build breaks.
Second, developers do not integrate their changes in the broken build; rather, they batch them.
Finally, when the build is fixed, all developers integrate their batched changes, leading to a high chance of breaking the build again.
Therefore, the safety-net-feedback cycle has to be fast.
This decreases the chance the build will break and increases the ability to check in more frequently.

**フィードバックサイクルのスピード** - 開発者は既存のテストを壊さない変更のみを統合すべきだ。
理想的には、全てのテストを統合前に実行していると良い。
これを可能とするには、テストがとても早く実行できるべきだ。
もし遅いようなら、開発者は「より効率良く働く」ために統合を遅らせるだろう。
しかしながら、全てのテストを実行することは、大きなシステムでは困難だ。
なので、開発者はチェックインの前にテストのサブセットのみを実行し、CIシステムが残りのテストを実行する。
CIシステムは、開発者が実行しなかったテストのフィードバックを返すことでセーフティーネットとして振る舞う。
CIシステムが遅かったらどうなるだろう？
まず、一つのサイクル中に多くの変更が含まれ、ビルドが壊れる問題が増加するだろう。
そして、開発者はビルドが壊れているうちは彼らの変更を統合しなくなり、それらを大きなバッチにするだろう。
そして終いには、ビルドが治った時、すべての開発者が大きなバッチになった変更を統合し、再びビルドが壊れる問題がより多発することになるだろう。
それゆえ、セーフティーネットのフィードバックサイクルは早くあるべきなのだ。
これはビルドが壊れる問題を減らし、より頻繁にチェックインできる機会を多くしてくれるのだ。

Rule of thumb for large products moving to agile and lean development: All developers integrate at least daily.
Even though “daily builds are for wimps ” [Jeffries04], daily is a first step for large products.
Recall the “lake and rocks” metaphor used in lean thinking–the big rock of just being able to build once a day with everyone’s updates is hard enough on big old systems with 300 developers in four countries.
Eventually, that big rock is removed, and shorter cycles are possible.

大きなプロダクトでのアジャイルやリーン開発への移行をおおまかにいとこうだ。
すべての開発者は少なくとも1日に1回統合する。
[「意気地なしのデイリービルド」](http://www.amazon.com/dp/0735619492)だとしても、日次実行は大きなプロダクトでの第一歩である。
リーン思考の「水と石」のメタファを思い出そう。
全員の更新分を1日に1回ビルドできるようにする際の大きな岩は、4つの国で300人の開発者がいる大きな古いシステムではとても困難なものだ。
最終的に大きな岩は取り除かれ、短いサイクルが可能となる。

On large products, it will take time to learn to split changes, simplify the integration process, and set up a fast CI system running…

大きなプロダクトでは、変更の分割を学ぶには時間がかかるだろうが、統合プロセスを単純化し、早いCIシステムをセットアップし、、、

### On the Mainline

Developers integrate on the mainline or trunk [BA03].
Making changes on a separate branch means that the integration with the main branch is delayed.3 The current status is not visible, so you do not know if everything works together.

開発者はメインラインかtrunkに統合する。
異なるブランチに変更を加える事は、メインのブランチでの統合が遅れることを意味する。
現在の状況が見えないので、全てが一緒に動くかどうかはわからないだろう。

Branching during development breaks the purpose of CI and should be avoided.
There are exceptions: First, customers might not want to upgrade their product to the latest release but still want patches.
Thus, release branches are needed.4 Second, when scaling up a CI system, it can be useful to have very short-lived branches that are automatically integrated in the mainline–more about that later.

開発中のブランチ分けはCIの目的を壊すので、避けるべきである。
が、例外はある。
一つ目は、顧客が彼らのプロダクトを最新リリースにアップグレードをしたいとは思っておらず、パッチを当てたいと思っている場合だ。
これにはリリースブランチが求められる。
二つ目は、CIシステムがスケールアップした時、メインラインでの統合を自動で行うかなり短命のブランチを作るのは有用だろう。
これについては後述する。

What about branching for customization? Bad idea! Instead, manage these through a configurable design or parameterized build instead of using your Software Configuration Management (SCM) system.
We once worked on a network-optimizing product being built by a co-located product group who insisted on branching for different configurations.
Developers worked on these separate branches for over a year.
Afterwards, it took them an additional half-year –and lots of fighting–to merge them in the trunk.

カスタマイズ用のブランチはどうだろう？
それは悪い考えだ！
そうではなくて、フトウェア構成管理システムを使う代わりに、設定可能な設計やパラメタライズドビルドを通して管理するのだ。
筆者らはかつて、異なる構成にブランチを使用することにこだわった一箇所にまとめられたプロダクトグループによって構築された、ネットワーク最適化プロダクトの仕事に関わったことがある。
開発者はい年以上を通して分離したブランチで作業を行っていた。
その後、trunkにそれらをマージするのに多くの格闘とともに更に半年費やしていた。

Successful mainline development is…

メインラインの開発をうまくやるには、、、

### Supported by a CI System

Lean emphasizes minimizing inventory–one type of waste.
Inventory acts as a buffer (another queue) in which mistakes are hidden.
Mistakes become painfully visible when these buffers are removed–and that is a good thing.
The same thing happens when all changes are integrated directly to the mainline.
All developers update their local copy frequently; when someone checks in broken code, it is visible to everybody–they will be annoyed.

リーンはムダの一つである在庫の最小化を強調している。
在庫は、誤りが隠蔽されてしまうバッファやキューとして振る舞う。
誤りはバッファが取り除かれると痛々しさが目に見えるものとなるが、それはいいことなのだ。
同じようなことが、すべての変更がメインラインで直接統合されるときに現れる。
すべての開発者はローカルコピーを頻繁に更新する。
誰かが壊れたコードをチェックインしてしまうと、みんなに対して可視化されているので、彼らはイラつくだろう。


People make mistakes.
That’s OK.
A lean stop-the-line safety net is needed to detect them early.
Developers fix a mistake before it affects others.
This safety net, an andon -like system, in Toyota terminology, is a CI system.

人はミスを犯してしまうものだ。
それは仕方がない。
リーンのラインを止めるセーフティーネットは、それらを素早く検知するためのものだ。
開発者は他に影響を及ぼす前にミスを修正する。
この、トヨタの用語で言うあんどんのようなシステムであるセーフティーネットはCIシステムなのだ。

<img src="http://less.works/img/technical-excellence/xcontinuous-integration-system.png.pagespeed.ic.-b-wfzT07E.png" alt="continuous-integration-system.png" pagespeed_url_hash="215266350" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

A CI system (See CI system.) listens to the SCM system.
When a developer checks in code, the CI system checks out all the code and compiles it, runs some tests, installs it, and runs more tests.
All this happens fast; Extreme Programming recommends within ten minutes.
If a developer breaks the build, the CI system will query the SCM system and find out who made the change.
It sends him e-mail saying: “You broke the build, fix it!” Fixing the broken build is the number one priority because it affects everybody.

CIシステムはSCMをリスンする。
開発者がコードをチェックインすると、CIシステムは全てのコードをチェックアウトしてコンパイルし、いくつかの種類のテストを実行し、インストールし、そしてさらに別のテストを実行する。
これら全ては素早く行われる。
XPでは10分以内と述べている。
もし開発者がビルドを壊してしまったら、CIシステムはSCMシステムに問い合わせ、どの変更によるものかを見つける。
そしてその開発者に対し、「ビルドを壊したので修正するように！」とメールを送り付ける。
壊れたビルドを修正することは全員に対して影響をおよぼすので、No.1のプライオリティを持つ。

For a small product, it is easy to have a fast, ten-minute build.
For a large product with legacy code and many people, it is quite a challenge.
Later, this chapter examines several techniques for scaling up a CI system…

小さなプロダクトでは10分以内に素早くビルドを行うことは容易だ。
レガシーコードと多くの人が関わる大きなプロダクトでは、かなりのチャレンジとなる。
後ほど、このチャプターでCIシステムのスケールアップに関する幾つかのテクニックについて考察する、、、

### With Lots of Automated Tests

It is not very hard to have a CI system compile everything; it’s not very useful either.
You want to have as many tests as possible running in your CI system.
The more automated tests, the better your safety net and the more confidence your system is working.

CIシステムに全てをコンパイルさせることはそれほど大変でもないし、それほど有益なものでもない。
CIシステムで走らせられるだけのテストをほしいと思うだろう。
自動テストが多いほど、セーフティーネットが良くなり、システムが動くという自信がより持てるだろう。

For new products, creating automated tests is not hard.
However, many large products have legacy code without automated tests.
Developers need to add automated tests–which is a lot of work.
The chapter on legacy code covers this.

新規のプロダクトでは、自動テストを作るのはそれほど大変でもない。
がしかし、多くの大きなプロダクトは、自動テストのないレガシーコードを持つ。
開発者は自動テストを追加する必要があるが、それは多くの作業を要する。
レガシーコードの章でこれを扱う。

### Scaling a CI System

First, the build and test need to be fully automated.
Many large products groups we worked with have manual steps in their build.
See the recommended readings for texts that are useful for automating the build.

まず、ビルドとテストは完全に自動化できている必要がある。
筆者らが働いていた多くの大きなプロダクトはビルドのステップがマニュアル化されていた。
自動ビルに関する有用なおすすめ記事を見ること。

The obstacles for scaling a CI system relate to more people producing more code and tests.
First, the probability of breaking the build increases with more people checking in code.
Second, an increase in code size leads to a slower build and thus a slower CI feedback loop.
These together can lead to continuous build failure (See the dynamics of broken builds.).

CIシステムをスケーリングする際の障害は、より多くの人がより多くのコードとテストを生み出しているかに関わる。
最初に、ビルドが壊れる可能性は多くの人がコードをチェックインするにつれ増大化していく。
次に、コードのサイズの増加がビルドを遅くしてしまうので、CIのフィードバックループも遅くなってしまう。
これらはともに継続的ビルドの失敗へと繋がるのだ。（ビルド失敗のダイナミクスの図を参照）

<img src="http://less.works/img/technical-excellence/xcontinuous-integration-causal-loop-ci-number-of-people.png.pagespeed.ic.IEXxsQEX8M.png" alt="continuous-integration-causal-loop-number-of-people" pagespeed_url_hash="884724140" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

The solutions are simple:

解決策は単純だ。

* speed up the build
* implement a multi-stage CI system

* ビルドの速度を上げる
* マルチステージのCIシステムを実装する

Job one: Speed up the build.
If the whole product can be compiled and tested within one second , then scaling techniques are not needed.
The one-second build is out of reach for large products, for now .
Though every improvement brings us closer, the one-second build helps.
Giving general guidelines for speeding up builds is hard–it’s often product specific.
Some general solutions [Rasmusson04]:

最初の作業は、ビルドの高速化だ。
もしすべてのプロダクトが1秒でコンパイルとテストを実行できるなら、スケールするテクニックは不要だろう。
1秒ビルドは大きなプロダクトでは今のところ難しい。
しかし、全ての進歩は1秒ビルドに近づく助けとなる。
ビルドの高速化の一般的なガイドラインを提供することは難しい。
プロダクトの特性によるからだ。
いくつかの一般的な解決策はこれだ。

* add hardware
* parallelize
* change tools
* build incrementally
* deploy incrementally
* manage dependencies
* refactor tests

* ハードウェアの増設
* 並列化
* ツールの変更
* 増分ビルド
* 増分デプロイ
* 依存性の管理
* テストのリファクタ

Add hardware –the easiest way to speed up the build is to buy more hardware.
Throw a couple of extra computers, extra memory, or a faster network connection at the problem and it goes away.
Upgrading existing hardware takes investment and only minimum effort, making it the easiest and best choice.
The build of one telecom product speeded up 50 percent by compilation on a RAM disk–and this only required a memory upgrade.

**ハードウェアの増設** - ビルドの高速化の最も手っ取り早い手段はハードウェアを買い足すことだ。
幾つかのコンピューター、メモリ、あるいは高速なネットワーク接続の追加をすることで、問題を取り除ける。
既存のハードウェアをアップグレードすることは、投資とほんのちょっとした努力を要するが、対処としては最も容易で最善の選択である。
あるテレコムのプロダクトのビルドはコンパイルにRAMディスクを利用することで、50パーセントの高速化ができた。
そしてそれはメモリを増設するだけですんだのだ。

Parallelize –related to adding hardware is to parallelize and distribute the build.
It often requires redesigning the build scripts, changing tools, or even building new tools.
Therefore, more effort is needed compared with just adding new hardware.
A large telecom product speeded up their build by building every component on a separate computer.

**並列化** - ハードウェアの増設と関連することに、ビルドの並列化と分散化がある。
それはたいてい、ビルドスクリプトの再設計、ツールの変更、あるいは新しいツールのビルドなどが必要となる。
それゆえ、ハードウェアを増設するよりも多くのやるべきことがある。
大きなテレコムプロダクトは全てのコンポーネントを別々のコンピューターでビルドすることで、ビルドの高速化ができた。

Change tools –upgrading tools to the latest version or replacing a slow tool with a fast one speeds up the build a lot.
Simply by switching compilers we once made a 50 percent improvement in compile time.
The most common problematic, slow tool we see used is IBM Rational ClearCase.
Every time a product group switched from ClearCase to Subversion–a good free open-source SCM system–they… First, speeded up the build (our clients have seen 25%-50% improvement); Second, saved the company significant money by eliminating licenses; And third, improved the lives of the developers, since ClearCase is often the most hated development tool in the groups we work with.
Some misinformed people incorrectly argue that Subversion is not suitable for large-product development.
But we have seen it used successfully in product groups with four hundred people located at multiple sites around the globe.
Ironically, the so-called large-scale features of ClearCase, such as multisite support, make real CI impossible because they force code ownership.

**ツールの変更** - ツールを最新版にアップグレードするか遅いツールを早いものに置き換えるかすることで、ビルドの高速化をはかれる。
単純にコンパイラを変えることで、筆者らはコンパイル時間を50パーセント改善した。
非常によくある厄介事だが、筆者らが見た遅いツールというのはIBMのRational ClearCaseだ。
プロダクトグループの全ての時間に関して、ClearCaseから（よく出来たオープンソースのフリーなSCMシステムである）Subversionに変えたら。。。
第一に、（筆者らの顧客の25%から50%の環境で）ビルド時間が短くなった。
第二に、ライセンスを除外することで企業の大事なお金の出費を抑えられた。
そして第三に、開発者の生活常用が改善した。
それ以来、筆者らが仕事をしているグループでは、ClearCaseは最も嫌がられるツールである。
何人かの勘違いを人たちが、Subversionは大規模なプロダクト開発には向かないと、誤ったことを伝えている。
しかし、筆者らは400人もの人びとと世界中の幾つかの場所からなるプロダクトのグループでうまく使っているのを見たことがある。
皮肉なことに、ClearCaseのマルチサイトサポートといった、いわゆる大規模向けなフィーチャーは、コードのオーナーシップを共用するので、真のCIを不可能にしてしまっているのだ。

Build incrementally –you only need to compile changed components and run related tests.
Easy in theory; hard in practice.
Dependencies between components, changes in interfaces, or incompatible binaries are some of the things that make compiling only the change a difficult proposition.
For the same reasons, finding all tests related to the changed component can be difficult.
Incremental builds are rarely 100 percent reliable, and to prevent corruption of the incremental build, it’s a good idea to also keep a clean daily build.

**増分ビルド** - 変更のあったコンポーネントをコンパイルして、関連するテストを実行する必要があるだけだ。
理論はやさしいが、実践は難しい。
コンポーネントの遺贈関係、インターフェイスの変更、あるいは互換性のないバイナリーは、変更した部分だけをコンパイルするのを難しいものとしてしまう。
同じ理由で、コンポーネントの変更に関わる全てのテストを検出することも難しくなる。
増分ビルドが100パーセント確かなものとなることはあまりないので、増分ビルドの腐敗を避けるのに、日次でのクリーンビルド実行もいい考えだ。

Deploy incrementally –on large embedded products, it can take a long time to deploy or install software; a radio network’s telecom product we worked with took more than an hour to deploy.
This is not unusual.
Testing speeds up when the deployment is done incrementally–only the changed components are deployed.
The changes need to be loaded, and this can be done by rebooting the system.
However, starting a large system is time consuming, and therefore some systems are upgraded dynamically–an important feature in telecom and other industries where downtime is very expensive.
Incremental deployment–especially dynamic upgrading–requires changes to the system, making this option difficult.

**増分デプロイ** - 大規模の埋め込みプロダクトでは、ソフトウェアのデプロイやインストールは長い時間を要する。
ラジオ放送網のテレコムプロダクトで働いていた時は、デプロイに1時間以上費やしていた。
これは異常なことではない。
テストは（変更のあったコンポーネントだけの）増分デプロイがなされると早くなる。
変更はロードされる必要があり、それはシステムのリブートによりなされる。
しかしながら、大規模なシステムの起動は時間がかかるので、幾つかのシステムは動的にアップグレードがなされる。
テレコムや、停止時間が非常に高価なである他業種での重要なフィーチャーなどだ。
（特に動的アップグレードだが）増分デプロイはシステムの変更を要することが、この選択肢を困難なものとしている。

Manage dependencies –unmanaged dependencies are a common reason for slow builds.
Examples: Header files including many other header files, or multiple link cycles to resolve cyclic link dependencies.
For a multimedia product, we spent several hours on re-ordering link dependencies–cutting link time in half.
Reducing dependencies speeds up your build and, as a side effect, improves the structure of your product.

**依存性の管理** - 依存性を管理していないことが、ビルドが遅いことのよくある原因だ。
例えば、たくさんのヘッダーファイルをインクルードしたヘッダーファイルや、循環参照を解決するための複数のリンクサイクルだ。
マルチメディアプロダクトで、筆者らはリンクの依存性の順番替えに数時間を費やして、リンクする時間を半分にしたこともある。
依存性を減らすことはビルドを高速化するが、副次的な効果として、プロダクトの構造の改善にも繋がる。

> Note a key insight
> Improving the build improves the structure of your product.
Why? Because bad structure becomes painfully visible when you try to shorten the cycle time of the build.

> This is a lean insight discussed before: A powerful side effect of shorter cycle times is the need to dramatically improve the processes and the product to support short cycles and small batches.

> 洞察メモ
> ビルドの改善がプロダクトの構造を改善する。
なぜかって？
良くない構造はビルドのサイクルタイムを短くしようとした時に、苦行に見えるようになってしまうからだ。

> リーンでの洞察で前に述べたことだ。
サイクルタイムを短くする強力な副次的な効果は、短いサイクルとスモールバッチを支援するために、プロセスとプロダクトの劇的な改善を必要とすることだ。

Refactor tests –unfortunately, many developers care less about test code than production code.
The result? Badly structured test code and slow tests.
We once spent only half a day refactoring tests–and speeded up the build by 60 percent! By profiling and refactoring tests you can frequently make these kinds of quick gains.

**テストのりファクター** - 不幸なことに、多くの開発者はプロダクトコードほどテストコードに気を配らない。
結果は？
良くない構造のテストコードと遅いテストだ。
筆者らはかつてテストのリファクタリングにたった半日費やしただけで、60％もビルドが早くなったことがある。
テストを調べてリファクタリングすることで、頻繁にこの手の素早い結果を出せる。

A multi-stage CI system splits the build and executes it in different feedback cycles.
At the lowest level, it has a very fast CI build containing unit tests and some functional tests.
When this CI build succeeds, it triggers a higher-level build, containing slower system-level tests.
Larger products have more stages.

マルチステージのCIskステムはビルドを分割し、それらを異なったフィードバックサイクルで実行する。
最も低いレベルでは、単体テストといくつかの機能テストを含んだ非常に高速なCIビルドを持つ。
このCIビルドが成功すると、遅いシステムレベルのテストを含んだ高いレベルのビルドが始まる。
大きなプロダクトではステージがもっとある。

A CI system is comparable to the “stop the line” culture at Toyota.
When a defect is detected, Toyota stops the line, and the first priority is to fix the defect and its root cause.
Isn’t a multi-stage CI system hiding defects and against this lean principle? No.
A stop-the-line attitude is absolutely needed, but this does not mean that you should blindly stop all the work.
Even Toyota does not do that [LM06a].

CIシステムはトヨタの「ラインを止める」文化に例えられる。
欠陥が見つかると、トヨタはラインを止め、そして最優先として行うことは、欠陥を直しその根本原因を突き止めることだ。
マルチステージのCIシステムは欠陥を隠し、これがリーンの原則に反してやいないかだって？
反してはいない。
ラインを停めるという態度は本当に必要だが、盲目的に全てを止めるということを意味してないのだ。
トヨタでさえそうしてない。

> Toyota has developed a system that allows problems to be identified and elevated without necessarily stopping the line.
When a problem is identified and the cord is pulled, the alarm sounds and a yellow light is turned on.
The line will continue to move until the end of work zone–the “fixed position stop” point… the line will stop when the fixed position is reached and the andon will turn red.

> トヨタは、ラインを止めることなく問題を特定し浮上させるようなシステムを開発した。
問題が特定され紐が引かれると、渓谷がなり黄色いランプが点灯する。
ラインは作業エリアの最後、定位置停止と呼ばれるところまでは動き続ける。
ラインが止まるのは定位置停止に到達したときで、そこでアンドンが赤く点灯する。

A multi-stage CI system works the same way.
You identify the problem early and act on it, but you do not want it to affect everyone.
Only if the problem turns out to be really serious do you “stop the line.”

マルチステージのCIも同様に働く。
問題を早く見つけ、そこに働きかけるが、みんなに影響を与えたくはないだろう。
問題が本当に深刻になった場合にだけ、「ラインを止める」のだ。

When building a multi-stage CI system, consider

マルチステージのCIシステムを構築するときは、以下のことを考慮する。

* a developer build
* component or feature focus
* automatic or manual promotion
* event or time triggers
* the number of stages

* 開発者ビルド
* コンポーネントかフィーチャーかにフォーカス
* 自働か手動かのプロモーション
* イベントか時間かで実行
* ステージの数

A developer build –developers practicing CI need to verify their changes before checking in.
Therefore, they must be able to work with a subset of the system, often a component, and be able to run unit tests for it.
Take this into account when automating your build.

**開発者ビルド** - 開発者のCIの実践はチェックイン前に彼らの変更の検証が必要だ。
なので、彼らはコンポーネントなどといったシステムのサブセットで作業でき、その単体テストを実行できる必要がある。
ビルドを自動化するときには考慮しよう。

Component or feature focus –a traditional multi-stage CI system is structured around components.
The lowest level builds one component, the next level a subsystem, and the highest level builds the whole product.
With teams organized around components, the team takes care of “their” CI system [AKB04 (originally at: http://www.cmcrossroads.com/articles/agilemar04.pdf)].
But where to include higher-level acceptance tests, and what about feature teams? An alternative is to structure your CI system around features.
When someone checks in code, all the related feature-CI systems are triggered.
Tests are now run in parallel, but the same component is compiled multiple times.

**コンポーネントかフィーチャーかにフォーカス** - 伝統的なマルチステージのCIシステムはコンポーネントを中心に構築されている。
低いレベルでは一つのコンポーネントをビルドし、次のレベルではサブシステム、更に高いレベルでは全てのプロダクトをビルドする。
コンポーネントを中心に組織化されたチームでは、チームは「自分たちの」Ciシステムの面倒を見る。
しかし高いレベルの受け入れテストを含むところで、フィーチャーチームはどうなんだろう？
代替案はCIシステムをフィーチャー中心に構築することだ。
誰かがコードをチェックインすると、全ての関連するフィーチャーのCIシステムが実行される。
テストは並列で実行されるが、同じコンポーネントは複数回コンパイルされる。

One distributed product group we worked with mixes the two approaches.
On a lower level, the CI system is organized around components, and the output of this triggers multiple-feature CI systems running higher-level acceptance tests in parallel.

2つのことなるアプローチをミックスしていた、とある分散したプロダクトグループで働いていた。
低いレベルではCIシステムはコンポーネント中心に組織化され、これの成果物により並列に高いレベルの受け入れテストを実行する複数のフィーチャーCIシステムが動いていた。

Automatic or manual promotion –letting all stages of a CI system listen to the mainline creates a mess.
When a developer makes a mistake, all the stages fail.
A higher-level CI system needs to be triggered by an announcement that the component can be used.
Such announcement is called a promotion and is done by labeling (or tagging) the component.
Promoting a component can be done automatically or manually [Poole08].
With automatic promotion the lower-level CI system promotes a component after it passed.
Avoid manual promotion whereby the team decides when the component is “good enough” and promotes it.

**自動か手動かのプロモーション** - CIシステムの全ステージはメインラインの混乱をリスンする。
開発者がミスを犯した時、全てのステージが失敗する。
高いレベルのCIシステムはコンポーネントが利用可能だというアナウンスによってトリガーされる必要がある。
このようなアナウンスはプロモーションと呼ばれ、コンポーネントのラベリング（あるいはタギング）によって完了する。
コンポーネントをプロモートするのは自動でも手動でもできる。
低いレベルのCIシステムの自動プロモーションは、コンポーネントがパスしたことをプロモートする。
手動でのプロモーションによって、コンポーネントが「いいぐあい」であることを判断し、プロモートするようなことはやめよう。

Event or time triggers –every CI system is triggered by either an event or by time.
The low-level CI systems are always triggered by an event–a code check-in.
For higher-level CI systems, the trigger is either the promotion of a component or time.
A trigger by promotion is faster, but for slow builds it is not worth the extra effort in configuration and maintenance.
A higher-level daily build might be good enough [Vodde08].
For example, one distributed product group we worked with had low-level, code-triggered CI systems, a higher-level promotion-triggered CI system, and a daily build running tests that lasted over eight hours.

**イベントか時間かで実行** - 全てのCIシステムはイベントか時間かによってトリガーされる。
低いレベルのCIシステムはコードのチェックインといったイベントによって常にトリガーされる。
高いレベルのCIシステムでは、トリガーはコンポーネントのプロモーションか時間になる。
プロモーションによるトリガーは早いが、ビルドが遅いところでは構成やメンテナンスの余計な努力をする価値はない。
高いレベルではデイリービルドで十分かもしれない。
例えば、とある分散したプロダクトグループで働いてた時、低いレベルではコードによってトリガーされるCIシステムがあり、高いレベルではプロモーションによってトリガーされるCIシステムがあった。
そして、テストを実行するのに8時間を超えるデイリービルドが実行されていた。

The number of stages –the size and ‘legacy-ness’ of the product determine how many levels of CI systems are needed.
Common stages are

**ステージの数** - プロダクトのサイズと「レガシーさ」がどれだけの数のCIシステムのレベルが必要かを決める。
一般的なステージは次の通り。

* fast component-level –a very fast low-level CI system for quick feedback.
It runs unit tests, code coverage, static analysis, and complexity measurements.
* slow component-level –a slower low-level CI system.
It runs integration or slow component-level tests.
* product stability-level –a very fast product-level CI system for quick feedback on the basic product stability.
It runs fast functional tests (smoke tests) .
* feature-level –a slower high-level CI system.
It runs functional and acceptance tests.
* system-level –a slow high-level CI system.
It runs system-level tests, which often take hours.
* stability-performance-level –a very slow high-level CI system.
It continuously runs stability and performance tests, which often take days, if not weeks.


- 早いコンポーネントのレベル - フィードバックの早い高速な低いレベルのCIシステム。
単体テストを実行し、カバレッジを取り、静的解析をし、複雑度を計測する。
- 遅いコンポーネントのレベル - 遅い低いレベルのCIシステム。
結合テストか遅いコンポーネントレベルのテストを実行する。
- プロダクトの安定性レベル - 基礎となるプロダクトの安定性に対するフィードバックの早い高速なプロダクトレベルのCIシステム。
速い機能テスト（スモークテスト）を実行する。
- フィーチャーレベル - より遅くて高いレベルのCIシステム。
機能テストと受け入れテストを実行する。
- システムレベル - 遅くて高いレベルのCIシステム。
たいてい数時間は掛かるシステムレベルのテストを実行する。
- パフォーマンスの安定性レベル - 非常に遅くて高いレベルのCIシステム。
安定性とパフォーマンスのテストを数日から場合によっては数週間かけて実行し続ける。

We have yet to see all stages in one product.
Most products select stages most important for them and add more stages only when needed.
An unnecessarily complex CI system is a waste.

筆者らは一つのプロダクトに全てのステージがあるのを見たことがない。
殆どのプロダクトはこの中から重要なものを選び、必要になった時だけ追加する。
不必要に複雑なCIシステムはムダだ。

### Example Staged-CI System

See scaled CI system.
shows an example staged-CI system.
In this example, every component has a CI system executing unit tests, plus static analysis and code coverage metrics.
A successful build promotes the component and triggers feature-level CI systems executing higher-level tests.
A daily build executes system-level tests such as performance tests.

ステージにわかれたCIシステムの事例で、スケールしたCIシステムを見てみよう。
この事例では、全てのコンポーネントは単体テストに加え、静的解析やコードカバレッジといったメトリクス取得を実行するCIシステムを持つ。
ビルドが成功するとコンポーネントがプロモートされ、高いレベルのテストを実行するフィーチャーレベルのCIシステムをトリガーする。
デイリービルドはパフォーマンステストといったシステムレベルのテストを実行する。

<img src="http://less.works/img/technical-excellence/xcontinuous-integration-scaled-system-example.png.pagespeed.ic.FnY9-Dpf1k.png" alt="continunous-integration-scaled-system-example.png" pagespeed_url_hash="1603173634" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

A CI system can effectively include visual management–a lean principle.
When the build breaks, a visual signal indicates failure–an andon system (Toyota terminology).
The intent is not for managers to punish the developer who broke the build; it is for developers to see the status of the build.
What would they do with this information? Investigate what is going on or delay their integration when the build fails.
If, after some time, the visual signal still indicates failure, more people may explore why it is not fixed.

CIシステムはリーンの原則である見える化を効果的に含められる。
ビルドが壊れたら、トヨタで言うところのアンドンで見える化できる。
意図としてはマネージャーがビルドを壊した開発者を罰するためのものということではない。
開発者がビルドの状態を見るためのものなのだ。
この情報で彼らは何をするんだろう？
ビルドが失敗すると、何が起こっているのかを調査するか、あるいは統合を遅らせる。
もしいくらか時間が経ったあとでまだアンドンが失敗を示しているなら、多くの人がなぜ解決できないのかを模索するだろう。

A popular early visual tool to plug into a CI system was a lava lamp.
A green bubbling lava lamp indicated a passing build.
But when the build failed, a red lava lamp started bubbling.

CIシステムに最初に取り入れられる見える化ツールはラバランプだった。
緑の泡のラバランプはビルドが通ったことを表す。
しかし、ビルドが壊れると、赤のラバランプが泡立ちはじめる。

After lava lamps, people started attaching all kinds of displays to the build, such as Christmas lights, sirens, and moving skeletons that screamed when the build broke.
Though less entertaining, a simple monitor showing a Web page of a large red or green color blob (a red-green screen ) is more easily reproducible.
Red-green screens seem to have become ubiquitous in large-scale CI.
Some versions include a yellow signal to indicate “the broken build is now being fixed.” The simple large color blob–visible from a distance–is the key element, but the display can also add text or chart data, such as build duration or test coverage.
The information does not need to be limited to build information [Rogers08].

ラバランプのあとは、クリスマスライトやサイレンやビルドが失敗した時に叫ぶ動く骸骨といったものを使いはじめる。
あまり面白くないが、単純に大きな赤か緑のウェブページを見せるだけのモニターは、より感嘆に真似できる。
赤と緑の画面は大規模CIにおいてはユビキタス言語になってきているように見える。
別のところでは、ビルドが治ったのを表すのに黄色を使うのもある。
単純な大きな色の塊はは遠くから見ることもでき、重要な要素ではあるが、ビルド時間やテストのカバレッジといった文字列や表データをディスプレイに表示できる。
情報はビルドの情報に限定する必要もない。

<img class="rounded shadowed" src="http://less.works/img/technical-excellence/xcontinuous-integration-andon-skeleton.jpg.pagespeed.ic.PuB-qPPam_.webp" alt="andon-skeleton.jpg" pagespeed_url_hash="1570946843" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

<img class="rounded shadowed" src="http://less.works/img/technical-excellence/xcontinuous-integration-andon-red-green.jpg.pagespeed.ic.5N9GjbchL1.webp" alt="andon-red-green.jpg" pagespeed_url_hash="543269719" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

One warning related to visual management, well stated by Jeffrey Liker [LH08]:

見える化に関する忠告はジェフリーライカーがうまく述べている。

> Just because there is visual presentation does not mean there is visual management.
It is relatively easy to set up nice display areas that are for show.
The challenging part is making them “for go.” Many people who visit Toyota openly voice the difference of their approach.
We often hear comments such as “Now I see, the things that Toyota displays are actually driving action on a daily basis.” This is indeed the difference, and Toyota would suggest that if it is not driving daily action, get rid of it.

> 単に見えるものがあれば、見える化できているというわけではない。
見せるためのいい感じのディスプレイエリアを用意するのは比較的簡単だ。
頑張りどころはそれらを「なしですませる」ことだ。
トヨタを訪れる多くの人が彼らのアプローチとの違いを口にする。
「やっとわかったのは、トヨタが示していることは、日常的に実際に運転するさいの行動だ」というコメントをよくきく。
これは実際に違っていて、もし運転するときの日々の行動ではなければ取り除く、ということをトヨタが示唆しているのだ。

On large products it is even harder to split large changes into small ones.
Developers sometimes want to restructure or re-architect their legacy system and are convinced that it must be done in one large change.
But we have yet to see a large refactoring that could not be done gradually.
Every time, after discussion with the developers, we found ways of splitting the must-be-done-at-once large refactoring [RL06].

大きなプロダクトでは大きな変更を小さく分けるのですら難しい。
開発者は時々レガシーシステムを再構築や再設計したがり、大きな変更ではそうすべきだと確信を持つ。
しかし、我々は徐々にはできない大きなリファクタリングをまだ見たことがない。
開発者と議論した後、毎回「一度に実施されるべき大きなリファクタリング」を分割する方法を見つけている。

Interface changes are a common problem in large systems.
Many components use the interface and need to be changed–making it impossible to do gradually, right? Not so.
In fact, an interface change in APIs is common, and there is a well-known solution:

インターフェイスの変更は大きなシステムではよくある問題だ。
そのインターフェイスを使っている多くのコンポーネントが修正される必要がある。
それを徐々にすることは不可能だって？ほんとに？
違うでしょ。
実際には、APIのインターフェイスの変更はよくあることなので、よく知られた解決策もある。

Every step can be done independently and at different times.
For public APIs, it is impossible to find out if there are still users of the old interface.
This makes removing the old interface difficult.
But most interfaces are not part of a published API, so do not forget to remove the obsolete one.
We have seen many products with three or four file system interfaces or logging interfaces because the old ones were never removed.

全てのステップは依存せずに別々の時間で実施できる。
パブリックなAPIでは、古いインターフェイスを使ってるユーザーがいるなら、不可能に見える。
これが古いインターフェイスを取り除くことを難しくしている。
しかし多くのインターフェイスは公開されたAPIの部分にあるわけではないので、使われないものを消すのを忘れないように。
筆者らは、古いものが全く削除されずに、3つか4つのファイルシステムやロギングのインターフェイスをもつ多くのプロダクトを見た。

### Do’s and Don’ts

The previous section alluded to CI do’s and don’ts:

これまでの節でCIでやることとやらないことをそれとなく示してきた。

DO commit and integrate every TDD cycle (e.g., every 5 or 10 minutes)—And as hands-on developers ourselves we know that speed is easy with new code, but hard with messy legacy code.

**（5か10分の）全てのTDDサイクルでコミットして統合すべし** - 実践する開発者としては、新しいコードではそのスピード感は簡単に達成できるが、乱雑なレガシーコードでは難しいことを知っている。

Do NOT develop on branches—If using a distributed tool such as Git, push to the common ‘master’ every TDD cycle.

**ブランチで開発すべからず** - Gitのような分散ツールを使っていても、すべてのTDDサイクルでmasterにpushすべし。

Do NOT have a policy to review code before commit—If you do that, you will have long-delayed integration creating other big quality problems and many hidden issues! Instead…

**コミット前のコードレビューのポリシーを持つべからず** - もしそうしてるなら、他の大きな品質問題と多くの見えない問題を生み出す、統合の長期遅延を招くだろう。その代わりに。。。

DO build quality in to the code to support optimistic integration— How to move from a pessimistic policy of delayed integration after a code review to an optimistic policy of early integration?2 Create a culture of software craftsmanship, TDD and refactoring for clean code, pair or mob programming to review-while-coding, and automated code- checking tools.
And if code reviews are still desired, do them on a slower cycle of small batches of already-checked-in code.

**楽観的な統合をサポートするためにコードに品質を埋め込むべし** - コードレビュー後の遅い統合という悲観的なポリシーから、どのようにして早い統合の楽観的なポリシーに移行できるのだろうか？
ソフトウェア職人の文化を作り、クリーンコードのためのTDDとリファクタリングを行い、コード時にレビューするペアやモブプログラミングを行い、コードをチェックするツールを自動化しよう。
それでもコードのレビューが望まれるなら、チェックイン済みコードのスモールバッチの遅いサイクルで行おう。

Do NOT have a “don’t break the build” policy; and do NOT have blaming and shaming when it breaks—if you do that, it will create fear and avoidance of integration.
Then once again, long-delayed integration with many hidden problems.
Instead…

**「ビルドを壊すべからず」というポリシーとそれを壊した時に非難して恥をかかせるようなことはやるべからず** - もしそれをやってしまうと、統合に対して恐れを抱き、避けるようになってしまうだろう。
そしてもう一度、多くの問題が隠蔽された長く遅延した統合になってしまう。
その代わりに。。。

DO make it is easy to fail fast, stop & fix, and learn from ‘mistakes’— Create a lighting-fast CI system that gives rapid feedback when the build breaks.
Eliminate the barriers that inhibit people from practicing stop and fix.
Create an environment of personal safety where people can admit problems and learn to improve.

**早く失敗し、直し、「誤り」を学ぶことが簡単になるようにすべし** - ビルドが壊れた時に素早いフィードバックをくれる光速のCIシステムを構築しよう。
人びとが手を止めて直すことを実践するのを抑制するような、バリアを取り除こう。
問題を受け入れられて改善を学べるような、安全な環境を作ろう。

DO “stop and fix” when the build breaks—“We’re too busy dealing with problems to fix our broken build.” Need to spell it out? Didn’t think so.

**ビルドが壊れたら「手を止めて直す」べし** - 「壊れたビルドを直すにも対処する問題で手一杯なんです。」
まだ説明する必要があるのか？
そうは思わないが。

DO use visual management showing the state of the build—Install old and unloved computers and monitors ‘everywhere’ to show build state.

**ビルドの状態を見える化すべし** - 古くて使われてないコンピューターとモニターでビルドの状態を「どこでも」見えるようにしよう。

### Use Feature Toggles

As with continuous integration, feature toggle are often (unfortunately) not seen as a mechanism to support coordination and integration.

継続的インテグレーションで、フィーチャートグルは（残念なことに）連携と統合をサポートするメカニズムだとみなされることはほとんどない。

A frequent large-group integration-coordination problem is that some teams have added features that are immediately ready for use, and other teams have added features that aren’t ready for prime time and shouldn’t be made visible.
This is usually because they aren’t feature-rich enough to be minimally useful.
Rather than delay integration by working on a separate branch or not checking in the code, what to do?

大きなグループの統合と連携のよくある問題は、幾つかのチームはすぐに利用できるフィーチャーを追加し、別のチームはゴールデンタイムで準備はできてなく、見えているひつようもないフィーチャーを追加する場合だ。
これはたいてい、それらが十分小さくて有用なフィーチャーリッチなものではないことによる。
分割したブランチで作業して、コードをチェックインせずに統合を遅らせる以上に何ができるんだろう？

Use feature toggles that expose or hide features based on configuration settings, while still integrating continuously across all developers and teams.
And for scaling use a free open-source tool such as Togglz.

すべての開発者とチームをとうして継続的に統合している間は、構成の設定でフィーチャーを晒したり隠したりする**フィーチャートグル**を使おう。
そしてスケールするにはTogglzといったフリーのオープンソースツールを使おう。

At the simplest level, a feature toggle is just a conditional statement around code.
So why a special tool? What makes tools such as Togglz useful in a scaling context are the administrative features they provide for toggle management of many features in different deployments, such as production versus sandbox.

単純なレベルでは、フィーチャーとグルはコードでの条件文だ。
なんで特別なツールを？
スケーリングのコンテキストでTogglzのようなツールのもたらす利点は、プロダクションとサンドボックスのような異なった成果物での、多くのフィーチャーのトグルマネジメントを提供している管理用フィーチャーであることだ。

### Conclusion

How to start? Using CI requires

どうやってはじめる？
CIを使うにあたって必要なのはこれらだ。

* changing developer behavior
* setting up a CI system

* 開発者の振る舞いを変える
* CIシステムを構築する

Changing developer behavior –Because large products have many people, this is the hardest task.
Focus on TDD–a great way of splitting a large change into smaller ones.
Using TDD coaches, who pair-program to teach, is an efficient way of learning TDD.
But be patient.
TDD is a hard change for most developers and learning takes time.

**開発者の振る舞いを変える** - 大きなプロダクトは人が多いので、これは大変な作業だ。
大きな変更を小さな単位に分割する素晴らしい手法、TDDにフォーカスを当てよう。
ペアプロを教えるTDDのコーチを使うのは、TDDを学ぶのに効果的だ。
しかし、忍耐強くあること。
TDDは多くの開発者にとっては変わるのが難しく、学びには時間がかかる。

Setting up a CI system –Most products we worked with set up a separate project for building a CI system.
This works, though a better alternative is to add the work to the Product Backlog and let an existing feature team work on it.
This creates more visibility and a sense of ownership–the developers are also users.

**CIシステムを構築する** - 筆者らが働いてきたほとんどプロダクトでは、分離したプロジェクトごとにCIシステムを構築した。
これは機能したが、より良い代替案はプロダクトバックログに作業を加え、既存のフィーチャーチームにそれを実施させることだ。
これはより見える化と、開発者が同時にユーザーでもあるというオーナーシップの感性を生み出す。

Most problems implementing CI are organizational and not technical.
In many products we worked with, CI became an organizational mess.
It involved many traditional functions and roles: developers, managers, testers, test automation engineers, ScrumMasters, agile coaches, SCM administrators, and the IT department.
The result was unclear responsibilities, blaming, and committees (aka “steering groups”) who were forever discussing without anybody doing real work.
The result? No progress.
If this happens, do not try to hide the organizational problems with technical solutions and do not give up because “our product is too complex for CI. ”

CIの実装でよくある問題は、組織的なものであって技術的なことではない。
筆者らが働いてきた多くのプロダクトでは、CIは組織的な混乱になった。
開発者、マネージャー、テスター、テスト自動化エンジニア、スクラムマスター、アジャイルコーチ、SCM管理者、IT部門といった多くの伝統的な職能とロールがあった。
そして、不透明な責任、非難、そして（関係者の集まる運営グループとして知られる）誰も本当の仕事をすることなく延々と議論している委員会となった。
結果は？
何も進まない。
もしこうなったら、技術的な解決策で組織の問題を隠すようなことはせず、「我々の製品はCIするには複雑なので」という理由で投げ出さないことだ。

Why not give up? Because every product group we have worked with who went through this “big rock removal” process toward CI has unequivocally found it immensely useful .

ギブアップしないって？
CIでのこの「大きな岩とり」のプロセスを切り抜けてきた、我々が関わってきた全てのプロダクトグループは、疑いの余地なく非常に効果があることを知ったからだ。

### Recommended Readings

Original texts related to CI:

* Extreme Programming Explained , by Kent Beck. The term CI was first coined in the Extreme Programming method.
* Continuous Integration , by Martin Fowler. Probably the best CI description available.

Recommendations related to automating builds:

* Managing Projects with GNU Make , by Robert Mecklenburg. When working with C/C++, you will probably use Make. This book provides a great overview of Make and also talks about Make in large-scale development.
* Ant in Action , by Steve Loughran and Erik Hatcher. When working with Java, you will probably use Ant. This book’s focus is Ant, but it covers other topics. Maven –another popular build automation tool–is also covered.
* Groovy in Action , by Dierk Koenig, Andrew Glover, Paul King, Guillaume Laforge, Jon Skreet. Groovy is a recent JVM-based dynamic programming language. It has some excellent build automation support.
* Pragmatic Project Automation: How to Build, Deploy and Monitor Java Apps , by Mike Clark. A small book that covers lots of technology related to automating Java builds.
* Continuous Integration: Improving Software Quality and Reducing Risk , by Paul Duvall, Steve Matyas, and Andrew Glover. The focus of this book is on the automation of builds more than on the practice of CI.

CI in large development:

* “Scaling Continuous Integration ,” by Owen Rogers (also at: exortech.com/blog/wp-content/uploads/2008/05/scaling-ci-3.pdf) in Extreme Programming and Agile Processes in Software Engineering 2004 Conference Proceedings.

### Notes
1. CruiseControl.NET is a CI system server for Microsoft .NET.
1. For Java, ten minutes is too long. For C++, about average. For C, probably too short. Ten minutes is an average language-independent TDD cycle.
1. To be more precise, avoid branches that live longer than ‘hours’. Branching has gotten easier with modern distributed version control systems such as Git and Mercurial. Some short use of short branches can be useful…but it is a sharp-knife tool that can easily be misused [Fowler09].
1. Tip: Create a release branch off the mainline just before release, not at the start of a release (a release line).
1. This was from a paper called Continuous Integration and Automated Builds at Enterprise Scale which used to be available at blog.aspiring-technology.com/file.axd?file=Continuous+Integration+at+Enterprise+Scale.pdf. Unfortunately, the link stopped working. If anyone has a new link to the document, let us know people.
