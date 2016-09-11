---
layout: mechanics
title: Test-Driven Development
order: 10
---

# Test-Driven Development

---

## What Is Test-Driven Development

---

Test-driven development is a development style that drives the design by tests developed in short cycles of:

テスト駆動開発は短いサイクルで開発されたテストで設計を駆動していく開発スタイルである。

1. Write one test.
1. Implement just enough code to make it pass.
1. Refactor the code so it is clean.

1. テストをひとつ書く。
1. テストをパスするのに十分なだけの実装をする。
1. リファクタリングでコードをクリーンにする。

<img src="http://less.works/img/technical-excellence/xtdd.png.pagespeed.ic.qLQv1lyRI1.webp" width="30%" data-pagespeed-url-hash="655410892" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

In a language such as Java, this cycle is as short as five minutes. 
In older languages, with slower compilation and less automated refactoring support, this cycle is longer—perhaps twenty minutes.

Javaのような言語であれば、このサイクルは５分程度の短いサイクルになる。
コンパイルが遅くて自動リファクタリングのサポートもあまりないような古い言語であれば、このサイクルは（おそらく２０分位と）長くなる。

Is test-driven development different in large product development? 
No. 
It is an individual developer practice and the number of people in the development does not matter.

大規模のプロダクト開発でテスト駆動開発は違ったものになるのか？
そうではない。
開発者個人のプラクティスであり、開発者数は問題ではない。

The amount of legacy code, old technology, and embedded development does have an impact on unit testing and test-driven development. 
Therefore, most experiments in this section are related to these.

レガシーコードの量、古い技術、組込み開発は単体テストとテスト駆動開発にインパクトを与える。
なので、この節のほとんどの手法は、これらと関連がある。

## A TDD cycle Should Be …

- Short
    - The turnaround time for passing each test is short. It could take 5 mins per cycle.
- Rhythmic
    - You’ll feel the rhythm distinctly - “red, green, refactor... red, green refactor...” <br/>
- Incremental
    - You’ll know that as you write and pass more tests, working functionalities are being build up incrementally.
- Design-focused
    - With good knowledge of software design principles, you’ll discover TDD is not a testing technique but a method of designing software.
- Disciplined
     - TDD is a different way of developing software. 
     To break the old habit of "code and fix" and to adopt a new habit will require discipline and persistence.


- 短い
    - 個々のテストをパスする所要時間は短い。
    １サイクル５分くらい。
- リズミカル
    - はっきりとしたリズムを感じるだろう。
    「レッド、グリーン、リファクタ−、、、レッド、グリーン、リファクタ−、、、」
- インクリメンタル
    - たくさんのテストを買いてパスすると、正しく働く機能がインクリメンタルに構築されていくのを知るだろう。
- 設計にフォーカス
    - ソフトウェア設計原則の良い知見で、TDDはテストのテクニックではなくソフトウェア設計手法であることがわかるだろう。
- 規律
    - TDDはソフトウェア開発の異なる手法である。
    「Code and Fix」の古い習慣を壊して新しい習慣に適用することは、規律と忍耐を要する。

---

## Why Tdd?

---

## Coaching TDD

---


### Use TDD Coaches

When a client of ours reviewed a draft of the companion book, he mentioned that we ought to stress coaching more. 
“One of our mistakes is that we didn’t provide enough coaching,” he said. 
Though we agreed with him, we pointed out that since we are both consultants and provide such coaching, this advice would not be very credible. 
We might as well add an experiment “Try…Hire us.” 
Thus, we minimized the advice related to hiring coaches.

筆者らの顧客がガイドブックの原稿をレビューしたところ、コーチングをより強調すべきだと言った。
「我々の過ちのひとつは十分なコーチングを提供しなかったことだ。」とのことだった。
彼に同意はするものの、我々は二人共コンサルタントでこのようなコーチングを提供しているので、このアドバイスはとても信じられるものではなかった。
我々は「試してから、、、我々を雇って」という試みを加えてもいいだろう。
これは、コーチを雇うことに関するアドバイスを最小限にした。

But related to test-driven development, we cannot stress strongly enough: 
Hire coaches! 
Adopting TDD means unlearning traditional programming and relearning how to design and code. 
We rarely meet people who were able to adopt this by self-education. 
Most developers need a coach to pair-program with them for days or weeks. 
The coach constantly reminds them to write the tests first and to really clean up the code—including the test code. 
He helps them apply TDD and refactoring to their real code.

しかしテスト駆動開発に関しては、コーチを雇おう！とはそれほど強く強調はできない。
TDDを適用することは伝統的なプログラミングを捨て去り、どのように設計してコードを書くかを改めて学ぶ事を意味する。
独学でこれを適用できた人には余りあったことがない。
殆どの開発者は数日や数週間ペアプログラミングするコーチが必要だ。
コーチはテストを始めに書き、テストコードを含めてコードを本当にきれいにすることを定期的に思い出させる。
彼は現実のコードにTDDとリファクタリングを適用するのを手助けする。

Test-driven development might be the hardest agile practice to adopt, but it is also one of the biggest opportunities for improving the quality of the design and code.
Hire coaches!

テスト駆動開発は最も適用の難しいアジャイルプラクティスだろうが、設計とコードの質を向上する大きな機会の一つでもある。
コーチを雇おう！

### Internal and external coaches

External coaches are needed when adopting TDD because the competence does not yet exist inside the company. 
But, over time, growing internal coaches reduces the dependence on externals and the cost of coaching.

TDDを適用する時には、企業内にはまだその能力がないので外部のコーチは必要だ。
しかし、時間とともに、内部のコーチが育ってきて、外部のコーチへの依存とコーチングのコストが減る。

That said, we have seen several attempts fail to develop internal coaches. 
Some reasons:

とはいうものの、内部コーチの育成に失敗したいくらかの試みを見た。

- No structure was in place to decide when and with which teams to work.
- No time was reserved for coaching. 
Instead the internal coaches were asked to do normal development.
- Developers were less eager to learn from internal coaches…you are never a prophet in your own land.
- Coaching skills were not appreciated and further developed. The result is that skilled internal coaches often leave to be an external coach.

- いつ決定するか、どのチームと働くかが整った構造がない。
- コーチングの時間が残されてない。
その代わりに内部コーチが普通の開発をするよう求められる。
- 開発者が内部コーチから学ぶことに余り熱心でない。。。自分の所有地で指導者には決してなれないということ。
- コーチングスキルが十分評価されておらず、さらに開発されてもいない。
その結果、スキルのある内部コーチは外部コーチに転職してしまう。

Choose both internal and external coaching. Depending on either of them alone is risky but combining them can lead to good results.

内部と外部のコーチを選ぼう。
いずれか片方のみに頼るのはリスキーだが、一緒にすると良い結果へと導いてくれるだろう。

---

## Test-driven development for a better architecture

---

TDD can help improve the architecture of a system. 
How?

TDDはシステムのアーキテクチャをより良くする。
どうやって？

When we are coaching, a frequent request is help for dealing with our client’s “inflexible architecture.” 
This most often boils down to problems in high coupling between components—a common problem in legacy code written without TDD because the original developer did not try to test the component in isolation.

我々がコーチングを行うとき、よく言われる要求はクライアントの「柔軟性のないアーキテクチャ」の扱いについての手助けだ。
これは結局のところ、もともとの開発者がコンポーネントを分離してテストを試してないので、TDDなしで書かれたレガシーコードのよくある問題、コンポーネント間の密結合にいきつく。

On the other hand, when a developer creates a new component (such as a class) with TDD, or refactors a legacy component to be unit-testable, they must break the dependencies of that component so that it is testable in isolation. 
That requires designing (or refactoring) for dependency injection and increased use of mechanisms for flexibility: interfaces, polymorphism, design patterns, dependency injection frameworks, function pointers, and more.

一方、開発者がTDDあるいは単体テスト可能なようにレガシーコンポーネントのリファクタリングを用いて、クラスといった新しいコンポーネントを作るとき、分離してテストできるようにコンポーネントの依存性を壊す必要がある。
依存性の注入と、（インターフェイス、ポリモーフィズム、デザインパターン、DIフレームワーク、関数ポインタ、などの）柔軟性のあるメカニズムの利用を増やしていく設計が求められる。

In this way, TDD encourages lower coupling and simple, flexible configuration—qualities of a good architecture.

このようにして、TDDは良いアーキテクチャの柔軟性を持った構成品質である、疎結合と単純さを促進する。
