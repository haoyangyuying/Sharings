### [VENTURE ENGINEER MEETUP](https://eure.connpass.com/event/65067/)

## 「アルゴリズムマネジメント＆デザイン 〜機械学習の技術選定とマネジメントについて〜」

- @showwin
- AI企業、アルゴリズムマネージャ
- scoutyの機能
  - open dataで、会員登録必要なし、経歴、投稿、所属会社、転職履歴などのデータ、退職確率を予測、最適な企業をマッチングする、スカウトを送る
  - 退職率予測：確率分布を予測
  - 転職可能性を高、中、低にする
- アルゴリズムマネージャの仕事
  - AI研究と AIビジネス→ルールベース
  - ビジネスと技術の間でいる人間
- アルゴリズムマネージャはアルゴリズムのプロダクトマネージャー
  - アルゴリズムの精度、ビジネスKPI
- 退職率予測 → 1スカウトあたりのCVR、UIの使い安さ、単価、継続率、売り上げ
- 仕事：
  - メトリクス = 精度指標
    - 年単位か、平均誤差、予測が可能な人数
  - 完璧なversion1がないというスケジュールでアップデートするが大事
    - 事前調査と技術選定、V1.0リリース(経歴を使って予測できるようにする、年単位のprecision50%以上)
    - V1.1リリース：SNS投稿を使って予測できるように
    - 事前リサーチ：データの分布、目的関数との相関性の高い特徴
    - 候補技術を洗い出し
  - 統計的な手法、deeplearning, SVM, 生存時間分析(事前リサーチ)
    - 精度、解釈生、開発工数、必要とするデータ量
    - deeplearning
    - 決定木
    - ルールベース(さっと作れる、ある程度は使える、開発工数は少ない)→　制度をあげる
  - まとめ：いろんな手法を使う感覚、データ量の肌感覚、クライアント・ユーザとの対話能力、経営や事業に関するKPIへの理解、エンジニアのマネジメント能力
  - 理想：CTO から マネージャー：統計が強い、NLPが強い、深層学習が強い
  - 退職率予測アルゴリズム、人材マッチング + その他のアルゴリズム
- ルールベース(比率)：かなり多い
- 学習データ：qiita, github, エンジニアを使っているエンジニア、blogをとる時、skillを予測
- graphデータが必要
- 80万人くらい(データ量)

## 「HR Techの全体像とTalentioが挑戦していること」

- HR Tech
- 労働人口が減少、求人倍率が最高水準で上昇、人材関連のコストが上昇する
- 対策：労働人口を増やす、雇用流動性を高める、人事機能(雇用力)を強くする
- 候補者集める：indeed(求人を集める), linkedin(talentを集める)
- 採用の管理：talentio; 評価：cydas, 総合、分析

- 開発環境：aws vpc ec2 c3, php laravel, reac redux saas webpack yarn,   github confluence jira slack ansible sentry trello zendesk
- 開発で大事なこと：サイクルを回せない、
- 状態を見える化: trelloでカンバン、github issueにp-rのcommitを紐つけるhooks,slackに通知
- 開発のスリム化
- ユーザーサポートは解決まで：ログは事前に収集、zendesk slack issue p-r deploy
- データの民主化：re:dash 全員がデータに触れる環境
- 今後やりたいこと：候補者の情報取得の自動化
  - アグリゲーション、google chromeの拡張昨日で敵強
  - スケジュール調整の自動化
  - people analytics: 候補者のデータ→採用プロセス←コンピテンシー
  - 予想精度を上げる

## 「マイクロサービス化での技術的エントロピーの増大と技術標準化について」

- tcpdump
- エウレカのSREチーム
  - Pairs 台湾版、韓国版準備
  - 7人全員エンジニア
  - インフラ全般、サーバーサイド、アルゴリズム改善
  - 方向性：リリースバッチの最小化、インフラもコード化
- 標準化の必要性
  - プロダクションの本
  - 色々な技術
  - エントロピーを下げる
  - 新しい技術に挑戦するチャンス
  - 可用性：sla uptime downtimeの定義
- 何を標準化するのか
  - netflix  java 言語など
  - 決済, 投稿, ユーザー情報
  - aws codebuild packer
  - 導入した理由：プロビジョニングの排除など
  - ユーザー系のマイクロサービス：goo.gl/BRqkQk
  - インフラコードをモジュール化
  - 韓国：Pairs JPとPairs TW 標準化  投稿審査、ユーザー情報　→　pairs KR
  - 標準化して、今後を拡大しやすい
  - 運用中の標準化
  - 新しいサービスが　新しい技術をトライするチャンス
    - 可用性をなくすために、標準化していく
    - 運用するとき、現存のサービスを追求
