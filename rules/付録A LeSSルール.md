#付録ALeSSルール
<!---
The  LeSS  Rules  are  the  definition  of  the  LeSS  Framework.  They  are
things  we  consider  a  must.  Why?  This  is  explained  in  the  Why  LeSS
description on less.works.
--->
LeSSのルールはLeSSフレームワークを定義するもので、 必須と定めているものです.
なぜLeSSなのかについてはless.worksのWhyLeSSを参照ください.

<!---
LeSS Framework Rules
The LeSS framework applies to products with 2–“8” teams.

--->
## LeSSフレームワークのルール

LeSSフレームワークは2–8チームでの開発向けです.

<!---
### LeSS Structure
- Structure the organization using real teams as the basic organizational building block.
- Each team is（1） self-managing,（2） cross-functional,（3） co-located, and（4） long-lived.
- The majority of the teams are customer-focused feature teams.
- Scrum Masters are responsible for a well-working LeSS adoption. Their focus is towards the Teams, Product Owner, organization, and development practices. A Scrum Master does not focus on just one team but on the overall organizational system.
- A Scrum Master is a dedicated full-time role.
- One Scrum Master can serve 1–3 teams.
- In LeSS, managers are optional, but if managers do exist, their role is likely to change. Their focus shifts from managing the day-to-day product work to improving the value-delivering capability of the product development system.
- Managers’ role is to improve the product development system by practicing Go See, encouraging Stop & Fix, and “experiments over conformance.”
- For the product group, establish the complete LeSS structure “at the start”; this is vital for a LeSS adoption.
- For the larger organization beyond the product group, adopt LeSS evolutionally by using Go and See to create an organization where experimentation and improvement is the norm.

--->
### LeSSの構造

- 実際のチームを組織の基本単位としてブロックとして組み立てるように組織を構成します.
- 各チームは、（1）自己管理、（2）クロスファンクショナル、（3）同一ロケーション、（4）長期間存続とします.
- チームの大半は顧客中心のフィーチャーチームです.
- スクラムマスターはLeSS導入がうまく機能していることに責任をもちます.注力する対象は、チーム、 プロダクトオーナー、 組織、 技術的手法の改善であり、 各スクラムマスターは1チームだけの改善にとどまることなく、 組織全体の改善を行う必要があります。
- スクラムマスターは専任で専従の役割です.
- 1人のスクラムマスターは1–3チームを担当できます.
- LeSSではマネージャーは必須ではありませんが、 参加している場合でも多くの場合役割が変わります.マネージャーの仕事は、 日々の作業の管理ではなく、 プロダクトを開発するシステム全体の価値提供能力の向上に移ります.
- マネージャーの役割はプロダクト開発の仕組みの改善促進です.現地現物の実践、 
止めて直すの推奨、 「現状維持をせずに実験を繰り返すこと」を通じて改善を促進します.
- 単一のプロダクトグループへの導入では、 最初から教科書的なLeSSの体制をつくるようにします.これはLeSSの導入にとって不可欠です.
- さらに大きなプロダクトグループを越えて大規模な組織にに導入する場合は、 現地現物を用いて、 実験と改善が当り前であるような組織をつくり、 段階的にLeSSを導入します.

<!---
### LeSS Product
- There is one Product Owner and one Product Backlog for the complete shippable product.
- The Product Owner shouldn’t work alone on Product Backlog refinement; he is supported by the multiple Teams working directly with customers/users and other stakeholders.
- All prioritization goes through the Product Owner, but clarification is as much as possible directly between the Teams and customer/users and other stakeholders.
- The definition of product should be as broad and end-user/customer-centric as is practical. Over time, the definition of product might expand. Broader definitions are preferred.
- There is one Definition of Done for the whole product, common for all teams.
- Each team can have its own stronger Definition of Done by expanding the common one.
- The perfection goal is to improve the Definition of Done so that it results in a shippable product each Sprint（or even more frequently）.

--->
## LeSSのプロダクト
-プロダクトオーナーが1人、 プロダクトバックログが1つあり、 出荷可能なプロダクト全体を運用します.
-プロダクトオーナーだけでプロダクトバックログリファインメントをするべきではありません.複数のチームが顧客やユーザー、 ステークホルダーと直接コミュニケーションをとり、 プロダクトオーナーをサポートします.
-すべての優先順位付けはプロダクトオーナーに確認をとりますが、 要求や仕様の詳細確認は極力チーム間や顧客、 ユーザーまたはステークホルダーと直接行います.
-プロダクトの定義は現実的な範囲で、 広くエンドユーザーまたは顧客視点中心であるべきです.時間の経過とともにプロダクトの定義は広がるかもかもしれませんが、 広がっていくことは望ましいことです.
-プロダクト全体で全チーム共通の1つのDoneの定義をもちます.
-各チームは共通のDoneの定義を拡張してより厳しい独自のものを定めても構いません.
-究極の目標はDoneの定義を拡張し、 毎スプリント(あるいはより高い頻度で）出荷可能なプロダクトをつくれるようになることです.

<!---
### LeSS Sprint
- There is one product-level Sprint, not a different Sprint for each Team. Each Team starts and ends the Sprint at the same time. Each Sprint results in an integrated whole product.
- Sprint Planning consists of two parts: Sprint Planning One is common for all teams, whereas Sprint Planning Two is usually done separately for each team. Do multi-team Sprint Planning Two in a shared space for closely related items.
- Sprint Planning One is attended by the Product Owner and Teams or Team representatives. Together, they tentatively select the items that each team will work on during that Sprint. The Teams identify opportunities to work together, and final questions are clarified.
- Each Team has its own Sprint Backlog.
- Sprint Planning Two is for Teams to decide how they will do the selected items. That usually involves design and the creation of their Sprint Backlogs.
- Each Team has its own Daily Scrum.
- Cross-team coordination is decided by the teams. Prefer decentralized and informal coordination over centralized coordination. Emphasize Just Talk and informal networks through communicating in code, cross-team meetings, component mentors, travelers, scouts, and open spaces.
- Product Backlog Refinement（PBR） is done per team for the items they will likely do in the future. Do multi-team and/or overall PBR to increase shared understanding, and exploit coordination opportunities when having closely related items or a need for broader input/learning.
- There is one product Sprint Review; it is common for all teams.
Ensure that suitable stakeholders join to contribute the information needed for effective inspection and adaptation.
- Each Team has its own Sprint Retrospective.
- An Overall Retrospective is held after the Team Retrospectives to discuss cross-team and systemwide issues and to create improvement experiments. In attendance are Product Owner, Scrum Masters, Team Representatives, and managers（if any）.

--->
### LeSSのスプリント

- 1つのプロダクトに関わるチームはすべて、 同じスプリントで作業します.スプリントの開始も終了も、 全チーム共通です.スプリントの終わりにはプロダクト全体が1つに統合されている状態にします.
- スプリントプランニングは2つのパートに分かれます.スプリントプランニング1はすべてのチームが合同で実施します.それに対してスプリントプランニング2は通常、 各チームに分かれて別々で開きます.ただし、 関連性が強いアイテムをもっているチームは同じ場所で、 複数チームのスプリントプランニングとして一緒に行います.
- スプリントプランニング1はプロダクトオーナーと全チームまたはチームの代表で行います.参加者は一緒に、 各チームがこのスプリントで作業するアイテムをいったん選択します.チームは協働する部分や不明確な点を見つけ、 残った疑問があれば解決します.
- 各チームはチームごとのスプリントバックログを有します.
- スプリントプランニング2は各チームがどうアイテムを実現させるかを考える場であり、 設計やスプリントバックログの作成を行います.
- デイリースクラムはチームごとに行います.
- チームどうしの調整はチームに委ねられています.中央集権的な調整ではなく、 個別の判断で自由かつ非公式に調整する方が好ましいです.重要なのは、 ただ話すや、 非公式のコミュニケーションであるコード上でのコミュニケーション、 チームを横断した会議、 コンポーネントメンター、 トラベラー、 偵察、 そしてオープンスペースを活用することです.
- プロダクトバックログリファインメント(PBR）は、 将来そのチームが対応しそうなアイテムについてチームごとに行われます.複数チームや全体でPBRを行うのは、 関連性が強いアイテムがあったり、 より広範なインプットと学び得る必要があるときに、 共通理解を深め、 互いに関連したPBIについて協力する方法を探ったりするためです.
- スプリントレビューはすべてのチームが共同で行います.検証と適応を行うのに適切な情報を得られるよう、 必要なステークホルダーが参加するようにします.
- スプリントレトロスペクティブは各チームで行います.
- オーバーオールレトロスペクティブは各チームのレトロスペクティブの後に行われます.ここでは複数チームやシステム全体にまたがる課題を扱い、 改善に向けての試みを議論します.この場にはプロダクトオーナー、 全スクラムマスター、 チーム代表と、（いるなら）マネージャーが参加します.

<!---
## LeSS Huge Framework Rules
LeSS  Huge  applies  to  products  with  “8+”  teams.  Avoid  applying  LeSS Huge to smaller product groups as its principles will result in more over-head and local optimizations. 

All LeSS rules apply to LeSS Huge unless otherwise  stated.  Each  Requirement  Area  acts  like  the  basic  LeSS framework.
--->

## LeSSHugeフレームワークのルール

LeSS Hugeはプロダクトを8チーム以上でつくる場合に適用します.これよりも小さな規模でLeSSHugeを適用することは推奨しません.不必要なオーバーヘッドや部分最適の原因となります.

特に明記しない限り、 すべてのLeSSのルールはLeSSHugeにも適用されます.各要求エリアは、 基本的なLeSSのフレームワークのように働きます.

<!---
### LeSS Huge Structure
- Customer requirements that are strongly related from a customer perspective are grouped in Requirement Areas.
- Each Team specializes in one Requirement Area. Teams stay in one area for a long time. When there is more value in other areas, teams might change Requirement Area.
- Each Requirement Area has one Area Product Owner.
- Each Requirement Area has between “4-8” teams. Avoid violating this range.
- LeSS Huge adoptions, including the structural changes, are done with an evolutionary incremental approach.
- Remember each day: LeSS Huge adoptions take months or years, infinite patience, and sense of humor.
--->
### LeSSHugeの構造
- 顧客視点で強く関連する顧客要求は、要求エリアにまとめます.
- 各チームは1つの要求エリアに特化します.チームは長期間1つのエリアにとどまりますが他のエリアに、 より価値がよりがあると判断した場合、 チームは要求エリアを変更することもあります.
- それぞれの要求エリアには1人のエリアプロダクトオーナーがいます.
- それぞれ要求のエリアには、 「4–8」チームが含まれます.この範囲を超えてはいけません.
- LeSS Hugeの導入には、 組織の構造変更を伴いますので、 進化させながら、 インクリメンタルに進めます.
- 忘れないでください.LeSSHugeの導入には多くの年月、 計り知れない忍耐、 そしてユーモアのセンスが必要です.

<!---
### LeSS Huge Product
- Each Requirement Area has one Area Product Owner.
- One（overall） Product Owner is responsible for product-wide prioritization and for deciding which teams work in which Area. He works closely with Area Product Owners.
- Area Product Owners act as Product Owners towards their teams.
- There is one Product Backlog; every item in it belongs to exactly one Requirement Area.
- There is one Area Product Backlog per Requirement Area. This is conceptually a more granular view into the one Product Backlog.
--->
### LeSS Hugeのプロダクト
- 各要求エリアにはエリアプロダクトオーナーが1人ずついます.
- オーバーオールプロダクトオーナーの役割はプロダクト全体の優先順位決めと、 どのチームがどのエリアを対応するかを決めることとなります.そして、 エリアプロダクトオーナーと密にコミュニケーションをとる必要があります.
- エリアプロダクトオーナーは当該エリアのチームに対してプロダクトオーナーとしてふるまいます.
- プロダクトバックログは1つ.すべてのアイテムは1つの要求エリアごとに属します.
- 要求エリアごとにエリアプロダクトバックログ「(エリアバックログ」）が1つあります.このバックログは概念上1つの、 プロダクトバックログのより詳細なビューです.

<!---
### LeSS Huge Sprint
- There is one product-level Sprint, not a different Sprint for each Requirement Area. It ends in one integrated whole product.
- The Product Owner and Area Product Owners synchronize frequently. Before Sprint Planning they ensure that the Teams work on the most valuable items. After the Sprint Review, they further enable product-level adaptations.
--->
### LeSS Hugeのスプリント
- プロダクト単位で共通のスプリント期間とします.各要求エリアで別々のスプリント期間とすることはありません.すべてのチームがすべての要求エリアを超えて、 プロダクト全体にわたって継続的に統合し、 スプリントの終わりには統合された1つのプロダクトになっている必要があります.
- プロダクトオーナーとエリアプロダクトオーナーは頻繁に会話し、 スプリントプランニング時にチームが最も価値の高いアイテムに着手できるように準備する必要があります.また、 スプリントレビュー後にはプロダクト規模の適応を推し進めます.