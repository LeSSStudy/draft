---
layout: mechanics
title:  システム思考
order: 10
---

<!---
Systems Thinking
--->
## システム思考

<!---
I took a speed reading course and read “War and Peace” in twenty minutes. It involves Russia.
—Woody Allen
--->
私は速読のクラスを取り、『戦争と平和』を20分で読んだ。それにはロシアについて書いてあったと思う。  
ウッディ・アレン

<!---
“No matter what we do, the number of defects in our backlog remains about the same,” a manager told us;
this for a 15 MSLOC C and C++ product with several hundred developers where we were working.
What’s going on?
Systems thinking may help.
In small groups the forces at play are more quickly seen and informally understood, but in large product development—or any large system—it’s tough.
Gerry Weinberg highlights two decisive factors in this situation:
--->
「たとえ私達が何かしたとしても、バックログから発生する欠陥の数は変わらない」と、1,500万行(15 MSLOC)のCとC++の製品をつくる私達が数百人の開発者に対して、マネージャーは言った。  
何が起きたのだろう？  
システム思考ならそれがわかるかもしれない。  
小さな規模のグループでは、（バグの発生）要因がより迅速に見つかり、自然に理解もされているが、大規模開発－全ての大きなシステム－では、それが難しい。  
ゲイリーワインバーグはこの状況の2つの決定的な要因を強調する：

<!---
> Weinberg-Brooks’ Law:
> More software projects have gone awry from management’s taking action based on incorrect system models than for all other causes combined.
--->

> ワインバーグ-ブルックスの法則:  
> すべてを兼ね備えたの原因そのものより、間違ったシステムモデルに基礎を置いたマネジメントで行動する多くのソフトウェアプロジェクトはうまくいかない。

<!---
> Causation Fallacy:
> Every effect has a cause…
> and we can tell which is which. [Weinberg92]
--->

> 因果関係の間違った考え方：  
> すべての結果は原因を持っている…  
> だから、何がどのようになっているか分かるはず。[[ワインバーグ92]](http://www.amazon.com/Quality-Software-Management-Systems-Thinking/dp/0932633226/ref=sr_1_1?ie=UTF8&qid=1413527418&sr=8-1&keywords=Quality+Software+Management%3A+Systems+Thinking)

<!---
These reflect the impact of our mental models on the system, a subject that will be revisited later in this section.
--->

これらは、私達のシステム上におけるメンタルモデルの影響を反映しており、このセクションの後で再び取り上げる問題である。

<!---
Problems stemming from mental models and assumptions are one issue.
Another is that large-scale adoption of Scrum, lean thinking, and agile principles is not isolated to the development group.
It bumps into product management, budgeting, beta-testing, launch, and governance and HR policies.
Accordingly, in large-scale agile adoption it is useful to be able to get together with colleagues and effectively reason about the mental models, causal relations, feedback loops, and control mechanisms (or illusions of control) in a big system that is about to be seriously perturbed.
Systems thinking is one of those reasoning tools.
--->

メンタルモデルと仮定から生じる問題は、1つの論点になる。  
さらに、スクラム、リーン思考やアジャイルの原則の大規模な適用が、開発グループと切り離されてしまっている。  
それは、プロダクトマネジメント、予算化、ベータテスト、ローンチ、および管理と人的リソースの方針に行き着く。  
従って、大規模な環境でのアジャイルの採用には、メンタルモデル、因果関係、フィードバックループ、および本当に大きなシステムの中でのコントロールメカニズム（とか、コントロールの幻想）について、仲間達と集まり、効果的に論じることができることが有益である。  
システム考察は、論理的思考のツールの1つである。

<!---
In 1958, the Harvard Business Review published “Industrial Dynamics: A Major Breakthrough for Decision Makers,” a landmark paper by Jay Forrester, MIT Sloan School professor.
This paper spurred the movement of systems thinking in business education, and the MIT Sloan School of Management became known for educating people in system dynamics.
System dynamics is sometimes treated as a synonym for systems thinking , though the latter is a more general term.
--->

1958年、ハーバードビジネスレビューにおいて、MITスローン経営学大学院教授のジェイ・フォレスターによって[「インダストリアルダイナミックス：意思決定者のための主要なブレークスルー」](http://www.lottepiil.dk/kandidat/Industrial%20Dynamics%20(Forrester%201958).pdf)という画期的な論文が発表された。  
この論文は、職業教育においてシステム思考のムーブメントを駆り立て、そして、MITスローン経営学大学院は、システムダイナミクスの中で人々を教育するものとして知られるようになった。
システムダイナミクスはシステム思考の類義表現として、時々論じられるが、システム思考はより一般的な専門用語である。


<!---
MIT also attracted other system-dynamics-oriented researchers such as Peter Senge.
--->

MITは、ピーター・センゲなどの他のシステムダイナミクス指向の研究者も引き付けた。

<!---
Consistent with Weinberg-Brook’s Law , Forrester’s research showed that decision makers who were given dynamic models of a business system and asked to improve their output performance, usually made them run worse [SKRRS94].
The observation was that most people have weak judgement on how to fundamentally improve systems, usually applying incorrect “common sense” and quick-fix ‘solutions’ that do not create long-lasting systemic improvement.
--->

ワインバーグ-ブルックスの法則と一致するものとして、フォレスター・リサーチ社は、ビジネス・システムの力学モデルを考慮し、アウトプットのパフォーマンスの改善をさせて欲しいと頼む意思決定者がよく悪化させてしまうということを明らかにした。[[SKRRS94]](http://www.amazon.com/The-Fifth-Discipline-Fieldbook-Organization/dp/0385472560/ref=sr_1_fkmr0_3?ie=UTF8&qid=1413528034&sr=8-3-fkmr0&keywords=The+Fifth+Discipline+%EF%BF%BCFieldbook)
その結果は、ほとんどの人は通常、間違った「常識」と、持続的な組織の改善をしない応急処置的な「ソリューション」を適用し、根本的にシステムを改善する方法について乏しい判断しか持ち合わせていないということであった。

<!---
Why is the behavior of a large development group (a system) not understood or guided skillfully?
The answer lies, in part, in the behavior of stochastic systems with queues and variability, as explored in the Queueing Theory LeSS principle.
And the same answer lies in control theory :
Most systems of interest—such as a product development group—have complex positive and negative feedback loops and nonlinear behavior.
The behavior of these systems defies our gut instinct.
And then there is the minor issue of people.
--->

なぜ、大きな開発グループ（組織）の行動は、理解されなかったりうまく先導されなかったのか？  
答えは、LeSSの原則である[待ち行列理論](http://less.works/less/principles/queueing_theory.html)の中で掘り下げているように、待ち行列と変動性を持つ確率論的なシステムの振る舞いの部分的なものの中にある。  
そして、同じような答えが制御理論にある：  
－製品開発グループのような－ほとんどの組織は、複合的にポジティブかつネガティブなフィードバックループおよび非線型挙動を持っている。  
これらの組織の行動は直感を無視している。  
それから、ちょっとした人々の問題がある。


<!---
In summary, reasons for not being skillful in fathoming or guiding a big system include (but are not limited to):
--->
大きなシステムを理解したり指導することに熟練していないことの理由の要約（しかし、以下に制限されない）：

<!---
* lack of knowledge about the system dynamics, feedback loops, nonlinear systems behavior, and unintended consequences in workplace systems
* not understanding root causes of problems (and how to find)
    * causes, not cause;
      in systems thinking one sees that there are multiple, indirect, and dynamic causes to problems
* not knowing if or why quick-fix or local-department decisions degraded overall delivery performance.
--->

* システムダイナミクス、フィードバックループ、突然変換する組織の行動、職場組織における思いがけない結果について知識が不足している
* 問題の根本的な原因（や、その見つけ方）を理解しない
    * 原因というのはは複数あるもので、一つではない  
      システム思考で、複数、間接的、動的に作用を及ぼすような原因が問題となっていることがわかる
* もし、あるいは、なぜ応急処置やローカル部門の決定した時に、全体の配達性能を低下させたのか理由がわからない

<!---
In short, not being systems thinkers.
--->

要するに、システム思考できる人がいないのである。

<!---
These reasons are consequential at the intersection of management and large-scale adoption of lean and agile principles.
The leadership team is part of the system being perturbed;
if they do not apply systems thinking, they could really perturb it—and not in a good way!
--->

これらの理由は、マネジメントとリーンおよびアジャイルな原則の大規模な採用が交差する点において重要である。  
システムの一部として存在するようなリーダーシップチームは、かき乱すだろう；  
もし彼らがシステム思考を適用しないならば、本当に混乱させるかもしれないし、よい方法ではない！

<!---
As a summary of systems thinking insight, we like the 11 ‘laws’ described in The Fifth Discipline:
--->

システム思考の見識からの要約として、私達は、[5つの規律](http://www.amazon.com/Fifth-Discipline-Practice-Learning-Organization-ebook/dp/B000SEIFKK/ref=sr_1_1?ie=UTF8&qid=1413531002&sr=8-1&keywords=the+fifth+discipline)（邦題：[最強組織の法則](https://www.amazon.co.jp/dp/419860309X/ref=pd_sim_14_3?ie=UTF8&dpID=51YRBFKJWEL&dpSrc=sims&preST=_AC_UL160_SR108%2C160_&psc=1&refRID=P6DY1MPQRY4RCD2NQ9K7) / 完訳版：[学習する組織](https://www.amazon.co.jp/dp/4862761011/)）の中の[11の‘慣習’](https://en.wikipedia.org/wiki/The_Fifth_Discipline#The_11_Laws_of_the_Fifth_Discipline)が説明されることを好んでいる：

---

<!---
* Today’s problems come from yesterday’s ‘solutions.’
* The harder you push, the harder the system pushes back.
* Behavior will grow worse before it grows better.
* The easy way out usually leads back in.
* The cure can be worse than the disease.
* Faster is slower.
* Cause and effect are not closely related in time and space.
* Small changes can produce big results…but the areas of highest leverage are often the least obvious.
* You can have your cake and eat it too—but not all at once.
* Dividing an elephant in half does not produce two small elephants.
* There is no blame.
--->

1. 今日の問題は昨日の‘解決策’から発生する
1. あなたが激しく押すにつれて、システムはより激しく押し戻す
1. 行動はよくなるよりも先に悪くなる
1. いつも先導されるのが当たり前という姿勢から抜け出す
1. 治療は病気より悪影響を与えることもある
1. より速くはより遅くなる
1. 原因と結果は、時間やスペースと密接に関連しない
1. 小さな変更は、大きい結果をもたらすことができる… しかし、最高の手段というのは、少なく明白なことがほとんど
1. あなたはケーキを、一度だけでなく何度も食べることができる
1. 象を半分に分けても、2匹の小さな象を産むわけではない
1. 疑いようがないものである

---

<!---
Toyota’s internal motto is “Good thinking, good products.”
Systems thinking is a set of thinking tools to help…
--->

トヨタの標語は、[「よい思考、よい製品」](http://www.toyota-global.com/company/toyota_traditions/quality/may_jun_2005.html)である  
システム思考は、それを手助けする思考ツールのセットである…

<!---
* see system dynamics—
  a development organization is a system of people and policies with subtle feedback loops and unintended consequences
    * we can learn to see and thus improve the system with **causal loop diagrams** created in a workshop
* see mental models—
  one reason behind suboptimal decisions is mistaken assumptions and faulty reasoning
    * causal loop diagramming and Five Whys expose these
* see local optimization—
  another source of suboptimal decisions is local optimization,
  making the ‘best’ decision from the viewpoint of a person or department,
  rather than global optimization for the lean systems-level goal of deliver value fast with high quality and high morale.
--->

* システムダイナミクスを知る  
  開発組織は、捉えがたいフィードバックループと予想だにしない成り行きと共にする人々とポリシーのシステムである
    * 私達は、ワークショップで作成された **因果ループ図** によってシステムを改善することを学ぶことができる
* メンタルモデルを知る  
  部分的な解決になっている背景には、誤った仮定と不完全な理由がある
    * 因果ループ図と'5つのなぜ'が、これらを明らかにする
* 部分最適を知る  
  部分的な解決になっている別の要因は、高い品質や意欲と共に素早く価値を提供するというリーンのシステムゴールのための **全体最適化** よりも、人または部門の観点から‘最もよい’解決策を作るという **部分最適化** である

<!---
This introduction is organized around the following areas in systems thinking: Learning to see (1) system dynamics , (2) mental models , (3) root causes , and (4) local optimization .
--->

この序論は、システム思考の下記の要素で構成される：  
学べること  
(1) システムダイナミクス  
(2) メンタルモデル  
(3) 根本原因  
(4) 部分最適化  


<!---
Seeing System Dynamics: Introduction
--->

### システムダイナミクスを知る：序文 

<!---
Static versus Dynamic Complexity
--->

#### 複雑さにおける 静的 VS 動的 

<!---
Many of us, especially in engineering and finance, are educated to master complexity of static details—learning to analyze and manage information (requirements, financial analysis, …), decompose complex structures into simpler ones, and so forth.
That is, complexity of a static, information, or structural nature.
--->

私達の多くは、特にエンジニアリングおよび財政において、静的な内容  
ー情報（要件、財務分析、…）を分析し、管理したり、複雑な構造をより簡単なものなどに分解することを学ぶことなどー  
の複雑さをマスターするために教育される。  
すなわち、静的、情報、または構造の自然の複雑さ。


<!---
Why do big software systems tend to degrade, with more and more time spent on defects?
What might happen if the USA invades Iraq?
Seeing the dynamics behind these questions involves analysis of the complexity of dynamics.
--->

なぜ、大きなソフトウェアシステムは欠陥に使われたより多くの時間とともに低下する傾向があるのか？  
もし米国がイラクを侵略するならば、何が起こるであろうか？  
力学の背景にあるこれらの問題を理解するには、力学の複雑さに関する分析を必要とする。

<!---
In contrast to static-details education, many of us receive no formal education in analyzing dynamics complexity, especially workplace dynamics.
Perhaps there is a belief it is sufficient to rely on common sense in the workplace.
Forrester demonstrated that “common sense” is just not so in complex systems,
and showed it is possible to formally educate people to become better system dynamics thinkers in the workplace using dynamic system models visualized in flow diagrams [Forrester61].
--->

静的詳細教育と対比すると、私達の多くは、特に職場力学という分析力学の複雑さについて形式的な教育を全然受けない。  
おそらく、職場の常識に頼っていることに十分な確信を持っている。  
フォレスターはただ「常識」が複雑系にそうないのを証明した、  
そして、フローチャート[Forrester61]において視覚化された動的なシステムモデルを使い、これまでよりも良い形で職場のシステムダイナミクス思想家になるように、人々を形式的に教育することが可能であると伝えている。

<!---
Flow diagrams encompass material, financial, and information flows, stocks (variables with a quantity, such as cash or number of defects), the impact of decisions and policies, and cause-effect relations.
A popular simplification is the causal loop diagram that focuses on cause-effect relationships and feedback loops in a system [Sterman00].
There are a variety of similar notations;
they all show stocks (variables), causal links, and delay.
In [Weinberg92] this is called the diagram of effect.
--->

フローチャートは、素材、金融、および情報フロー、株（欠陥の現金や数などの量を持つ変数）、決定と方針のインパクト、および原因効果関係を含んでいる。  
ポピュラーな単純化は、システム[Sterman00]の原因効果関係とフィードバックループを中心に行う因果ループ図である。  
各種の同様な表記法がある；  
それらすべては、株（変数）、原因となるリンク、および遅延を示す。  
[Weinberg92]において、これは効果の図と呼ばれる。

<!---
The First Law of Diagramming: Model to Have a Conversation
--->

### 図示の最初の規定：対話をするモデル

<!---
A tool to learn to see system dynamics is a causal loop diagram, ideally sketched on a whiteboard in a LeSS Overall Retrospective with colleagues.
Before going further, here is the First Law of Diagramming
--->

システムダイナミクスを理解するためのツールは、因果ループ図である。理想としては同僚と一緒にLeSSのオーバーオールレトロスペクティブの中で、ホワイトボードに書けるとよい。  
先に進む前に、これが図示するための最初の規律である

<!---
> The primary value in diagrams is in the discussion while diagramming—we model to have a conversation.
--->

図の主要な価値は、図示する間の議論にある－対話しながらのモデリング

<!---
When a group gets together to sketch a causal loop diagram on a whiteboard (See it is the acts of discussing and thinking that are most important when diagramming, Valtech India.),
the primary value is the conversation and shared understanding they arrive at while creating the model.
Its visualization as an easy-to-see diagram is important to make concrete and unambiguous (on the whiteboard) the ideas—the mental models people have—because words alone can be fuzzy and misunderstood.
But still, the diagram is secondary to what people take away:
learning and a revised understanding through a discussion.
--->

グループがホワイトボードに因果ループ図を描くために集まる時（Valtech India社では、議論して考えることが図示するときの最も重要な行為であることがわかる）、  
主要な価値は対話であり、それが彼らがモデルを作成する間に生まれた理解を共有している。  
言葉だけではあいまいで誤解するかもしれないため、簡単でわかりやすい図は、（ホワイトボード上で）アイデア－人々が持つメンタルモデル－を具体的かつ明白にすることが重要である。  
それでもやはり、図は二の次である。人々が持ち帰る何か（対話を通しての理解で、学び復習すること）

![](https://less.works/img/systems_thinking/xgroup,P20cld,P20modeling.jpg.pagespeed.ic.Pnh1_YRIQk.jpg)

<!---
Doing system thinking.
Sketching a causal loop diagram together—modeling to have a conversation.
--->

システム思考を実践中。  
因果ループ図を対話しながら一緒にモデリングして描いている。

<!---
Concrete modeling tip :
We start by writing on sticky notes to define variables.
A note might read “feature velocity” or “# defects.”
We place these on a whiteboard.
Then we sketch causal link lines between the sticky notes.
There will be (or should be) lots of rewriting, erasing, and redrawing during the modeling session.
The most meaningful outcome is understanding ; in addition, some participants will want to take a digital photo of the whiteboard sketch.
--->

具体的なモデリングの秘訣：  
私達は、変数を定義するために、付箋に書いて始める。  
付箋からは、“機能速度”、または“#欠陥。”を読みとることができる。  
これらをホワイトボードに貼る。  
そして、付箋の間に原因を表す線をスケッチする。  
モデリング中にたくさんの書き替え、消したり、また書き直したりする（または、そうであるはずである）。  
最も意味がある結果は理解がある；さらに、何人かの参加者がホワイトボードスケッチのデジタルの写真を撮りたいだろう。

<!---
Seeing System Dynamics: Causal Loop Diagrams
--->

### システムダイナミクスを知る：因果ループ図 

<!---
Causal loop diagrams are used regularly in introductions to LeSS, to help see the dynamics of what is going on in large-scale development.
It is useful to understand them for that reason alone.
And more useful to you,
we recommend you do these together with colleagues at a whiteboard.
Model to have a conversation.
When?
Probably during a LeSS Overall Retrospective.
--->

因果ループ図は、大規模な開発において力学がそういうものだと理解するのに役立つように、LeSSの序文の中で正式に使われる。  
理由だけを理解することに役立つ。  
そして、あなたにとって有益である、私達は、ホワイトボードで同僚とともにこれらをするように勧める。  
対話しながらモデリングをする。  
いつ実施するのか？  
たぶん、LeSSのオーバーオールレトロスペクティブの時に。

<!---
The practical aspect of this tip is more important than may first be appreciated.
It is vague and low-impact to suggest “be a systems thinker.”
But if you and four colleagues get into the habit of standing together at a large whiteboard,
sketching causal loop diagrams together,
then there is a concrete and potentially high-impact practice that connects “be a systems thinker” with “do systems thinking.”
--->

この秘訣の実用的な面は、最初に真価が認められうるより重要である。  
「システム思想家でありなさい。」ということを示唆することは、漠然としていて、印象としては小さい。  
しかし、もしあなたと4人の同僚が、大きいホワイトボードの前で一緒に立つことを習慣にしていれば、一緒に因果ループ図を描くことができ、  
そして、「システム思想家でありなさい」を、「システム思考をしなさい。」に繋げるプラクティスとして高い印象を与える可能性がある。

<!---
The following examples seem sterile when presented in a book.
But imagine you were at a whiteboard with other people and the diagrams were being sketched during a lively conversation.
That’s the way we suggest ‘doing’ systems thinking.
--->

以下の例は、本の中で示されているような内容が乏しいものに見えるかもしれない。  
しかし、あなたが、他の人々と一緒にホワイトボード前にいて、活発な会話中に図の概略を述べていたと想像してください。  
それが、私達が提案するシステム思考を‘実践する’方法である。

<!---
Notation and Examples
--->

#### 表記法と例

<!---
Causal loop diagrams contain many elements; the following common useful subset is explored through a scenario.
--->

因果ループ図は多くの要素を含んでいる；  
以下の共通の有益なサブセットはシナリオを通して探究される。

<!---
* Variables           reactions; quick-fix reactions
* causal links        interaction effects
* opposite effects    extreme effects
* constraints         delays
* goals               positive feedback loops
--->

* Variables（変数）           反応; その場しのぎの反応
* causal links（因果リンク）   相互作用した効果
* opposite effects（相反効果） 極端な効果
* constraints（制約）         遅延
* goals（ゴール）             ポジティブなフィードバックループ

<!---
The following simplified scenario is for a particular organization. It is not a generalization.
--->

以下の簡素化されたシナリオは、特定の組織に向いているもので、一般化ではない。

<!---
Variables—
Causal loop diagrams include variables (or stocks) such as the velocity (rate of delivery) of software features and number of defects.
Variables have a measurable quantity.
--->

変数ー  
因果ループ図は、欠陥数やソフトウェア機能の生産量（納品率）のような変数を含む。  
変数は、測定できる量を持っている必要がある。

![](https://less.works/img/systems_thinking/xsystems,P20thinking-4.png.pagespeed.ic.7hyPwR5tv7.png)

<!---
Causal links—An element can have an effect on another, such as if feature velocity increases, then the number of defects increase;
that is, more new code, more defects.
--->

因果リンク－要素は別の効果があるかもしれない、もし機能生産量の増加させれば、欠陥数が増加するかもしれない；  
すなわち、より新しいコードが増え、それに伴いより多くの欠陥が増えるということである。

![](https://less.works/img/systems_thinking/xsystems,P20thinking-5.png.pagespeed.ic.1C4UDvPgs8.png)

<!---
Now it is time to bump into Weinberg-Brook’s Law and the Causation Fallacy.
It is easy to sketch a diagram;
it is something else to model with insight.
For example, consider the relationship between the number of developers and feature velocity.
--->

今や、ワインバーグ・ブルックの法則と因果関係の誤った推論をぶつける時である。  
図を描くことは容易である；  
それは、洞察を持つ素晴らしいモデルである。  
例えば、開発者の数と機能生産量の間の関係を考察する。

<!---
The nature of any cause-effect relationship is actually not obvious,
though it is common for people to jump to conclusions such as more developers means better velocity.
Adding people late in development may reduce velocity (a sub-element of “Brooks’ Law” [Brooks95]).
Or, more bad programmers could really slow you down.
An argument can be made that removing terrible developers can improve velocity.
--->

人々がより多くの開発者がより生産量を多くするという意味のような結論に跳ぶというような発想は人々に共通しているが、  
全ての原因と効果の関係の性質は、実際には明らかにならない、  
人を追加することは、開発の遅延させ生産量を減らすかもしれない（「ブルックスの法則」の部分的な要素[Brooks95]）。  
または、能力の低いプログラマーは、あなたの生産性を落とすことができるだろう。  
ひどい開発者を除去することが生産量を高めることができると言った議論を作ることができる。

![](https://less.works/img/systems_thinking/xsystems,P20thinking-6.png.pagespeed.ic.Gl_PMhx0t9.png)

<!---
Opposite effects—A causal link effect may be the same or opposite direction;
if A goes up then B goes up, or vice versa.
Opposite effect is shown with an ‘O’ on the line.
Suppose defects going up puts a drag on the system,
lowering the velocity of new features because people spend more time fixing or working around bugs.
--->

逆の効果－原因となるリンク効果Aは同じまたは逆方向であるかもしれない；  
もしAが上がるならば、Bは上が理、逆もまたしかり。  
逆の効果は、ライン上に『O』で示される。  
バグ対応に追われて多くの時間を費やすため、新機能を生産する量は低下することから、欠陥とはシステム上に邪魔なものを置いていくとようなものである。

![](https://less.works/img/systems_thinking/xsystems,P20thinking-7.png.pagespeed.ic.uD9mVpPZOe.png)

<!---
Constraints—Unless you can find people to work for free,
there is a constraint on the number of developers, based upon cash supply.
--->

制約－無償で働く人々を見つけることができない限り、報酬支払いに基づいて雇う開発者の人数という制約がある。

<!---
Constraints are not causal links.
As cash supply goes up, it is not the case that the number of developers goes up.
--->

制約は、因果リンクではない。  
報酬が増えることで、開発者の人数が上がるというケースではない。

![](https://less.works/img/systems_thinking/xsystems,P20thinking-8.png.pagespeed.ic.p4v-WNXZCh.png)

<!---
Goals and Reactions–People, departments, and systems have goals, such as higher feature velocity.
Goals often generate pressure for people to react (or act), with the intent of achieving the goal.
But since there is Causation Fallacy and Weinberg-Brooks’ Law to contend with,
people should be cautious about assuming what actions will help.
Now a goal and pressure for reaction is shown:
--->

目標と反応－人々、部門、およびシステムはより高い機能や生産量などの目標を持っている。  
目標はよく、目標を達成する意思を伴った反応（または行動）をすることでプレッシャーを生む。  
しかし、誤った考えから導き出された因果関係とワインバーグ・ブルックスの法則の対立があるゆえに、  
どんな行動も助けになると思い込むことに注意すべきである。  
今や、目標とプレッシャーの反応は表すことができる。

![](https://less.works/img/systems_thinking/xsystems,P20thinking-9.png.pagespeed.ic.7T3j6vKX6T.png)

<!---
Not only does a goal with a reward create pressure to act,
but also it creates pressure to appear to be acting and achieving,
due to the measurement dysfunction generated by rewards.
And the measurement dysfunction can be proportional to the perceived value of the reward
because people are being motivated to get a reward, not to improve the system [Austin96].
Notice how rewards can actually degrade system performance.
Visually, the system dynamics may be…
--->

報酬を目的として目標を達成することが、その行動でプレッシャーを生み出すだけではなく、  
行動し、達成しているようにも見えることもまたプレッシャーを生み出しており、  
それが報酬が生み出した機能不全の大きさの結果である。  
そして、機能不全の大きさは、報酬の価値を認めることに比例しているかもしれない。  
なぜなら、システム[Austin96]を改善することではなく、人々が報酬を得ることが動機となるからである。  
報酬が実際どのようにシステム・パフォーマンスを低下させるのかということに気づきなさい。  
見た目上、システムダイナミクスはそういっているかもしれない…

![](https://less.works/img/systems_thinking/xsystems,P20thinking-10.png.pagespeed.ic.dyejPasI0I.png)

<!---
It is quite interesting that all these dynamics have been added by introduction of reward,
and yet there is no necessary connection between the top part of this model and the bottom.
--->

すべてのこれらの力学が報酬の導入により追加されたことは非常に興味深い、  
それなのに、このモデルの一番上と下との間に必要な繋がりが全くない。

<!---
There is no guarantee that feature velocity has improved—or even been worked on.
--->

機能生産量が、改善したという保証が全然ないーよりいっそう取り組んだとしても。  

<!---
Removing the reward system is a root-cause solution to the dysfunction.
Another (lesser) surface countermeasure is the lean-thinking Go See (go see physically at the place of real work) principle and management behavior:
--->

報酬システムを取り除くことは機能不全の根本原因の解決策である。  
別の（より小さい）表面上の対策は、リーン思考の Go See（実際の仕事場に物理的に見に行くこと）の原則と管理行動である：

![](https://less.works/img/systems_thinking/xsystems,P20thinking-11.png.pagespeed.ic.mXineYilEP.png)

<!---
Quick-fix reactions—One difficult and slow solution toward the goal of higher velocity is to hire great developers,
to increase coaching and education of existing staff, and to remove terrible workers.
The alternative is called a quick fix , a reaction that is hoped to achieve the goal quickly and with less effort.
Sometimes a quick fix works well both in the short and long term, really strengthening the system.
Sometimes not…hence, “faster is slower.”
For example, people may believe that increasing the number of developers increases the feature velocity.
And they may thereby hope that hiring more developers will most quickly and easily solve the velocity problem.
‘QF’ indicates the quick fix:
--->

応急処置の反応－より高い生産量の目標に対して、難しく、時間のかかる解決策のひとつは、既存の開発者の指導と教育を増やし、ひどい労働者を追放するために、優れた開発者を雇うことである、  
選択肢は、その場しのぎの解決策と呼ばれ、少ない努力によって目標を迅速に達成するために望まれている反応である。  
その場しのぎの解決策は短期的にも長期的にもうまく作用し、実際にシステムを強化したりすることもあれば、そうでないこともある。  
「より速くはより時間がかかる」  
例えば、人々は、開発者の数を増大させることが機能生産量を増大させると信じるかもしれない。  
そして、より多くの開発者を雇うことにより生産性の問題を最も迅速に、容易に解決されることを望むかもしれない。  
『QF』はその場しのぎの解決策（quick fix）を示している：

![](https://less.works/img/systems_thinking/xsystems,P20thinking-12.png.pagespeed.ic.BS-FVQWluL.png)

<!---
Interaction effects—There is the constraint of cash supply on hiring.
One hard and slow solution is to get more cash.
A quicker fix is to hire much cheaper developers.
In this case, the level of cash supply now has an interaction effect with other causal links.
Low cash tends to strengthen the hire rate of much cheaper developers when there is pressure to increase hire rates.
--->

相互効果－雇用には給与払いの制約がある。  
難しく、時間のかかる解決策のひとつは、より多くの報酬を得ることである。  
その場しのぎの解決策は、低賃金開発者をたくさん雇用することである。  
このケースにおいて、報酬額のレベルは、現在、他の因果リンクによって相互効果がある。  
低予算は、雇用率を増やすプレッシャーがある時に、たくさんの低賃金開発者の雇用率を増やす傾向がある。

<!---
One could simply draw an (opposite) causal link directly from cash supply to hire rate of very cheap developers,
but that merely says that less cash leads to more hiring of extremely cheap developers.
That is not quite what we want to say; rather, we want to show the interaction effect—that effect A influences effect B.
This is done by showing a causal link entering another causal link.
For example, from cash supply to the quick-fix line going into hire rate of very cheap developers :
--->


低賃金開発者の雇用率に対して、（逆の）因果リンクを給与払いから単純に引くことができた、  
少ない予算が極めて低賃金な開発者をより多くの雇用するを引き起こしていると単に言っている。  
それは、私達が言いたいことではない；むしろ、私達はー影響Aは影響Bをもたらすといったー相互効果を示したい。  
これは、因果リンクを、別の因果リンクに合流するように見せることでできる。  
給与払いから低賃金開発者の雇用率に入っている応急処置の線の例：

![](https://less.works/img/systems_thinking/xsystems,P20thinking-13.png.pagespeed.ic.hoU7NExB0v.png)

<!---
Extreme effects—We have worked with some very inexpensive developers with excellent skill and some very expensive developers that are terrible,
but on average, you get what you pay for—when you hire from a large pool of very cheap labor, the average skill level is lower.
In the model we want to show that the impact of hiring very cheap labor on the number of low-skilled developers is a significantly greater effect than average.
--->

極端な効果－私達は、何人かの大変優秀なスキルを持っているにも関わらずとても低賃金な開発者、そして、驚くほど非常に高収入な開発者と働いたことがある、  
しかし、平均的に、あなたは、支払った分に見合ったものを得る－あなたがたくさんの低賃金労働者の中から雇用する時には、その平均的なスキルレベルはより低い。  
モデルの中で、私達は、低スキルの開発者の数の低賃金労働者を雇用すことの影響が、平均的なものよりかなり大きな影響を及ぼすことを示したい。

<!---
To show an extreme effect in the model, use a thick line:
--->

モデルの中で、極端な効果を示すためには、太線を使うこと：

![](https://less.works/img/systems_thinking/xsystems,P20thinking-14.png.pagespeed.ic.lhixsuuEBI.png)

<!---
Delays—One problem in hiring in software development is the fallacy of mild programmer variance
—the mistaken belief that programmer variance (in terms of productivity, code quality, etc.) is relatively small.
However, programmer variance studies suggest an average of four times faster in the top versus bottom quartile [Prechelt00].
Rather significant.
Also, the COCOMO model—based on large and longitudinal studies—shows that the capability of the development personnel is by far the most important factor for productivity [Boehm00].
And, on average, very weak programmers create poor-quality code (poor design) and more defects, creating another drag on the system.
--->

遅延－ソフトウェア開発において雇用することにおける1つの問題が、プログラマーの偏りはあまりないという誤った考えである  
－プログラマーの偏り（生産性 コード品質など）は比較的少ないということを信じているのは間違いである。  
しかし、プログラマーの偏りは、最上位の人と最下位の人で見たとき25％[Prechelt00]は平均よりも4倍仕事が速いとを示唆することを学んだ。  
むしろ意義深いことである。  
また、 COCOMOモデル－大規模かつ長期的な研究に基づく－開発人員の能力は生産性[Boehm00]のための最も重要な要因であることを見せてくれた。  
そして平均的に、能力の低いプログラマーは低品質のコード（ダメな設計）とより多くの欠陥を生み、システムのための別の障害物を作成する。

> メモ：  
> COCOMOモデル  
> ソフトウェア開発費用を見積もる手法のひとつ。  
> 開発に必要とする段階の数、各工程の難易度、あるいはチームの開発能力などを補正係数として掛け合わせて、工程数や人員を見積もる手法のこと。

<!---
But the impacts of these effects are not immediately obvious.
For example, it takes a relatively long time after hiring a large pool of weak programmers before the impacts of more and more bad code/design start to be felt.
Similarly, the average decrease in feature velocity (because of the powerful impact of programmer variance) will not show up immediately.
--->

しかし、これらの効果のインパクトはすぐに明らかになるものではない。  
例えば、能力の低いプログラマーを大量雇用した後、ますます多くの悪いコード／設計のインパクトを感じ始めるには相対的に長い時間かかる。  
同様に、機能生産量（プログラマーの偏りの強力なインパクトによる）の平均値の減少は、すぐには現れない。

<!---
To show these delayed effects in the model, use a double-line through the effect line:
--->

モデルの中で、これらの遅延効果を示すためには、効果ラインを通して二重線を使う：

![](https://less.works/img/systems_thinking/xsystems,P20thinking-15.png.pagespeed.ic.wNs033QPdZ.png)

<!---
Delay has an intriguing influence on the educational or corrective power in a system.
If an impact or unintended consequence is long delayed,
one does not feel the effect (pain or gain) and so does not clearly see how A influenced B, or more subtly how A influenced B influenced A .
--->

遅延は、システムにおいて、教育的で興味深い影響や矯正力を持っている。  
もし影響や思いがけない結果が長い間遅延させるようであれば、  
効果（苦痛または利益）を感じず、どのようにAがBに影響し、また、どのようにAがBに、そしてBがAに影響したかというより微妙なことがはっきりとわからない。

<!---
Therefore, one does not learn from or correct mistakes—in policy, management actions, tools, and so forth.
Likewise, gradual improvement through the lean thinking practice of kaizen can take a long time;
patience and insight are needed to see if and how things improve.
--->

従って、－方針、管理動作、ツールなどー明らかな誤りを正そうとせず、学びもしない。  
その上、改善活動といったリーン思考の実践に時間がかかるかもしれず、ゆるやかな改良になる；  
忍耐と洞察は、どのように物が改善するかを理解するために必要である。

<!---
Positive feedback loops—
Negative or positive feedback loops5 and delays are where things start to get more subtle in a system—and in understanding a system.
For example, how does one become a better programmer?
In part, by mentoring from great programmers and seeing lots of examples of great code.
But an office with a lot of low-skill developers does not generate a lot of great code examples, nor does it attract or retain the small pool of great programmers who could act as mentors.
They would rather work somewhere else.
--->

ポジティブなフィードバックループ－  
ネガティブまたはポジティブなフィードバックはループし、遅延は、システムにおいてより微妙になり始める所であり－システムを理解する中で。  
例えば、どのようにして、よりよいプログラマーになるか？  
偉大なプログラマーからの指導や、たくさんの素晴らしいコードの例として見ることは一部分である。  
しかし、たくさんの低スキルな開発者を持つオフィスは、たくさんの大きい素晴らしいコードの例を作れず、それは、指導者として行動できた少ない偉大なプログラマー引き付けず、維持もできない。  
彼らはどこか他の場所で働くほうがよいだろう。

<!---
Now the development group starts to enter a self-reinforcing downward spiral—a set of positive feedback loops.
Fortunately, the downward trend is constrained by the supply of cash.
--->

今や、開発グループは下向きのスパイラルを自ら補強し始める－ポジティブなフィードバックループの1セット。  
幸運にも、下向きの傾向は報酬により制約される。

<!---
More great programmers—who could craft great code and mentor others—leave.
So there is less and less quality code to look at and to learn from.
The percentage of weak programmers grows even larger and feature velocity drops further.
Code becomes more messy, awkward, and duplication-riddled, so the capacity to swiftly implement features declines.
Since feature velocity is dropping further, there is more pressure to hire yet more very cheap programmers.
All this leads to multiple positive reinforcement loops in the system, for example:
--->

－素晴らしいコードや指導などを念入り作れた－より偉大なプログラマーは去る。  
そして、質の高いコードから見て学ぶことはますます少なくなる。  
定スキルのプログラマーの割合はいっそう大きくなり、機能生産量の落下は促進する。  
コードはより乱雑で、扱いにくく、重複したもので溢れる。従って、機能を迅速に実装する能力は、衰える。  
機能生産量がさらに低下すると、いっそう低賃金のプログラマーを雇用するためのより多くのプレッシャーになる。  
このすべてがシステムにおいて複数のポジティブな増強ループをもたらすことを導く、例えば：

![](https://less.works/img/systems_thinking/xsystems,P20thinking-16.png.pagespeed.ic.mnzd-1dyJm.png)

<!---
Tip : You can find positive feedback loops by finding cycles with an even number of ‘Opposite’ effect relationships.
There are several examples in the model above.
--->

秘訣：あなたは、『逆の』効果の多く数のをもつサイクルとの関係性を見つけることで、ポジティブなフィードバックループを見つけることができる。  
上記のモデルにいくつかの例がある。


<!---
Conclusion
--->

#### 終わりに

<!---
The example scenario is only that—an example.
A causal loop diagram can visualize rich dynamics in a workplace system.
These are best created by a group at a whiteboard.
--->

シナリオは、あくまで例である。  
因果ループ図によって、職場システムの豊かな力学は視覚化できる。  
これらはホワイトボードでグループで実施することで最もよいものが作成される。

<!---
Seeing Mental Models
--->

<!---
The previous causal loop diagrams reflect people’s mental models of causation, which may be wrong. It is interesting to note that people’s models of causation are influenced by the timeliness (delay) and quality of feedback in the system.
--->

<!---
The implication of “mental models” is to improve our meta-cognitive skill to see and question our own assumptions and chains of reasoning. Are we making faulty leaps of logic? It also implies when working with others to discuss (inquiring rather than abusing) the mental models of our colleagues.
--->

<!---
Seeing these mental models is step one; changing them is the even harder part of step two. That art is beyond the scope of this introduction, though a successful LeSS adoption must involve changes in mindset and insight among many groups.
--->

<!---
A tip to better see the mental models (beliefs, chains of inference, …) playing out in the system dynamics is to ask the following question during a modeling workshop and then sketch the answers. “Let’s talk about the assumptions behind this model. What do we believe or assume in terms of facts and effects that led us here?”
--->

<!---
Answers are sketched on the whiteboard model, for example:
--->

![](https://less.works/img/systems_thinking/xsystems,P20thinking-17.png.pagespeed.ic.-_xkd1LDSi.png)

<!---
Visualizing the assumptions in our heads... our mental models.
--->

<!---
Example: The “Faster is Slower” Dynamic
--->

<!---
With the vocabulary of quick fixes, delays, positive feedback loops, and mental models, it is fascinating to see that there can be a short-term apparent improvement in a variable as the result of a quick fix, but a delayed degradation of the very same variable—the “faster is slower” dynamic. This is a recurrent dynamic in the workplace and a cause of weakness. So it is worth another illustration.
--->

<!---
The story of Microsoft Word and the secret developer toolbox : A classic example of the short-term ‘improving’ but long-term degrading dynamic is the story of the first release of Microsoft Word for Windows [Spolsky04]. It was released years later than desired. Why? Because managers tried to follow the original schedule and pushed developers to meet it .
--->

<!---
The story illustrates why wishful thinking is identified as one of the wastes in lean thinking. In this case the wishful thinking of insisting on (apparently) following a schedule, which implies the misconception or wishful thinking that development estimates are not estimates but are commitments—a common myth that propels degradation of a system.
--->

<!---
The next model illustrates a summary of the dynamics of what happened when the managers pushed people to evidently keep to the original schedule, and why this quick-fix reaction to slow progress appeared to make things faster in the short term but actually even slower in the long term. See the dynamic of schedule pressure and the secret toolbox. intentionally omits some deeper dynamics that are expanded and shown in See deeper dynamics of schedule pressure and the secret toolbox..
--->

![](https://less.works/img/systems_thinking/xsystems,P20thinking-18.png.pagespeed.ic.KhJK1oUzzu.png)

<!---
The dynamic of schedule pressure and the secret toolbox.
--->

<!---
As a quick fix, the Microsoft managers exhorted, bribed (with potential rewards), and threatened the Word developers to keep to the original schedule. Consequently, the developers predictably pulled out their secret developer toolbox —the many practices related to hacking out dirty code (no tests, no reviews, ignore known defects, copy-paste programming, poor design, …) to apparently deliver a feature faster. You see, developers also have quick-fix reactions for their problems.
--->

<!---
The tactics seemed to have worked like magic. As the managers pressured the developers, ‘features’ were delivered quicker as people used the secret toolbox, which reinforced the belief that pressuring developers helps. But this apparent acceleration actually had a delayed effect to make things slower, which is explored next. Since management did not quickly see the delayed effect of the secret toolbox, and because they believed managers should not be frequently looking in detail at the source code or themselves be master programmers, they did not learn from this dynamic.
--->

<!---
A closer exploration of the system dynamics shows why things went slower in the long term and why the first Word for Windows release was years later than desired, illustrated in this model…
--->

![](https://less.works/img/systems_thinking/xsystems,P20thinking-19.png.pagespeed.ic.HIhJ8a7Yx_.png)

<!---
Some deeper dynamics of schedule pressure and the secret toolbox.
--->

<!---
Naturally, lots of dirty code eventually slowed things down. More subtly, developers would ignore the bug list of ever-increasing open defects to—instead—generate new features. This led to a long delay between the creation of a defect and its correction. It turns out that this significantly increases variability and time to fix a defect because of the compounding negative effect of a long-lived bug (for example, due to workarounds and coupling) and because developers have long forgotten the detailed context of code related to the defect and therefore need to slowly rediscover that context—with more and more dirty confusing code surrounding them.
--->

<!---
The astute reader may also notice the several positive feedback loops that reinforce the degradation cycle; this is one reason the product was years later than intended.
--->

<!---
Solution? The lean thinking Stop and Fix and Go See principles. First , rather than trying to go faster when there are problems, manager-teachers encourage people to go slower and help them learn to see system dynamics and root causes, and to fix these—to improve the system of development. By going slower, Toyota—the masters of lean thinking—has become one of the fastest companies around. Second , for managers to go see at the real place of work to learn what is going on. The “real place” in software development is the code, which suggests that first-level managers are master programmers who are frequently evaluating the code.
--->

<!---
Microsoft people did not reflect on the situation until after release. When they did finally hold a retrospective, it led to a zero-defects policy, meaning that the first priority was to fix known bugs in the code under development—to drive down to zero the open-defects list before writing more new-feature code.
--->

<!---
Seeing (and Hearing) Local Optimization
--->

<!---
“Everyone is doing their best yet overall systems throughput is degrading. How can that be?” This is the paradox of local optimization —when a person or departmental decision maker optimizes for the local view or self-interest. The party making the decision frequently believes they are making the best decision , but because ‘best’ is a local optimization, in fact it sub-optimizes overall system throughput. This is a result of “silo mentality,” misunderstanding, fear, limited information, delayed feedback, ignorance, careerism, avarice, and other common organizational learning disorders .
--->

<!---
A small product group of 30 people does not have the time or money to engage in much nonsense or waste. But large companies, with large product groups, centralized process and tool groups, a centralized “project management office,” and so forth, seem to have raised local optimization and waste to an art form. Government bureaucracies are the quintessential example, of course. As such, when you serve as a guide in large-scale agile adoption, seeing (or hearing ) and dealing with local optimization is singularly vital.
--->

<!---
For example, the legal and corporate security departments put in place a policy that seems terribly important from their perspective. In the aim of preventing loss of intellectual property (IP), the legal department decrees “no one shall put any information on the walls.” Or, in response to cost-cutting pressure, the facilities management says, “It is important to ensure our walls are not dirty or damaged.” And thus they shut down a practice in lean thinking, visual management (which is usually done on walls), and they inhibit a well-known innovation practice, group whiteboard work. The lawyers may succeed in reducing loss of IP (actually, that is questionable), and the facilities people will succeed in keeping the walls clean—at the cost of inhibiting the product development group from innovating and collaborating. Finally, the company falls behind with less and less IP even worth protecting because tools for innovation and delivering fast have been disallowed, but the lawyers have successfully fulfilled their mandate from the executive team to “ensure our IP is protected.” And the furniture police have clear walls. They have done their best .
--->

<!---
The following is a real e-mail quote from the FURNITURE POLICE in one organization that dissallowed visual management on the walls. Can you identify the local optimizations and mental models driving this?
--->

<!---
Individual work cubic partition can be personalized. But things obvious higher than the partition or harming the office environment’s harmony are restricted.
--->

<!---
We also see local optimization in centralized groups that make software tool choices for others. The common mindset is to choose a tool that is best at reducing some supposed cost (curiously, these groups seldom recommend free open source tools) or best at doing something complicated or best for the work of one specialized worker role (even though everybody has to use the tool), rather than maximizing the global goal of faster system throughput of value to customers.
--->

<!---
In large-scale adoption of Scrum or agile principles, most of the “Yes, but …” issues that are raised are examples of local optimization, such as, “Yes, but…what about management reporting?” or more generally, “*Yes, but…what about *?” Then, policies and practices are twisted around, serving the goal of reporting or some other secondary aim rather than the primary goal of optimizing for fast value throughput. Sometimes we see *local optimization for the extreme or rare case* . For example, a person responsible for making a centralized tool choice for the enterprise presents a scenario for a complex or rare case of use, and then chooses the tool that fits that, sub-optimizing for a 5 percent case instead of optimizing for ease and speed for the 95 percent case.
--->

<!---
Other local optimizations are due to ignorance of new ways of working. This is especially common in large-scale product groups. For example, we once helped a large networking product group in Europe adopt Scrum and the practice of continuous integration (CI) combined with a CI system that continually integrated, built, and automatically tested the product. After some time, an outside traditional manager inspected what was going on, and recommended the integration practices should be changed—because there was no written integration plan for how a human integration manager should manually integrate all the software, and of course, there was no integration manager. They wanted to ‘optimize’ around the work of an integration manager that was no longer needed. They could not see that their entire old-fashioned model of work had been eliminated with CI. This story repeats in all the departments of a large established product: local optimization around the existing ways of work, such as manual test, a separate architecture department, component teams, and so on. A coach working to introduce large-scale Scrum at the enterprise level has a mountain of similar local optimization thinking to deal with.
--->

<!---
In lean thinking and agile methods, the focus is on global systems goals: Deliver value fast with high quality and morale—global optimization . Try to consider decisions in light of this goal. To develop an “optimize the whole” culture, challenge all decisions and policies with the question:
--->

<!---
Does this decision or policy focus on delivering value to the external customer fast, or does it focus on the interests of a department, person, internal policy/practice, or rare case?
--->

<!---
In LeSS, the Product Owner is responsible for choosing high-value goals that could lead to potentially shippable product (at the end of the Sprint) and that maximize the desired impacts and that delight the customer, while maintaining a sustainable pace and high engineering quality. That explicit goal is meant to orient the system toward global rather than local optimization.
--->

<!---
Conclusion
--->

<!---
In addition to becoming a systems thinker yourself, encourage others to learn more about this topic. We suggest you to try getting together at a whiteboard with colleagues to sketch a causal loop diagram, so that being systems thinkers and doing systems thinking are connected at the workplace.
--->

![](https://less.works/img/systems_thinking/xgroup,P20cld,P20modeling.jpg.pagespeed.ic.Pnh1_YRIQk.jpg)

<!---
Doing system thinking. Sketching a causal loop diagram together—modeling to have a conversation.
--->

<!---
Recommended Readings
--->

<!---
W. Edwards Deming’s Out of the Crisis is a master work by arguably the most well-known systems thinker and quality expert. It opens with the modest goal, “The aim of this book is transformation of the style of American management… It requires a whole new structure, from foundation upward.” Deming also advocates the System of Profound Knowledge in which managers (1) appreciate there is a system , (2) understand common-cause and special-cause variation (queueing theory is related to variation), (3) understand limitations of knowledge and reasoning mistakes, and (4) know credible psychology and social research results so that behavior- or motivation-related policies are not based on “common sense.” The core of the book centers around his famous 14 Points for Management , including (for example), “Eliminate management by objective. Eliminate management by numbers, numerical goals. Substitute leadership .” 
--->

<!---
Jay Forrester’s Industrial Dynamics is the classic text on system dynamics—well written and insightful. Although written in the early 1960s, it is as relevant today as when published. It goes beyond cause-effect modeling to also model the flow and inventories of information, money, and material in systems. The book includes formal mathematical modeling but this is not obligatory to appreciate system dynamics.
--->

<!---
Weinberg’s Quality Software Management: Systems Thinking and An Introduction to General Systems Thinking are worthwhile. Written from the perspective of an experienced consultant in systems development. 
--->

<!---
Senge’s The Fifth Discipline is a classic that advocates the need for leadership to apply systems thinking (it is the fifth discipline) and other key disciplines for a great, sustainable enterpise. The others include leaders with (1) personal mastery and (2) reflection on their beliefs and faulty reasoning, the (3) definition and communication of a meaningful shared vision, and (4) the ability of teams to learn. We recommend ignoring—at least during the first few years of practice—the ‘archetypes’ notion presented in the book. It was well meant as a learning aid but has been observed to distract and intimidate people from learning and applying basic system dynamics modeling. The ‘archetypes’ are not part of original system dynamics. 
--->

<!---
The Fifth Discipline Fieldbook is an in-depth resource, written from the viewpoint of many practitioners and consultants. 
--->

<!---
The organizational-learning writings from Argyris, Putnam, McLain, and Schön. Important concepts include double-loop learning and high-advocacy/high-inquiry dialogue. Classic works include Action Science and Organizational Learning. 
--->

<!---
The publications and resources available through the Society for Organizational Learning.
--->

<!---
Notes:
--->

<!---
1. Senge wrote The Fifth Discipline , on systems thinking and learning organizations, named “one of the seminal management books of the last 75 years” by the Harvard Business Review. See** [Senge94].
--->

<!---
2. Another reason: Believing more control is possible than actually is. Complexity science suggests fundamental limits on predicting and controlling semi-chaotic social systems [Stacey07]. This is a rather large can of worms that will remain unopened in this book.
--->

<!---
3. Macroeconomics, psychology, sociology, and biology are exceptions, among many others.
--->

<!---
4. ‘Basic’ does not mean trivial or easy to solve. For example, ‘motivation’ and ‘quality’ are basic but not easy issues.
--->

<!---
5. Feedback loops is occasionally used in this book in the colloquial sense of feedback, rather than this system dynamics sense.
--->
