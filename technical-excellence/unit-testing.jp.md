---
layout: mechanics
title: Testing
order: 10
---

# Unit Testing

---

## What Is Unit Test?

---

Unit Tests are software programs written to exercise other software programs (called Code Under Test, or Production Code) with specific preconditions and verify the expected behaviours of the CUT.

ユニットテストは（CUTあるいはプロダクションコードと呼ばれる）他のソフトウェアプログラムを実行するために書かれたプログラムで、特定の前提条件のもとで期待されるCUTの振る舞いを評価するものだ。

Unit tests are usually written in the same programming language as their code under test.

ユニットテストはふつうCUTと同じプログラミング言語でかかれる。

Each unit test should be small and test only limited piece of code functionality. 
Test cases are often grouped into Test Groups or Test Suites.
There are many open source unit test frameworks. 
The popular ones usually follow an xUnit pattern invented by Kent Beck, for example, JUnit for Java and CppUTest for C/C++.

それぞれのユニットテストは小さくて、コードの限られただけをテストするべきだ。
テストケースはたいていテストグループやテストスイートでグループ化される。
たくさんのオープンソースのユニットテストフレームワークが存在する。
ポピュラーなものはケント・ベックによって発明されたxUnitパターンに従っており、例えば、JavaのためのJUnitやC/C++のためのCppUTestがある。

Unit tests should also run very fast. 
Usually, we expect to run hundreds of unit test cases within a few seconds.

ユニットテストは素早く実行できるべきでもある。
たいてい、数百ものユニットテストケースは数秒で終わるだろう。

---

## Why Unit Test

---

The purpose of unit testing is not for finding bugs. 
It’s a specification for the expected behaviours of the code under test. 
The code under test is the implementation for those expected behaviours. 
So unit test and the code under test are used to check the correctness of each other, and protect each other. 
Later when someone changed the code under test, and it changed the behaviour that is expected by the original author, the test will fail. 
If you code is covered by reasonable unit test, you can maintain the code without breaking the existing feature. 
That’s why Michael Feathers define legacy code as code without unit test.

ユニットテストの目的はバグを見つけることではない。
CUTの期待される振る舞いの仕様なのだ。
CUTは期待されている振る舞いの実装である。
なので、ユニットテストとCUTはお互いの正しさをチェックし、お互いを守る。
後に誰かがCUTを変更すると、もともとのコードを書いた人の期待する振る舞いとは変わってるので、テストは失敗する。
もしコードがほどよくユニットテストでカバーされているなら、既存のフィーチャーを破壊することなくコードを維持できるだろう。
なので、マイケル・フェザーズはユニットテストのないコードをレガシーコードと名付けた。

<img src="http://less.works/img/technical-excellence/xunit_test.png.pagespeed.ic.oiSjYH0HE8.webp" width="60%" data-pagespeed-url-hash="42144193" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

The purpose for unit testing is rather protect what we have implemented than to find any defects, just like the anchors set by a rock climber along his way up the rock. 
These anchors help him to protect what he has achieved.

ユニットテストの目的は、実装を守るというよりは欠陥を見つけるものであり、ロッククライマーが岩を登るのに打つ楔のようなものだ。
これらの楔は彼が成し遂げたいものを守る助けとなる。

### Purpose of Unit Test

The purpose of unit test can be summarized as:

ユニットテストの目的は次のようにまとめられる。

* Facilitates changes
    * It protects the behaviours decided by the previous programmers.
    So that people can change the code without breaking the existing features.

* 変更しやすくする
    * 前のプログラマの決定した振る舞いを守る。
    なので、既存のフィーチャーが壊れることなくコードを変更できる。

* Simplifies integration
    * Unit test tests the basic units of the program, the functions and the classes. 
    It makes sure the basic units are functioning as expected. 
    When these units are integrated together, we can separate the integration problems (the coupling problems) from the unit internal problems (the cohesion problems).

* 統合をシンプルにする
    * ユニットテストは関数やクラスといったプログラムの基本単位をテストする。
    基本単位が期待されている働きをすることを確かめる。
    これらの単位がひとつに統合されたとき、単体内での（凝集度の）問題から統合による（結合度の）問題を分離できる。

* Documentation
    * Well-written unit test can be used as documentation for the functionality of the code under test. 
    Unit test contains information typically you cannot find from the code under test, for example, the design purpose of the original programming who wrote the code, and how the code is expected to be used. 
    Unit test as documentation, unlike other traditional documentation, it doesn’t “lie”. 
    Because if it lies, the test would fail. 
    And that indicates either the test or the code is wrong.

* ドキュメント
    * うまく書かれたユニットテストはCUTの機能のドキュメントとしても使用できる。
    ユニットテストはCUTからはわからないもの、例えば、オリジナルのプログラミングを書いた人の設計の意図や、コードがどのように利用されることを期待されているのか、と言った情報を含んでいる。
    ドキュメントとしてのユニットテストは、旧来のドキュメントとは違い、「嘘」はつかない。
    嘘をついたとしたら、テストが失敗するだろう。
    そしてそれはテストかコードのどちらかが間違っていることを示すのだ。

* Design tool
    * Unit test is also an important design tool. 
    Unit test requires testability from the code understand. 
    Easy-to-test usually means easy-to-use. 
    So unit test could be used to make sure the design has consideration from the perspective of use, rather than only from the perspective of implementation. 
    Testable code needs better modularity and fewer dependencies. 
    So that the unit test can easily take a small part of the code under test (a “unit”) without taking care of the overwhelming amount of dependencies. 
    So unit test could be used to make sure the design has “high cohesion, low coupling”.

* 設計ツール
    * ユニットテストは重要な設計ツールでもある。
    ユニットテストはテスト容易性を求める。
    テストしやすさとはたいてい使いやすさでもある。
    なので、ユニットテストは、単に実装の観点からというよりは、利用する観点で考慮された設計であるかの確認に利用できる。
    テスト可能なコードは良いモジュラリティと低い依存性が求められる。
    そのため、ユニットテストは依存関係の数に埋もれることを気にかけることなく、CUTの小さな部分を扱うことができる。
    なので、ユニットテストは設計が「高凝集性と疎結合性」であることを確認できる。

### Why on “Unit” Level?

“Yes, it’s important to use automated test to protect the existing functionalities. 
But why does it need to be on the unit level?”

「うん、既存の機能を守るのに自動テストを使うのは重要だ。
しかし、なんで単体レベルが必要なんだい？」

You might wonder. 
Why don’t we just use thorough automated functional or system tests to protect the program?

不思議に思ったかもしれない。
プログラムを守るのに完全自動の機能テストあるいはシステムテストを使えばいいのに。

**Total cost of ownership – ** 
Unit test is based on the abstraction level of the programming language. 
It’s just some code exercising other code. 
It doesn’t need to run in the same environment as the production. 
For compiled programming language, it doesn’t even need to use the same compiler as the production. 
The creating and running cost of unit test is very low. 
If designed properly, the cost of maintaining is also very low. 
You may not get the same level of confidence from one successful unit test case as you can get from a functional test. 
You will need many small unit test cases to get approximately the same level of confidence. 
But the cost of these small unit test cases is still much lower than owning a few functional test cases.

**TCO（総保有コスト）- ** ユニットテストのTCOはプログラミング言語の抽象レベルに基づく。
別のコードをただ実行するだけのいくらかのコードなのだ。
プロダクションと同様の環境下で動作させる必要もない。
コンパイル言語の場合は、プロダクションと同じコンパイラである必要性すらない。
ユニットテストを書くことと実行することのコストは非常に低い。
ちゃんと設計されているなら、メンテナンスコストもまた非常に低くなる。
ユニットテストのケースが機能テストで得られる信頼度とは同じレベルにないと捉えてるかもしれない。
だいたい同じレベルの信頼度にはたくさんの小さなユニットテストが必要となるだろう。
しかし、これらの小さなユニットテストのケースのコストはほんの少しの機能テストケースよりもまだ低いものだ。

If a software code base hasn’t got any unit test for the past 2 years, there will be extra cost for applying unit test to this code base. 
The cost comes mostly from two sources:

もし、ソフトウェアのコードベースが2年もの間ユニットテストを含んでいなければ、このコードベースにユニットテストを適用するのに更なるコストがかかるだろう。
コストはたいてい2つのものがある。

1. The cost of applying a test framework to the code project. 
This is relatively easier for dynamic programming languages like Python, Ruby or Javascript. 
Usually, it’s also trivial for Java and C# project. 
It can be quite tricky for C/C++ project. 
No matter easy or hard, this is just one-time investment.

1. コードプロジェクトにテストフレームワークを適用するコスト。
Python、Ruby、Javascriptといった動的な言語の場合は比較的容易だ。
たいてい、JavaやC#のプロジェクトもまた些細なものである。
C/C++のプロジェクトでは、非常に扱いづらいものとなる。
簡単だろうが難しかろうが、これはたった一度の投資となる。

1. The existing code base is not testable. 
The code was designed without considering the testability. 
Applying unit test to this kind of code base often involves improving the current design. 
Doing so doesn’t only increase the cost of creating test, but also has potential cost of introducing new bugs by changing the design. 
So applying unit test to existing code base should be combined with other works that need the change from the code under test – when you have to change that piece of code regardless.

1. 既存のコードベースがテスト可能でない。
コードがテスト容易性を考慮されずに設計されている。
この種のコードベースへのユニットテストの適用は、現在の設計を改善することも含む。
そうすることはテストを作成するコストが増加するだけでなく、設計を変更することで新しいバグを埋め込んでしまう潜在コストも含む。
なので、既存のコードベースにユニットテストを適用するのは、CUTのコードの一部をなにがあっても変更する必要がある時のような、CUTの変更を要する他の作業と合わされるべきである。

**Internal Quality vs. External Quality – ** 
High level automated test like functional test and system test checks the external quality of the software. 
External quality means how well the software is functioning according to the requirement. 
Unit test is not as effective as the functional test in protecting the external quality. 
On the other hand, unit test ensures some of the internal qualities of the software. 
Internal quality here means the testability of the code and how well the code is protected. 
A testable design is in general a good design. 
Other levels of automated test cannot serve this purpose as well as unit test.

**内部品質と外部品質 - **
機能テストやシステムテストといった高レベルの自動テストは、ソフトウェアの外部品質をチェックする。
外部品質はソフトウェアが要求に従ってどのくらいよく機能しているかを意味する。
ユニットテストは、外部品質を保つのに機能テストほどの効果はない。
一方、ユニットテストはソフトウェアの内部品質をいくらか保証する。
内部品質とは、コードのテスト容易性や、コードがどのくらいよく保護されているかを意味する。
テスト可能な設計は一般的に良い設計とされる。
自動テストの他のレベルは、この目的においてはユニットテストと同等ではない。

**Quality of feedback -**
When you passed a functional test, you could be very confident about the functionality you just tested. 
But when you found it fail, usually you need to do some debugging to see what is wrong. 
Unit test might be able to give you more precise information about what is working and what is broken.

** フィードバックの品質 **
機能テストをパスした時、テストしたばかりの機能性に関してはかなり自信を持てるだろう。
しかし失敗した時には、たいてい何が間違っているのかを調べるのにいくらかデバッグをする必要がある。
ユニットテストは何が間違っているのか、何が壊れているのかに関するより正しい情報を与えてくれるだろう。

Unit test is on the abstraction level of the programming language. 
When running unit test, everything should happen just within the CPU and memory. 
And each test case should be small. 
Therefore, it should run very fast. 
Typically, you should be able to run hundreds of unit tests within a few seconds. 
Including the compiling or other preparation time, the whole process of running unit test should take less than 1 minute.

ユニットテストはプログラミング言語の抽象レベルにある。
ユニットテストを実行するとき、すべてのものはCPUとメモリの中で実行されるべきだ。
そしてそれぞれのテストケースは小さくあるべきだ。
それゆえ、非常に速い。
一般t系に、数百ものユニットテストは数秒内で実行できるべきだ。
コンパイルや他の準備時間を含み、ユニットテストを実行する全てのプロセスは1分以内であるべきだ。

Unit test should also be repeatable. 
If nothing changes, unit test runs should always return the same result.

ユニットテストはまた繰り返し可能であるべきだ。
何も変わってなければ、ユニットテストは毎回同じ結果であるべきなのだ。

If the unit test is very fast and repeatable, programmers can run it as often as they want, e.g. every a few minutes. 
The unit test will continuously provide quality feedback to the programmer. 
So that the programmer can go with a steady progress and focus on more important things rather than spending too much energy on trivial issues.

ユニットテストが非常に高速で繰り返し可能であれば、プログラマはやりたいときにいつでも、例えば数分毎といったタイミングで、実行できる。
ユニットテストはプログラマに品質のフィードバックを提供する。
プログラマが、確実に前進でき、些細な問題にかなりの労力を注ぐことなく、 より重要なものに注力できる。

<img src="http://less.works/img/technical-excellence/xtest_levels.png.pagespeed.ic.h6zJsjGNli.webp" width="50%" data-pagespeed-url-hash="696726064" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

A reasonable automated test structure should be like a pyramid. 
At the bottom are a lot of unit test cases. 
In the middle are much fewer integration level test cases. 
On the top, there are even fewer functional/system level tests.

適切な自動テストの構造というのはピラミッドのようなものである。
最下層にはたくさんのユニットテストケースがある。
中間にはそれよりは少ない統合レベルのテストケースがある。
そして頂上には、更に少ない数の機能／システムレベルのテストがある。

---

## Common Misconceptions of Unit Test

---

### Unit test is not as important as the production code

It is true that in the end, it’s production code that makes the product. 
But most software products have evolutionary life cycles. 
The code is not static. 
It changes over time. 
Code without unit test does not have the necessary protection when being changed. 
Unit test also contains important information that is not included in the production code.

結局のところプロダクションコードがプロダクトを作るというのは正しい。
しかし、ほとんどのソフトウェアプロダクトは進化的なライフサイクルを持つ。
コードは不変ではない。
変更は続くのだ。
ユニットテストのないコードは変更時に必要となる保護を持たない。
ユニットテストはまたプロダクションコードに含まれていない重要な情報を含んでいるのだ。

So unit test is just as important as the production code. 
They should be in the same SCM repository. 
They should follow the same coding standard as the production code.

なので、ユニットテストはプロダクションコードと同様に重要なものだ。
同じSCMリポジトリにあるべきだ。
そしてプロダクションコードと同様のコーディング規約に従うべきだ。

### Unit Test is done by testing engineers

The purpose of unit test is not for finding bugs. 
Technically, it checks rather than tests if the code under test has implemented the behaviour intended by the programmer who designed it. 
So the reasonable choice is just let the same programmer writes both the test and the code under test.

ユニットテストの目的はバグを見つけることではない。
技術的には、テストというよりは、CUTが設計したプログラマの意図した振る舞いの通りに実装されたかのチェックである。
なので、理想的な選択はテストとCUTは同じプログラマに書かせることだ。

It’s also encouraged to have two or more people pair up to do the programming together. 
They write the unit test and the code under test together. 
There are many fun ways of pair-programming. 
You may find more information in the Test-Driven Development section.

2名以上のペアで一緒にプログラミングをすることは励みにもなる。
一緒にテストもCUTも書く。
たくさんのペアプログラミングの楽しいやり方がある。
Test-Driven Development の章で多くの情報を見つけられるだろう。

### You can write unit test without changing the code under test

This is often not true. 
If the code doesn’t have good testability, you might still be able to write unit test for it technically. 
But the unit test written for non-testable code is usually very hard to maintain and understand. 
Therefore, it doesn’t make much sense to have it.

これはしばしば正しくない。
もしコードがそれほどテストしやすくないものであれば、技術的にはユニットテストことはまぁ可能だろう。
しかし、テスト可能でないコードのユニットテストは、たいてい保守するにも理解するにもとても困難なものだ。
それゆえ、そのままにしておくのは意味がないのだ。

The secret of unit test is not about writing test, but writing testable code under test. 
We want testable code and easy test, which is a win-win. 
We don’t want non-testable code and hard-to-maintain code, which is a lose-lose.

ユニットストの秘訣はテストを書くことではなく、テスト可能なCUTを書くことだ。
テスト可能なコードと容易なテスト、win-winのものがほしいのだ。
テスト可能でないコートと保守しづらいコード、lose-loseのものなどほしくない。

### I can add unit test later

Well, try asking the rock climbers to set their anchors later.

あぁ、それならロッククライマーに楔を後で打ってみるよう訪ねるといい。

<img src="http://less.works/img/technical-excellence/xunit_test.png.pagespeed.ic.oiSjYH0HE8.webp" width="40%" data-pagespeed-url-hash="42144193" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

---

## Good Unit Test Patterns

---

### No news is good news

If the test passes, it should just print OK (and perhaps some dots to show the progress). 
No other information.

テストが通ると、（おそらく進捗を表すいくつかのドットとともに）OKを出力するだけだ。
他の情報は何もいらない。

<img src="http://less.works/img/technical-excellence/500xNxunit_test_success.png.pagespeed.ic.WxBCqUtq9l.webp" width="500px" data-pagespeed-url-hash="1253239421" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

Rule of thumb:

おおざっぱには:

> No human intervention should be needed to get ready for the test, running the test cases or checking the result.

> テストの準備、テストケースの実行、あるいは結果の確認には人の関与は不要であるべきだ。

And when it fails, it should provide precise information. 
The goal is to limit the amount of time you spend on debugging when the test fails.

そして失敗した場合には、正しい情報を提供すべきだ。
目的はテストが失敗した時のデバッグに掛ける時間を制限することだ。

<img src="http://less.works/img/technical-excellence/342xNxunit_test_fail.png.pagespeed.ic.3_IivU-5nc.webp" width="342px" data-pagespeed-url-hash="1140092318" onload="pagespeed.CriticalImages.checkImageForCriticality(this);">

### Arrange, Act, Assert

A good pattern to follow in a unit test is “AAA”: Arrange, Act and Assert.

ユニットテストで従うべき良いパターンに「AAA」、Arrange - Act - Assertがある。

If you can easily find this pattern in each of your test cases, your tests should be easy to understand, and they should be fairly specific and to the point. 
One unit test case should test only one thing. 
Therefore, there should be only one set of AAA in one test case. 
A test case shouldn’t be very long (longer than 10 lines of code) if it follows the AAA pattern.

もしそれぞれのテストケースでこのパターンを簡単に見つけられるなら、テストは理解が簡単だし、それらはとても明確で的を得たものだ。
ひとつのユニットテストケースはたったひとつのことをテストすべきだ。
それゆえ、ひとつのテストケースには1セットのAAAがあるべきだ。
もしAAAパターンに従うなら、テストケースは（10行以上といった）とても長いものではいけない。

```
import unittest
class TestGroupForTextWrapping(unittest.TestCase):
    
    def test_should_have_no_wrapping_when_string_length_is_5_and_line_width_is_10(self):
        # Arrange:  Arrange all necessary preconditions and inputs. 
        wrapper = TextWrapper(width=10)
        
        # Act:  Act on the object or method under test. 
        wrapped = wrapper.wrap("a" * 5)
        
        # Assert:  Assert that the expected results have occurred. 
        self.assertEqual(["a" * 5], wrapped)
```

### Behaviour Driven Development (BDD) Style

Similar to the AAA pattern, the BDD style uses three other keywords to specify each test case: Given, When and Then. (You can also use And as another keyword.)

AAAパターンに似たもので、3つの別のキーワード、Given、When、Then（ともう一つのキーワードAnd）でそれぞれのテストケースを仕様化するBDDスタイルがある。


```
Given The Text Wrapper's Width Defined As 10
And Using '-' As Word Connector
When The Wrapper Wrap Text Length is Less Than 10
Then The Text Should Not Be Wrapped
```

As you can see, “given-when-then” maps to “arrange-act-assert” pretty well. 
They both simply define a state transition of a Finite State Machine (FSM). 
You can find more on this in the Uncle Bob’s article. 
Some differences:

見ての通り、「given-when-then」は「arrange-act-assert」に置き換えられる。
これらはどちらも単なる有限ステートマシンの状態遷移を定義している。
[Uncle Bobの記事](https://sites.google.com/site/unclebobconsultingllc/the-truth-about-bdd)で詳しく見ることができる。
いくらかの違いとしては:

* BDD is more “outside-in”, which means that it emphasises more the external behaviour

* BDDは、より外部の振る舞いを強調することを意味する、「アウトサイドイン」である。

* With BDD, you need to define a domain specific language to write your test specifications. 
Because of this, usually you’ll need a different framework. 
One example for Python is behave.

* BDDでは、テストの仕様を書くのにDSLを定義する必要がある。
このため、違ったフレームワークが必要となるだろう。
Pythonの例としてはbehaveだ。

### The Golden Rule Of a Unit Test

In general, a good rule for unit test case is:

一般的には、ユニットテストケースの良いルールはこれだ:

> Each unit test case should be very limited in scope.

> それぞれのユニットテストケースはスコープが非常に制限されているべき。

So that:

なので:

* When the test fails, no debugging is needed to locate the problem.

* テストが失敗した時、問題の特定にデバッグは不要である。

* Tests are stable because dependencies are simple.

* テストは依存関係がシンプルなので安定している。

* Less duplication, easier to maintain.

* 複製が少ないほど、保守も用意になる。

There is no secret to write good unit test. 
In order to write good unit test, you need to create easy-to-test design.

良いユニットテストを書く秘訣はない。
良いユニットテストを書くためには、テストしやすい設計にすることが必要なのだ。
